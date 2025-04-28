- For any random vector $X = (X_1, \dots, X_d)$ with **continuous** margins, the probability-transformed vector $U = (F_1(X_1), \dots, F_d(X_d))$ is such that:
	$U_j \sim U(0,1)$ for $j = 1, \dots, d$.
- The joint distribution of $(U_1, \dots, U_d)$ determines the dependence among $(X_1, \dots, X_d)$.

- A **copula** is a $d$-dimensional function with $U(0,1)$ marginal distributions (i.e., the joint CDF of $(U_1, \dots, U_d)$ where $U_j \sim U(0,1)$).
- Example:  $$C(U_1, \dots, U_d) = \prod_{j=1}^{d} U_j$$is the **independence copula**.
- #### Sklar’s Theorem
	1. If $F$ is a CDF with continuous margins $F_1, \dots, F_d$, then there’s a unique copula $C$ such that:$$F(x) = C(F_1(X_1), \dots, F_d(X_d)), \quad x \in \mathbb{R}^d$$
	2. The copula $C$ is given by: $$C(U) = F(F_1^{-1}(U_1), \dots, F_d^{-1}(U_d))$$for $U \in [0,1]^d$. Furthermore,$U = (F_1(X_1), \dots, F_d(X_d)) \sim C$ for $X \sim F$.
	3. Conversely, if $U \sim C$ for a copula $C$ and $F_1, \dots, F_d$ are continuous CDFs, then $F$ defined above is a CDF with copula $C$ and margins $F_1, \dots, F_d$.  
		Furthermore, $X = (F_1^{-1}(U_1), \dots, F_d^{-1}(U_d)) \sim F$ for $U = (U_1, \dots, U_d) \sim C$.
	- *Proof*: 
		- Let $X = (X_1, X_d) \sim F$. Let $U = (U_1, U_d)$ where $U_j = F_j(X_j)$. Then $U_j$ denotes the joint CDF of $U$, which is a copula. Then:
			- $P(U_1 \leq u_1, \dots, U_d \leq u_d) = P(F_1(X_1) \leq u_1, \dots, F_d(X_d) \leq u_d)$
			- $= P(X_1 \leq F_1^{-1}(u_1), \dots, X_d \leq F_d^{-1}(u_d))$
			- $= F(F_1^{-1}(u_1), \dots, F_d^{-1}(u_d))$
		- Since the joint CDF of $(F_1(X_1), \dots, F_d(X_d)) = C$.
-  **Algorithm**
	1. Find copula $C$ of $F$.
	2. Sample $U = (U_1, \dots, U_d) \sim C$.
	3. Return $X = (F_1^{-1}(U_1), \dots, F_d^{-1}(U_d))$.

-  **Steps determine a Copula**
	1. calculate the marginal cdf ($\sim U(0,1)$ and continues? )
	2. calculate the $F_{i}^{-1}$ write in $U_{i}$
	3. Substitute in $F_{i}^{-1}$ in to orginal F to get $C(u)=F(F_{i}^{-1}(x_{i}))$

-  ***Special Copulas***:
	- **Independent copula: $C(u)=\prod_{j=1}^{d}u_{i}, u \in[0,1]^{d}$**
	- **Comonotonicity Copula  *(perfect positive dependence)***  
		- Definition:  
			- $M(u) = \min \{u_1, \dots, u_d\}, \quad u \in [0,1]^d$
	- **Counter monotonicity Copula *(perfect negative dependence)***  
		- Definition:  
			- $W(u) = \max \{u_1 + u_2 - 1, 0\}, \quad u \in [0,1]^2$
		- Properties:  
			- $U = (U, 1 - U) \sim W$ for $U \sim U(0,1)$
	- **Probability Expression:**
		- $P(U \leq u_1, V \leq u_2) = P(U \leq \min\{u_1, u_2\})= \min \{u_1, u_2\}, \quad u_i \in [0,1]$
	![[Pasted image 20250313210157.png]]
- *Sampling from implicit Copulas*:
	a)Sample $X = (X_{1}, . . . ,X_{d}) ∼ N_d (0, P).$
	b)