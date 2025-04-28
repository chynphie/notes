- **Theorem 29**
	- Let $n$ be a positive number. An element $[a] \in \mathbb{Z}_n$ is a unit if and only if $\gcd(a, n) = 1$.
	- **Proof.**
	If $\gcd(a, n) = 1$ there exist $x, y \in \mathbb{Z}$ so that $ax + ny = 1$, so $ax \equiv 1 \mod n$.  Therefore there exists $x \in \mathbb{Z}$ so that $[a][x] = [1]$ in $\mathbb{Z}_n$ and $[a] \in \mathbb{Z}_n^*$.  Conversely, suppose $[a][x] = [1]$ in $\mathbb{Z}_n$ for some $x \in \mathbb{Z}$.  Then $ax = 1 + ny$ for some $y \in \mathbb{Z}$, which rearranges to $ax - ny = 1$.  Therefore $\gcd(a, n) = 1$, completing the proof.
- **Corollary 30**
	- Let $p$ be a prime. Then $[x] \in \mathbb{Z}_p^*$ if and only if $[x] \ne [0]$.
- **Theorem 31** *(Euler’s Theorem)*  
	- Let $n$ be a positive integer, and let $[a] \in \mathbb{Z}_n^*$. Then $[a]^{\varphi(n)} = [1]$ in $\mathbb{Z}_n$.
- **Lemma 32**  
	- Let $[a] \in \mathbb{Z}_n^*$. Then the function $\psi : \mathbb{Z}_n^* \to \mathbb{Z}_n^*$ given by $\psi([b]) = [a][b]$ is a bijection.
	- **Proof.**  
	Note that since the product of two units is a unit, $\psi$ is well-defined (i.e. $\psi([b]) \in \mathbb{Z}_n^*$ for every $[b] \in \mathbb{Z}_n^*$).
	For injectivity, suppose $\psi([b]) = \psi([c])$, so $[a][b] = [a][c]$.  
	Then since $[a]$ is a unit, multiplying both sides by $[a]^{-1}$ gives $[b] = [c]$, so $\psi$ is injective.
	For surjectivity, let $[c] \in \mathbb{Z}_n^*$.  
	Since $[a]^{-1}$ and $[c]$ are units, so is $[a]^{-1}[c]$.  
	Then $\psi([a]^{-1}[c]) = [a][a]^{-1}[c] = [c]$, so $\psi$ is surjective, and thus a bijection. ■
- **Corollary 33** *(Fermat’s Little Theorem)*  
	- Let $p$ be a prime and suppose $a \in \mathbb{Z}$ with $p \nmid a$. Then  $a^{p-1} \equiv 1 \mod p$.
-  **Proposition 34**  
	- Let $p$ be a prime and $e$ a positive integer. Then $\varphi(p^e) = p^e - p^{e-1}$.*
	**Proof.**  
	The number of integers in $\{0, \ldots, p^e - 1\}$ coprime to $p^e$ is exactly the number not divisible by $p$.  
	There are $p^{e-1}$ multiples of $p$ in $\{0, \ldots, p^e - 1\}$, so  
	$\varphi(p^e) = p^e - p^{e-1}$. ■
- **Lemma 35**  
	- Let $a, m, n \in \mathbb{Z}$. We have $\gcd(a, m) = 1$ and $\gcd(a, n) = 1$ if and only if $\gcd(a, mn) = 1$.
-  **Lemma 36**  
	- Let $m$ and $n$ be coprime positive integers. Let $c \in \mathbb{Z}$. Then the function $f : \mathbb{Z}_n \to \mathbb{Z}_{mn}$ given by $f([a]) = [a][m] + [c]$ is a bijection.*
- **Proposition 37**  
	- Let $m$ and $n$ be positive coprime integers. Then  $\varphi(mn) = \varphi(m)\varphi(n)$.
- **Theorem 38**  
	- Suppose a positive integer has prime factorisation $n = p_1^{e_1} \cdots p_k^{e_k}$ where the $p_i$ are distinct prime factors and $e_i > 0$ for all $i$. Then $\varphi(n) = \prod_{i=1}^{k} (p_i^{e_i} - p_i^{e_i - 1}) = \prod_{i=1}^{k} p_i^{e_i - 1}(p_i - 1) = n \prod_{i=1}^{k} \left(1 - \frac{1}{p_i}\right).$
- **Lemma 39**  
	- Let $n$ be a positive integer and $d$ a positive divisor of $n$. Let*  $S_d = \left\{ a \in \{0, \ldots, n-1\} : \gcd(a, n) = \frac{n}{d} \right\}.$  Then $|S_d| = \varphi(d)$.*
- **Theorem 40**  
	- Let $n$ be a positive integer. Then  $\sum_{d \mid n} \varphi(d) = n$  *where $\sum_{d \mid n}$ denotes the sum over all positive divisors $d$ of $n$.
<div style="page-break-after: always;"></div>
