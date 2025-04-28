- **Definition** 
	- A technique for estimating analytically intractable (but existing) expectations by simulation;
	- Generating large number of random samples to evaluate the outcome
	- For integrals that do not have closed forms.
	The expectation $\mu$ is defined as:$$\mu = \int_{\mathbb{R}} g(x) dF(x) = \mathbb{E}[g(X)]$$where $X \sim F$, and its Monte Carlo estimate is: $$\hat{\mu}_n^{MC} = \frac{1}{n} \sum_{i=1}^{n} g(X_i), \quad X_i \sim F$$use in estimating (rare event), probabilities or conditional. expectations
- **MC method estimates $\mu$ by**:
	- Since $\mu = \mathbb{E}(g(X))=\int_{\mathbb{R}^d} g(x)dF(x), X \sim F$ , then $\hat{\mu}_n^{MC} = \frac 1n \sum_{i=1}^n g(X_i)$, and $X_1,...,X_n$ are independent $\sim F$
	- Able to estimate quantiles that related to F, not just E(X) 
- **Properties of MC estimator**
	- $\mathbb{E}(\hat{\mu}_n^{MC})=\frac 1 n \sum_{i=1}^n\mathbb{E}(g(X_i)) = \mu$ 
	- If $\sigma^2 = Var(g(X)) \lt \infty$, then $Var(\hat{\mu}_n^{MC})=\frac{\sigma^2} n$ 
	- *Theorem 4.7(Central Limit Theorem)*: 
		- If $(Z_{n})_{n \in \mathbb{N}}$ is a sequence of independent rvs with cdf F, and if $\mu=\mathbb{E}(Z_{1}) \text{ and } \sigma^{2}=Var(Z_{1})<\infty$ then $$\sqrt{ n } \frac{{\frac{1}{n}\sum_{i=1}^{n}Z_{i}-\mu}}{\sigma} \to N(0,1)$$Shows **Asymptotic normality** and ROC, and MC converges to $\mu$ is $\frac {\sigma }{\sqrt(n)} = O(\frac{1}{\sqrt{ n }})$   
	- *SSLN Theorem*: 
		- states that $\mathbb{P}_{n\to \infty} (\hat{\mu}_{n}^{MC}=\mu)=1$ => strongly consistent
	- *Proposition 1 (Delta method)*:
		- if $h: \mathbb{R} \to \mathbb{R} \text{ is continuously differentiable with } h'(\mu) \neq 0 \text{ then }\sqrt{ n }{h\left( \frac{\hat{\mu}_n^{MC}-h(\mu)}{\sigma h'(\mu)} \right)}$
	- **Asymptotic Confidence Interval for** $\mu$ $$CI= \left[ \hat{\mu}_n^{MC} \pm Z_{\frac{1-\alpha}{2}} \frac{\sigma}{\sqrt{n}} \right]$$where $\sigma = s_n = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (g(X_i) - \hat{\mu}_n^{MC})^2}$
- **Integration** 
	- If $\mu = \int_a^b g(x) dx$, substitute $u = \frac{x-a}{b-a}$,  then $\mu = (b-a) \mathbb{E}[g(a + (b-a)U)]$ and its Monte Carlo estimate: $\hat{\mu}_n^{MC} =\frac{(b-a)}{n} \sum_{i=1}^{n} g(X_i)$
	- if $\mu=\int_{0}^{\infty}g(x)dx$, substitute $u=\frac{1}{1+x}$ then $\mu= \mathbb{E}\left( g\left( \frac{1}{U-1} \right){\frac{1}{U^{2}}} \right)$
	- If $\mu = \int_{-\infty}^{\infty} g(x) dx$, substitute $u = \frac{1}{1-x}$,  then $\mathbb{E}\left( \left( -g\left( -\frac{1}{1-U} \right)+g\left( \frac{{1-U}}{U} \right) \right){\frac{1}{U^{2}}} \right)$
- **Inversion**$$\mu = \int_{\mathbb{R}} g(x) dF(x) = \mathbb{E}[g(X)] = \mathbb{E}[g(F^{-1}(U))]$$where:$\mu = \int_0^1 g(F^{-1}(u)) du = \mathbb{E}[f(U)], \quad U \sim \prod$ (Independence copula)

### Monte Carlo Estimation of Probabilities
- If we are interested in estimating $\mu=\mathbb{P}(X \in A),A \subset \mathbb{R}^{d}$ , then
	1. $\mu=\mathbb{E}(g(X))=\mathbb{E}(\mathbb{1}_{\{X\in A\}})=1\cdot \mathbb{P}(X\in A)+0\implies\hat{\mu}_{n}^{MC}=\frac{1}{n}\sum_{i=1}^{n}\mathbb{1}_{\{X_{i}\in A\}}, X_{1},\dots,X_{n} \sim F$
	2. $\sigma^{2}=Var(g(X))=\mu(1-\mu)\implies Var(\hat{\mu}_{n}^{MC})=\frac{1}{n}\mu(1-\mu)$
-  *Example*: 
	Let $f(x) = \mathbb{1}_{\{X > 2\}}$. We estimate:$$\mu = P(X > 2)$$
	The cumulative distribution function:$F(x) = P(X \leq x) = \int_{-\infty}^{x} \frac{1}{\pi(1+x^{2})} dt = \lim_{ b \to -\infty }\left( \frac{1}{\pi}\arctan(x) \right)|^{x}_{b}$
	$$= \frac{1}{\pi} \arctan(x) + \frac{1}{2}$$Thus: $\mu = P(X > 2) = 1 - P(X \leq 2) = 1 - F(2) = \frac{1}{2} - \frac{\pi}{2} \arctan(2)$
	Variance of the Monte Carlo estimate:$$\text{Var}(\hat{\mu}_n^{MC}) = \frac{1}{n} \text{Var}(\mathbb{1}_{\{X_i > 2\}}) = \frac{\mu(1-\mu)}{n} \sim \text{Bin}(1,\mu)$$
-  Minimum sample size: $n\geq max\left\{  50,\left\lceil  \left( z_{1-{\alpha}/{2}}\frac{\sigma}{\epsilon} \right)^{2}  \right\rceil  \right\}$