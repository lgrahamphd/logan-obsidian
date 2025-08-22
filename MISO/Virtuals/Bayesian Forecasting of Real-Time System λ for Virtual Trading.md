## Introduction
In modern organized electricity markets, the **day-ahead (DA)** and **real-time (RT)** energy markets operate in tandem. Participants submit DA bids and offers based on forecasts, but the **true cost** of balancing supply and demand unfolds in RT. For traders in **virtuals** (increment offers and decrement bids), the profit depends on the difference between the RT price and the DA clearing price.

A **Bayesian framework** provides a coherent way to:

1. Incorporate **uncertainty** in forecasts—load, renewables, outages—through probability distributions.  
2. **Update beliefs** sequentially as new information arrives (e.g., RT price observations, DA settlement).  
3. Produce **full predictive distributions**, not just point estimates, to support risk-aware bid sizing.

This guide walks through two models:

- **Model A1**: the *unconditional* predictive distribution of RT λ using only **pre-DA** information.  
- **Model A2**: the *conditional* predictive distribution of RT λ **given** the observed DA clearing price, which is crucial for valuing virtual bids.

We assume you are comfortable with calculus, linear algebra, and basic probability, but provide all necessary Bayesian concepts in situ.
## 1 Bayesian Primer
Bayes’s theorem updates a **prior** belief $p(\theta)$ about unknown parameters $\theta$ in light of **data** $y$ using the **likelihood** $p(y|\theta)$:

$$
p(\theta \mid y)
=
\frac{p(y \mid \theta)\, p(\theta)}{\displaystyle\int p(y\mid\theta)\,p(\theta)\,d\theta}.
$$

Once we have the **posterior** $p(\theta\mid y)$, predictions for a new observation $y^*$ follow by marginalizing $\theta$:

$$
p(y^* \mid y)
=
\int p(y^* \mid \theta)\,p(\theta \mid y)\,d\theta.
$$

A **conjugate prior** is chosen so that the posterior stays in the same family as the prior, yielding closed-form updates.  In **sequential** settings, we treat the posterior at time $t-1$ as the prior for time $t$, enabling **online** updates without full re-estimation.
## 2 Dynamic Linear Model (DLM)
We let $z_t = \log \lambda_t^{\mathrm{RT}}$ denote the logged RT price.  A **state-space** (or DLM) representation has two parts:
1. **State evolution (random walk)**  
   $$
   \boldsymbol\theta_t
   = 
   \boldsymbol\theta_{t-1}
   + 
   \boldsymbol\eta_t,
   \qquad
   \boldsymbol\eta_t \sim \mathcal N(\mathbf{0},\mathbf{W}),
   $$
   where $\boldsymbol\theta_t = (\alpha_t,\gamma_t)^\top$ encodes a time-varying **bias** $\alpha_t$ and **scale** $\gamma_t$.

2. **Measurement (observation) equation**  
   Conditional on a weather/load scenario $s$, we write
   $$
   z_t
   = 
   \alpha_t
   + \gamma_t\,\log \lambda^{\mathrm{base},(s)}_t
   + \boldsymbol\beta^\top \mathbf w_t
   + \varepsilon_t,
   \qquad
   \varepsilon_t \sim \mathcal N(0,\sigma_\varepsilon^2),
   $$
   where $\mathbf w_t$ contains deterministic covariates (fuel spreads, calendar dummies, etc.) and $\boldsymbol\beta$ are their static coefficients.

Because both the state noise $\boldsymbol\eta_t$ and the measurement noise $\varepsilon_t$ are Gaussian and the relationships are linear in $\boldsymbol\theta_t$, the **Kalman filter** yields the exact posterior
$$
p(\boldsymbol\theta_t \mid z_{1:t},s)
$$
for each scenario $s$ in closed form.
## 3 Scenario Mixture

We generate 51 Monte-Carlo scenarios for load and renewables.  Let the latent variable $S_t \in \{1,\dots,51\}$ have prior probabilities $\{\omega_{t,s}\}$.  The **regular-regime** predictive density for $z_t$ is then the exact mixture

$$
p_{\mathrm{reg}}(z_t \mid z_{1:t-1})
=
\sum_{s=1}^{51}
\omega_{t,s}\,
\mathcal N\!\bigl(z_t;\,\mu_{t,s},\,v_{t,s}\bigr),
$$
where each $(\mu_{t,s},v_{t,s})$ comes from the Kalman one-step forecast under scenario $s$.  This mixture preserves the full uncertainty from our ensemble.
## 4 Modeling Scarcity Spikes (GPD Tail)
While $z_t$ is roughly Gaussian in its central bulk, extreme upward **spikes** occur rarely but violently.  To capture them:

