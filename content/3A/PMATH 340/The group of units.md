- ***Proposition 49:***
	- For all elements $a, b \in \mathbb{F}$, if $ab = 0$ then $a = 0$ or $b = 0$.
- ***Proposition 50:***
	- Let $f, g \in \mathbb{F}[x]$ with $f \neq 0$ and $g \neq 0$. Then $\deg(fg) = \deg(f) + \deg(g)$.
- ***Theorem 51 (Division algorithm for polynomials):***
	- Let $f, g \in \mathbb{F}[x]$ with $g \neq 0$. Then there exist unique polynomials $q, r \in \mathbb{F}[x]$ so that $f = qg + r$, where $\deg(r) < \deg(g)$ or $r = 0$.
	- **Note**:
		- If $f(x) = x^p \in \mathbb{Z}_p[x]$ we have $f([a]) = 0$, $[a] \neq [0]$, so Fermat's little theorem tells us that $f([a]) = a^p = a$.
		- That means if $f([a]) = a^p$ and $g([a]) = [a]$, they define the same function.
- ***Proposition 52.***
	- Let $f(x) \in \mathbb{F}[x]$ and $c \in \mathbb{F}$. Then $f(c) = 0$ if and only if $(x - c) \mid f(x)$.
- ***Theorem 53.*** 
	- Let $f(x) \in \mathbb{F}[x]$ be such that $f(x)$ is not the zero polynomial. Then $f(x)$ has at most $\deg(f(x))$ roots.
- ***Lemma 54.*** 
	- Let $[a] \in \mathbb{Z}_n^*$ and suppose $\operatorname{ord}([a]) = t$. Then $\operatorname{ord}([a]^k) = t$ if and only if $\gcd(k,t) = 1$
- ***Theorem 55.*** 
	- Let $p$ be a prime. Then $\mathbb{Z}_p^*$ has $\varphi(d)$ elements of order $d$ for every positive divisor $d$ of $p - 1$.
- ***Corollary 56.*** 
	- Let $p$ be a prime. There exists a generator of $\mathbb{Z}_p^*$.
- ***Proposition 57.*** 
	- Let $p$ be an odd prime. The polynomial $x^2 + [1] \in \mathbb{Z}_p[x]$ has a root if and only if $p \equiv 1 \pmod{4}$.
- ***Proposition 58.*** 
	- There are infinitely many primes $p$ such that $p \equiv 1 \pmod{4}$.
- **Generator** iff $ord[a]=\phi(n)$
- find generator for $Z_n^*$:
	1) compute $\phi(n) = x$ since a generator of $Z_n^*$ is an element $[a]$ order a = $\phi(n)$ 
	2) Compute $\phi(x) = y$ which is the number of generator in n, $y=p_i^{e_i}$
	3) verify by using $[a]^{\phi(n)/p_i} \neq [1]$ if all condition holds then [a] is one!
