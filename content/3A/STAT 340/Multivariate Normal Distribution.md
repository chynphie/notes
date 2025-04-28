- Given a d-dimensional random vector $X = (X_1, ..., X_d)$ with joint cdf $F(x_1, ..., x_d) = P(X_1 \leq x_1, ..., X_d \leq x_d), x_1, ..., x_d \in \mathbb{R}$, we sample (multivariate) realizations of $F$.
- Vectors $(X_1, ..., X_d) \in \mathbb{R}^d$ stored in an $(n, d)$ matrix, where the j-th row is a realization of $X_j$.
### Sampling Random Vectors with Independent Components
- Let $X = (X_1, ..., X_d)$ be a d-dim. r.v. with joint cdf $$F(X) = P(X \leq x) = P(X_1 \leq x_1, ..., X_d \leq x_d), X \in \mathbb{R}^d$$For $j = 1, ..., d$, the j-th marginal of $F$ is $F_j(x_j) = P(X_j \leq x_j) = F(\infty, ..., x_j, \infty, ...)$
- Assume $F(X_1, ..., X_d) = \prod_{j=1}^{d} F_j(X_j)$, so that $X_1, ..., X_d$ are mutually independent.
#### Algorithm:
1. Sample $X_j \sim F_j$ independently for $j=1,...,d$ (via $X_j = F_j^{-1}(U_j)$ for independent $U_1, ..., U_d \sim U(0,1)$)
2. Return $X = (X_1, ..., X_d)$

 - Example
	- If $Z_1, ..., Z_d \overset{iid}{\sim} N(0,1)$, then $Z = (Z_1, ..., Z_d)$ follows the standard normal distribution $Z \sim N(0, I_d)$.  Let  and  be positive definite. Then a lower-triangular matrix  such that  (computed via t(chol(Sigma))).
	- Let $Z \sim N(0, I_d)$ and define $X \sim N(\mu, \Sigma)$ via:
		- $X = \mu + AZ$, or explicitly,
		- $X_1 = \mu_1 + a_{11}Z_1$
		- $X_2 = \mu_2 + a_{21}Z_1 + a_{22}Z_2$
		- $\vdots$
		- $X_d = \mu_d + a_{d1}Z_1 + a_{d2}Z_2 + ... + a_{dd}Z_d$
	- Algorithm:
		1. Compute $A$ such that $AA^T = \Sigma$
		2. Sample $Z_1, ..., Z_d \overset{iid}{\sim} N(0,1)$ (e.g., via $Z_j = \Phi^{-1}(U_j)$ for $U_1, ..., U_d \sim U(0,1)$)  
		3. Return $X = \mu + AZ$
	

### Multivariate Normal and t-distribution
- "Normal distribution" may fail to capture the likelihood of **large values**, so we use t-distribution.
- $X \sim t_d(\nu, \mu; \Sigma)$, where $\nu$ is the **degrees of freedom**.
- Stochastic representation:
	- $X = \mu + \sqrt{W} A Z$, where $Z \sim N_d(0, I_d)$, We want $W \sim IG(\psi_1, \psi_2)$, since $X \sim \text{Gamma}(\alpha, \beta)$ and $\frac{1}{X} \sim IG(\alpha, \beta)$, $\Rightarrow$ Sample $W \sim \text{Gamma}(\nu/2, \nu/2)$.
- #### Sample from t-distribution Algorithm
	1. Sample $Z$
	2. Sample $W$
	3. Return $X = \mu + \sqrt{W} A Z$