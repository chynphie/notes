***Goal***: 
- To improve the convergence order $\frac{1}{\sqrt{ n }}$, and decrease $\sigma$ or $\sigma^{2}$
- VRTs aim to reduce variance without changing the expected value 
1. **(AV) Antithetic Variates** 
	- **Formula**: $\frac{1}{{n/2}}\sum_{i=0}^{n/2}\:\frac{g(X_{i})+g(Y_{i})}{2}$
	- Questions:
		1. Why and when does this lead to a better estimator for µ? 
		2. How can one construct CIs for µ based on µˆ AV n ? 
		3. How can one construct negatively correlated pairs (Xi , X˜ i)?
	- Key Concept:
		1. Antithetic variates work by creating negatively correlated pairs 
		2. Not all functions benefit equally from this technique 
		3. Careful analysis is needed to determine applicability
		4. Generating Antithetic Pairs 
			- Most effective when using inversion method 
			- Works well when: 
				1. Function g is ***continuous*** and ***monotone*** 
				2. Sampling from uniform distribution U(0,1) 
			- For $U \sim U(0,1)$, can use $(U, 1-U)$, more generally, can use $(F^{-1}(U), F^{-1}(1-U))$
	- Variance Characteristics 
		- Variance depends on correlation between g(X) and g(Ỹ) 
		- Best when pairs are negatively correlated
	- Zero Variance Case
		- Occurs for linear functions $g(u) = a + bu$
	- Confidence Interval:
		- Estimated mean $(\hat{\mu}_{n}^{AV})$
		- Estimated standard deviation 
		- Typically narrower than crude MC confidence intervals
	- ***Proposition 1***: 
		- $Let\:\sigma^{2}=Var(g(X)).\:The\:variance\:of\:the\:AV\:estimator\:\hat{\mu}_{n}^{AV}is\:given\:by$$Var\left( \hat{\mu}_{n}^{AV} \right)=\frac{\sigma^{2}}{n}+\frac{1}{n}Cov(g(X),g(\tilde{X}))$ $Hence,\:Var(\hat{\mu}_{n}^{AV}\leq Var(\hat{\mu}_{n}^{MC}))\iff Cor(g(X),g(\tilde{X})))\leq0$
2. **(CV) Control Variates**
	- *Basic Concept* 
		- Use a related random variable C with known expected value 
		- Adjust Monte Carlo estimator to reduce variance
	- *Control Variate Estimator* : 
		- $\hat{\mu}_{n}^{CV}=\frac{1}{n}\sum_{i=1}^{n}(Y_{i}+\beta(\mu_{c}-Ci))$ 
		- β chosen to minimize variance (for any fixed b, CV is unbiased)
	- *Methods to estimate $\beta$*:
		- optimal constant $\beta^{*}=\frac{Cov(Y,C)}{Var(C)}$ minimizes the estimator's variance
		- The corresponding estimator $\hat{\mu}_{n}^{CV,opt}=(1-p^{2})Var(\hat{\mu}_{n}^{MC})\:<\:\hat{\mu}_{n}^{MC}$ 
3. **Stratified sampling**
	- ***Basic Concept:***
		- Divide the domain $\Omega$ into M non-overlapping strata $(S_{1},S_{2},\dots,S_{M})$
		- Perform *MC estimation* separately in each stratum
	- ***Stratified estimator:
		- $\hat{\mu}_{n}^{SS} =\sum_{j=1}^{m}p_{j}\hat{\mu}_{j}$
		- $\hat{\mu}_{j} =\frac{1}{N_{j}}\sum_{i=1}^{N_{j}}g(X_{i,j}) ,\:the^{ \: }MC\:estimator\:for\:stratum\:j$
		- $\mathbb{E}\left( \hat{\mu}_{n}^{SS}\right)= \mathbb{E}\left( \sum_{j=1}^{M}p_{j}\hat{\mu}_{j} \right)=\sum_{j=1}^{M}p_{j}\mu_{j}=\mu\implies \hat{\mu}_{n}^{SS}\:is\:unbiased\:for\:\mu$ 
		- $Var(\hat{\mu}_{n}^{SS})=\sum_{j=1}^{M}\frac{p_{j}^{2}}{N_{j}}\sigma_{j}^{2}$
	- ***Allocation Strategies*** 
		1. **Proportional Allocation** $\hat{\mu}^{SS,\:prop},\:N_{j}=np_{j}\:for\:j=1,\dots,M$
			- Allocate samples proportional to stratum probabilities 
			- Simple to implement 
			- Guaranteed variance reduction, $Var(\hat{\mu}_{n}^{SS,opt})$
		2. **Optimal Allocation** 
			- Choose $N_{1},\dots,N_{M}$ such that $Var(\hat{\mu}_{n}^{SS})=\sum_{j=1}^{M}\frac{p_{j}^{2}}{N_{j}}\sigma_{j}^{2}$
			- Minimize variance by allocating samples based on stratum variability 
			- Requires pilot study to estimate stratum variances 
			- More complex but potentially more efficient
		- $Var(\hat{\mu}^{SS,\:opt})\leq\:Var(\hat{\mu}^{SS,\:prop})$
