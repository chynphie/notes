- "Normal distribution" may fail to capture the likelihood of **large values**, so we use t-distribution.
- $X \sim t_d(\nu, \mu; \Sigma)$, where $\nu$ is the **degrees of freedom**.
- Stochastic representation:
	- $X = \mu + \sqrt{W} A Z$, where $Z \sim N_d(0, I_d)$, We want $W \sim IG(\psi_1, \psi_2)$, since $X \sim \text{Gamma}(\alpha, \beta)$ and $\frac{1}{X} \sim IG(\alpha, \beta)$, $\Rightarrow$ Sample $W \sim \text{Gamma}(\nu/2, \nu/2)$.
- #### Sample from t-distribution Algorithm
	1. Sample $Z$
	2. Sample $W$
	3. Return $X = \mu + \sqrt{W} A Z$
