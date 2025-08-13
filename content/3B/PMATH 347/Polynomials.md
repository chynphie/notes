
Let $R$ be a ring.  
The ring of polynomials in variable $x$ with coefficients in $R$  
is the ring with elements $\sum_{i=0}^n a_i x^i$ for $n \geq 0$, and $a_0, \dots, a_n \in R$.  
Addition and multiplication are defined as usual, so  
$\left(\sum_{i=0}^n a_i x^i\right)\left(\sum_{j=0}^m b_j x^j\right) = \sum_{k=0}^{n+m} \left( \sum_{i=0}^k a_i b_{k-i} \right) x^k$  
where $a_i = b_j = 0$ for $i > n$, $j > m$.  
As usual, we can talk about degree, monomials, evaluation, etc.  
Question: how do we formalize all this?

---

> [!definition] Formal definition of polynomial rings  
> Given a ring $R$, let $R[x]$ be the set  
> $\{(a_i)_{i=0}^{\infty} \subseteq R : \text{there exists } N \geq 0 \text{ such that } a_i = 0 \text{ for } i \geq N\}$.  
> We define binary operations $+$ and $\cdot$ on $R[x]$ by  
> $(a_i)_{i=0}^{\infty} + (b_i)_{i=0}^{\infty} = (a_i + b_i)_{i=0}^{\infty}$ and  
> $(a_i)_{i=0}^{\infty} \cdot (b_i)_{i=0}^{\infty} = (c_k)_{k=0}^{\infty}$ where $c_k = \sum_{i=0}^k a_i b_{k-i}$.  
> The choice of variable matters only in that we let  
> $\sum_{i=0}^n a_i x^i$ denote $(a_0, \dots, a_n, 0, 0, \dots)$ (note: not a unique rep’n).  
> If we change the variable then we change this notation.

---

> [!lemma]  
> $(R[x], +, \cdot)$ is a ring.  
> **Proof.**  
> Need to show that $+$ and $\cdot$ are well-defined.  
> Let $N_1, N_2 \geq 0$ be such that $a_i = 0$ for $i \geq N_1$, $b_j = 0$ for $j \geq N_2$.  
> Then $a_i + b_i = 0$ for $i \geq \max(N_1, N_2)$, so $(a_i)_{i=0}^{\infty} + (b_i)_{i=0}^{\infty} \in R[x]$  
> If $k \geq N_1 + N_2$ and $0 \leq i < N_1$, then $k - i > N_2$.  
> So $\sum_{i=0}^k a_i b_{k-i} = 0$ if $k \geq N_1 + N_2 \Rightarrow (a_i)_{i=0}^{\infty} \cdot (b_i)_{i=0}^{\infty} \in R[x]$  
> **Exercise:** $(R[x], +)$ is an abelian group with $0 = (0, 0, \dots)$.  
> Next, want to show that $\cdot$ is associative.  
> Suppose that $(a_i)_{i=0}^{\infty}, (b_i)_{i=0}^{\infty}, (c_i)_{i=0}^{\infty} \in R[x]$.

---

> [!proof] Proof continued  
> Let $(a_i)_{i=0}^{\infty} \cdot ((b_j)_{i=0}^{\infty} \cdot (c_k)_{i=0}^{\infty}) = (d_n)_{n=0}^{\infty}$. Then  
> $d_n = \sum_{i=0}^n a_i \left( \sum_{j=0}^{n-i} b_j c_{n-i-j} \right) = \sum_{i+j+k=n} a_i b_j c_k = \sum_{\ell=0}^n \left( \sum_{i=0}^{\ell} a_i b_{\ell - i} \right) c_{n - \ell}$  
> From this, see that $(d_n)_{n=0}^{\infty} = ((a_i)_{i=0}^{\infty} \cdot (b_j)_{i=0}^{\infty}) \cdot (c_k)_{i=0}^{\infty}$  
> So $\cdot$ is associative.  
> **Exercise:** $1 = (1, 0, 0, \dots)$ is an identity for $\cdot$.  
> For distributivity, suppose $(a_i)_{i=0}^{\infty}, (b_i)_{i=0}^{\infty}, (c_i)_{i=0}^{\infty} \in R[x]$ again,  
> let $(d_n)_{n=0}^{\infty} = (a_i)_{i=0}^{\infty} \cdot ((b_i)_{i=0}^{\infty} + (c_i)_{i=0}^{\infty})$. Then  
> $d_n = \sum_{i=0}^n a_i \cdot (b_{n-i} + c_{n-i}) = \sum_{i=0}^n a_i b_{n-i} + \sum_{i=0}^n a_i c_{n-i}$  
> so $(d_n)_{n=0}^{\infty} = (a_i)_{i=0}^{\infty} \cdot (b_i)_{i=0}^{\infty} + (a_i)_{i=0}^{\infty} \cdot (c_i)_{i=0}^{\infty}$  
> Right distributivity similar. Conclusion: $R[x]$ is a ring.