1. Select a high **threshold** $u$ (e.g.\ the 97.5 percentile of historical prices).  
2. Introduce a binary regime $R_t\sim\mathrm{Bernoulli}(\pi_t)$, where  
   $$
   \pi_t = \mathrm{logit}^{-1}(\boldsymbol\eta^\top \mathbf q_t)
   $$
   depends on **scarcity indicators** $\mathbf q_t$ (reserve margin shortfall, outage flags, etc.).  
3. If $R_t=1$, model the exceedance $y_t - u$ with a **Generalised Pareto distribution (GPD)**:
   $$
   p(y_t \mid R_t=1)
   =
   \mathrm{GPD}(y_t - u;\,\sigma,\xi),
   $$
   where the **shape** $\xi>0$ controls tail heaviness.
The **overall** predictive for the original price $y_t=\exp(z_t)$ is

$$
p(y_t \mid \mathcal D_{t-1})
=
(1-\pi_t)\,p_{\mathrm{reg}}(y_t)
\;+\;
\pi_t\,p_{\mathrm{spike}}(y_t).
$$
## 5 Model A1 – Unconditional Predictive

Putting together the DLM, scenario mixture, and GPD tail, **Model A1** delivers the full predictive density of $\lambda_t^{\mathrm{RT}}$ **before** the DA price is known.

---

## 6 Model A2 – Conditioning on the DA Clearing Price
When the ISO publishes the DA clearing price $\lambda_t^{\mathrm{DA}}$, we denote its log by $d_t = \log \lambda_t^{\mathrm{DA}}$.  Empirically, the **expected RT price** rises **convexly** as $d_t$ falls below the “efficient” level.  To encode this, we augment the measurement equation with a **convex function** $f(d_t)$, for example a quadratic spline:
$$
f(d_t)
=
\delta_0\,d_t
\;+\;
\delta_1\,\max\{d^\star - d_t,0\}
\;+\;
\delta_2\,\max\{d^\star - d_t,0\}^2,
\quad
\delta_2 > 0.
$$
The updated measurement equation becomes
$$
z_t
=
\alpha_t
+ \gamma_t\,\log \lambda_t^{\mathrm{base},(S_t)}
+ \boldsymbol\beta^\top \mathbf w_t
+ f(d_t)
+ \rho\,\varepsilon_t^{\mathrm{DA}}
+ \tilde\varepsilon_t,
$$
where $\varepsilon_t^{\mathrm{DA}}\sim\mathcal N(0,\sigma_{\mathrm{DA}}^2)$ is the DA pricing error.  Because $f(d_t)$ is known once the DA clear arrives, the model remains **linear** in $(\alpha_t,\gamma_t,\delta)$ and the Kalman filter still applies.
## 7 Sequential Inference via Particle Filtering
To handle the latent **scenario** $S_t$ and **regime** $R_t$, we embed the Kalman filter within a **particle filter**:

Initialize N particles with state priors
FOR each time t:
  FOR each particle i:
    1. Predict state (α,γ,δ) via random walk
    2. Sample S_t^(i) ~ Categorical(ω_t)
    3. Sample R_t^(i) ~ Bernoulli(π_t)
    4. Compute likelihood:
         if R_t=0 → Normal(z_t | μ_{t,s}, v_{t,s})
         else      → GPD(y_t | u,σ,ξ)
    5. Update weight_i *= likelihood
  Normalize weights; resample if ESS low
1. **Overnight**: re-estimate static hyperparameters $(\mathbf W,\sigma_\varepsilon,\xi,\rho,\boldsymbol\eta)$ via MCMC on recent history.
2. **Pre-DA**: generate 51 scenarios, run production-cost → $\lambda^{\mathrm{base},(s)}$, filter on recent RT prices → update $(\alpha,\gamma)$.
3. **DA close**: observe $\lambda^{\mathrm{DA}}$, compute $f(d_t)$, update via Kalman → **Model A2** predictive $p(\lambda^{\mathrm{RT}}\mid\lambda^{\mathrm{DA}})$.
4. **Bid sizing**: feed the conditional predictive into a CVaR-constrained optimisation for DEC/INC positions.
### Why This Matters
1. Full predictive distributions capture **tail risk** essential for CVaR-based bid sizing.
2. Convex conditional mean ensures **asymmetric upside** for under-priced DA outcomes and **corrects** otherwise linear biases.
3. Sequential updates keep the model **adaptive** to evolving system conditions without manual re-calibration.
## Further Reading
- Gelman et al., _Bayesian Data Analysis_ (3rd ed.), Chapters 2–4.
- West & Harrison, _Bayesian Forecasting and Dynamic Models_, Sections on DLM and mixture extensions.
- Coles, _An Introduction to Statistical Modeling of Extreme Values_, for GPD tails.