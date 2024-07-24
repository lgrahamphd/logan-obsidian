Conditional Value-at-Risk (CVaR) represents a conditional expectation of loss.
### Key Takeaway
Rockafellar and Uryasev (1999) showed that we can minimize CVaR using a linear program. The authors created an auxiliary function $F_\beta (x, \alpha)$, which is linear in $x$ (and often linear in $(x, \alpha)$). By minimizing $F_\beta(x, \alpha)$, one minimizes CVaR.
### Notes
Let $f(x, y)$ denote the loss associated with decision vector $x$ and uncertainties $y$, where $Y$ is a random vector.

Define $\psi (x, \alpha)$ as the probability of the loss $f(x, y)$ being at most $\alpha$:
$$\psi (x, \alpha) := \int_{f(x, y) \ge \alpha} p(y) dy.$$
That is, $$\psi(x, a) = \mathbb{P} \{f(x, y) \le \alpha \}.$$
##### Value-at-Risk (VaR)
The $\beta$-Value-at-Risk (VaR) is defined as
$$\alpha_\beta (x) := \min_{\alpha \in \mathbb{R}} \psi (x, \alpha) \ge \beta.$$
This is the minimum value $\alpha$ such that the probability of loss $f(x, y)$ being no more than $\alpha$ is at least $\beta$. More intuitively, the $\beta$-VaR is the loss associated with a probability $\beta$ event.
##### Conditional Value-at-Risk (CVaR)
The $\beta$-Conditional Value-at-Risk (CVaR) is defined as $$\phi_\beta (x) := \frac{1}{1-\beta} \int_{f(x, y) \ge \alpha_\beta (x)} f(x, y) p(y) dy.$$
This is the conditional expectation of loss given that it is at least $\alpha_\beta (x)$. More intuitively, the $\beta$-CVaR is the conditional expectation of loss given that a probability $\beta$ event has occurred.
##### Auxiliary Function
Define
$$F_\beta (x, \alpha) := \alpha + \frac{1}{1-\beta} \int_{y \in \mathbb{R}^n} [f(x, y) - \alpha]^+ p(y)dy,$$
where $[x]^+ = x$ where $x \ge 0$, and $[x]^+ = 0$ where $x \le 0$. That is, $F_\beta (x, \alpha)$ is the expectation of loss in excess of $\alpha$, where $\alpha$ is the $\beta$-VaR.
##### Theorem 1
$$\phi_\beta (x) = \min_{\alpha \in \mathbb{R}} F_\beta (x, \alpha).$$
That is, the $\beta$-CVaR associated with a given decision vector $x$ can be computed by minimizing $F_\beta (x, \alpha)$ with respect to $\alpha$.
##### Theorem 2
$$\min_{x \in X} \phi_\beta (x) = \min_{(x, \alpha) \in X \times \mathbb{R}} F_\beta (x, \alpha).$$
That is, the decision vector $x^*$ that minimizes the $\beta$-CVaR can be computed by minimizing $F_\beta (x, \alpha)$ with respect to $(x, \alpha)$. $\alpha^*$ gives the $\beta$-CVaR corresponding to the optimal decision vector $x^*$.

When $X$ is a polytope and $f(x, y)$ is linear in its arguments, then the problem of minimizing $F_\beta (x, \alpha)$ over $(x, \alpha) \in X \times \mathbb{R}$ reduces Linear Programming.
##### Application to Portfolio Optimization
Let $x$ denote the vector of portfolio allocation proportions, and let $y$ denote the vector of returns for the instruments associated with $x$'s elements. Then, $x^T y$ is portfolio return, and $-x^T y$ is the portfolio loss $f(x, y)$. 

Substituting $f(x, y) = -x^T y$, the auxiliary function becomes $$F_\beta (x, \alpha) = \alpha + \frac{1}{1-\beta} \int_{y \in \mathbb{R}^n} [-x^T y - \alpha]^+ p(y) dy.$$
$F_\beta (x, \alpha)$ is therefore linear in $(x, \alpha)$.

Our objective is to minimize the $\beta$-CVaR subject to $x \ge 0$, $\mathbb{E}[x^T y] \ge R_0$, where $R_0$ is a minimum acceptable return. Due to the above results, this can be done by minimizing $F_\beta (x, \alpha)$, which is possible via reduction to Linear Programming by Theorem 2.
### Extensions of the Portfolio Optimization Application
Rockafellar's and Uryasev's results hold if *return* is substituted for *loss*. For example, one might wish to maximize a conditional expectation of return plus an expected return minus a conditional expectation of loss.

Let $R$ be a random variable denoting return. Define the $\beta$-Value-to-Gain (VtG) as the return associated with a probability $\beta$ event, and define the $\beta$-Conditional Value-to-Gain (CVtG) as the conditional expectation of return given that a probability $\beta$ event has occurred.

Then, with tuning parameters $\gamma_1, \gamma_2, \gamma_3$, we might seek to maximize $$\gamma_1 \cdot \beta \text{-CVtG} + \gamma_2 \cdot \mathbb{E}[R] - \gamma_3 \cdot \beta\text{-CVaR}.$$
Of course, this is linear in $(x, \alpha)$ due to Rockafellar's and Uryasev's results. The intuition behind this is that one should target both expected return and positive tails, while one should seek to avoid negative tails.
### Paper
![[Optimization of Conditional Value-at-Risk.pdf]]