---

> [!note] Terminology / notation for polynomial rings  
> - $R[x]$ is called the ring of polynomials in variable $x$ with coefficients in $R$.  
> - $x$ is referred to as the variable or indeterminate. Can use any variable we want, e.g. $R[x], R[y], R[\pi]$  
> - We only use $(a_i)_{i=0}^{\infty}$ to denote elements of $R[x]$ when we are defining or proving something formally.  
> - Use $\sum_{i=0}^n a_i x^i$ when working with $R[x]$. If we don’t want to specify coefficients, denote elements of $R[x]$ by $p$ or $p(x)$.  
> - **Exercise:** there is an isomorphism $R[x] \cong R[y]$ : $p(x) \mapsto p(y)$  
>   (this works with $x$ and $y$ replaced by any pair of variables).

---

> [!definition] Degree and coefficients  
> The degree of $p(x) \in R[x]$ is the smallest integer $n$ such that  
> $p(x) = \sum_{i=0}^n a_i x^i$ with $a_n \ne 0$, or $-\infty$ if no such $n$ exists.  
> The degree is denoted by $\deg(p)$.  
> Examples: $\deg(1) = 0$, $\deg(1 + x - x^3) = 3$, $\deg(0) = -\infty$.

---

> [!definition]  
> The coefficient of $x^i$ in $(a_i)_{i=0}^{\infty} \in R[x]$ is $a_i$.  
> A monomial is a polynomial of the form $x^i$ for some $i \geq 0$,  
> and a polynomial of the form $a_i x^i$ is called a term.  
> If $p(x) = \sum_{i=0}^n a_i x^i$ is a polynomial of degree $n$, then the  
> polynomials $a_i x^i$, $i = 0, \dots, n$ are called the terms of $p(x)$.  
> $a_n x^n$ is the leading term, and $a_n$ is the leading coefficient.

---

> [!note] Constant polynomials  
> Polynomials of degree $\leq 0$ are called constant polynomials.  
> There is a constant polynomial $a x^0 \in R[x]$ for every $a \in R$.  
> Usually just denote this polynomial by $a$.

---

> [!lemma]  
> Let $R$ be a ring. The set of constant polynomials in $R[x]$ is a  
> subring, and is isomorphic to $R$.  
> Because of this isomorphism, we think of $R$ as a subring of $R[x]$.

---

> [!lemma] Commutativity  
> If $R$ is commutative, then $R[x]$ is commutative.  
> **Proof.**  
> $\left(\sum_{i=0}^n a_i x^i\right) \cdot \left(\sum_{j=0}^m b_j x^j\right) = \sum_{i=0}^n \sum_{j=0}^m a_i b_j x^{i+j}$  
> $= \sum_{j=0}^m \sum_{i=0}^n b_j a_i x^{i+j} = \left(\sum_{j=0}^m b_j x^j\right) \cdot \left(\sum_{i=0}^n a_i x^i\right)$  
> $R[x]$ makes sense even if $R$ is not commutative, but note that  
> $x \in Z(R[x])$, so it’s not the most natural.
