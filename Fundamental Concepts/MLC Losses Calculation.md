Consider a bus $i$ for which a pnode is defined. Write $LMP_i$ for its locational marginal price. The pnode's locational marginal price can be decomposed into the sum of its *marginal energy component (MEC, $\lambda$)*, *marginal congestion component (MCC)*, and the *marginal loss component (MLC)*:
$$
LMP_i = \lambda + MCC_i + MLC_i.$$
$MEC$ is constant across the footprint. It represents the price of delivering an incremental unit of power at the slack bus (in PJM and MISO, "slack bus" refers more precisely to a load-weighted, distributed slack bus).

We write $S_{ik}$ for the *power transfer distribution factor (PTDF)* associated with a unit increase in injection at bus $i$ and a corresponding unit increase in withdrawal at the slack bus (such PTDFs are sometimes called *generator shift factors*). This is the increase in flows over element $k$ associated with such injection and withdrawal. The marginal congestion component $MCC_i$ is the inner product of all binding constraints' shadow prices $\mu_k$ for constraints $k \in K$ and the corresponding PTDFs:
$$MCC_i = \sum_{k=1}^K S_{ik} \mu_k.$$
Bus $i$'s *loss factor* $LF_i$ is the sensitivity of system losses to a unit increase in injection at bus $i$. Multiplying the loss factor by $-\lambda$ yields the marginal loss component at bus $i$:
$$MLC_i = -LF_i \cdot \lambda.$$
In some settings, it's more natural to refer to bus $i$'s *delivery factor* $DF_i = 1 - LF_i$.

---
Write $P_L$ for aggregate system losses, $\Delta P_L$ for changes in aggregate system losses, and $\Delta P_i$ for changes in net injection at bus $i$ ($\Delta P_i > 0$ corresponds to increased injection/decreased withdrawals at bus $i$). Then, $$MLC_i = -\lambda \cdot LF_i.$$
Assuming $\lambda \neq 0$, it follows that
$$\frac{MLC_i}{\lambda} = -LF_i.$$
---
### Losses = $I^2 R$
By definition, real power $P$ is the product of current $I$ and voltage (difference) $V$
$$P = I \cdot V.$$Ohm's Law states that current flowing over a circuit is directly proportional to the voltage difference across the circuit. Let $R$ denote the corresponding constant of proportionality, and refer to it as the circuit's *resistance*. Then, we may express Ohm's Law via the equation $$I = V / R.$$Solving for $V$, we obtain $V = I \cdot R$. Substituting this into the definition of power, it follows that
$$P_\ell = I_\ell^2 R,$$which represents losses on branch $\ell$ (in the form of heat dissipation) attributable to resistance.
#### Implications
1. Losses increases with line length, for longer lines result in increased resistance (all else equal).
2. Losses decrease with line voltage (all else equal). Since power lost to heat dissipation grows *quadratically* with current, and $P = I \cdot V$, simultaneously increasing $V$ and decreasing $I$ while holding their product $P$ fixed leads to a decrease in line loss that scales quadratically with the current decrease.

---
### Estimating power flow from losses
Since $P = I \cdot V$, and Ohm's Law gives $I = V/R$, losses on branch $\ell$ can be expressed as follows:
$$Loss_\ell = \frac{P_\ell^2}{V^2}\cdot R.$$
Writing $S_{i \ell}$ for the generation shift factor associated with injection at bus $i$, withdrawals at the slack bus, and flow over branch $\ell$, 
$$\frac{MLC}{\lambda} = -\frac{\Delta P_\ell^2}{\Delta P_i}\cdot\frac{R}{V^2}.$$
Therefore,
$$
\frac{MLC}{\lambda} = -S^2_{i \ell} \cdot \frac{R}{V^2}.
$$
As a key consideration, one might filter the considered shift factors $S_{i\ell}$ to restrict oneself to only those with sufficiently large absolute value.

Let $P_f$ denote a penalty factor, designed to adjust the incremental cost of each generator to account for losses. Note that, when injection *increases* system losses, $$P_f = \frac{1}{DF_i} \to P_f > 1.0.$$