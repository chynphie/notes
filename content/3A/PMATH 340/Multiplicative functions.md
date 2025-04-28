- ***Theorem 43.*** 
	- The divisor functions τ and σ are multiplicative
- ***Theorem 44 (Mobius inversion formula):***
	- Let $f: Z_{>0} \to C$ be an arbitrary $g(n)=\sum_{d|n} f(d)$ for all $n\in Z_{>0}$ Then
$$
	f(n)=\sum_{d|n} \mu(d)g(\frac n d)
$$
- Applications:
	1. Euler's Totient function: $\sum_{d|n} \phi(d)=n$ =>= $\phi(n)=n\sum_{d|n} \frac{\phi(d)}{d}$
	2. Dirichlet Inverse of $\sigma_k(n)$: $\sigma_k(n)=\sum_{d|n}d^k$ => $n^k=\sum_{d|n}\sigma_k(n/d)$ 
- An **arithmetic function** is a function $f : Z_{>0} \to C.$ 
- A **multiplicative function** is an arithmetic function f satisfying $f (nm) = f (n)f (m)$ whenever $gcd(n, m) = 1$ i.e. n,m are coprime
- ***divisor functions:***
	a) $\tau (n)=\sum_{d|n}1=\prod_{i=0}^{k}\tau(p_{i}^{e_i})$  (number of divisors)
	b) $\sigma(n)=\sum_{d|n}d=\prod_{i=0}^{k}\sigma(p_{i}^{e_i})$ (sum of divisors)
- $\sigma_k(n)$
	- $\sigma_0(n)$  counts the number of divisors of n
	- $\sigma_1(n)$  sums up the divisors of n
- **Unit function**: The multiplicative functions $u(n) = 1$ and $N (n) = n$ for all $n ∈ Z_{>0}$ 
- **Mobius function** $μ : Z>0 → C$ as the multiplicative function such that $\mu(p^{e})=$
	a) -1 if $e=1$
	b) 0 otherwise
- **identity function** $I(n)=\sum_{d|n}\mu(d)$    