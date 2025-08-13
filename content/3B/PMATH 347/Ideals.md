> [!proposition]  
> Let $\varphi : R \to S$ be a homomorphism, where $S \ne {0}$.  
> (a) $\operatorname{Im} \varphi$ is a subring of $S$.  
> (b) $\ker \varphi$ is an ideal of $R$.
> 
> Starting point: what’s special about kernels?

> [!lemma]  
> If $\varphi : R \to S$ is a homomorphism, and $m \in \ker \varphi$, then $rm$ and $mr$ are in $\ker \varphi$ for all $r \in R$.

**Proof.**  
$\varphi(rm) = \varphi(r)\varphi(m) = \varphi(r) \cdot 0_S = 0 = \varphi(mr)$.

> [!definition] Ideal  
> An **ideal** of a ring $R$ is a subgroup $I$ of $(R, +)$ such that if $m \in I$, $r \in R$, then $rm, mr \in I$.

> The lemma shows that the kernel of a homomorphism is an ideal.  
> If $R$ is commutative, we only need to check that $rm \in I$ for all $m \in I$, $r \in R$.

Example $m\mathbb{Z}$  
> [!lemma]  
> $m\mathbb{Z}$ is an ideal of $\mathbb{Z}$ for every $m \in \mathbb{Z}$.

**Proof.**  
Already know that $m\mathbb{Z}$ is a subgroup of $(\mathbb{Z}, +)$.  
If $r \in \mathbb{Z}$, and $km \in m\mathbb{Z}$, then $rkm \in m\mathbb{Z}$.  
So $m\mathbb{Z}$ is an ideal.

Intuition: if $m \mid x$, then $m \mid rx$ for all $r \in \mathbb{Z}$.  
Special case: when $m = 0$, $m\mathbb{Z} = {0}$.

Exercise
${0_R}$ is an ideal of any ring $R$, called the **trivial ideal**, and often denoted by $(0)$.

### Simplifying Conditions

To show that $I$ is a subgroup of $(R, +)$, need to check:  
- (a) $I$ contains 0,  
- (b) $I$ is closed under addition, and  
- (c) $I$ is closed under negation (additive inverses).

You can speed this up by checking:  
- (a') $I$ is non-empty, and  
- (b') $f, g \in I \Rightarrow f - g \in I$.

> [!lemma]  
> Let $R$ be a ring and $I \subseteq R$. Then $I$ is an ideal if and only if:  
> (a) $I$ is non-empty  
> (b) If $r \in R$, $f, g \in I$, then $rf + g, fr + g \in I$.

**Proof.**  
If $f, g \in I$, then $(-1) \cdot g + f = f - g \in I$, so (a'), (b') are satisfied.  
Since $I$ is a subgroup of $(R, +)$, $0 \in I$.  
If $m \in I$, $r \in R$, then $rm = rm + 0 \in I$.  
So $I$ is an ideal.

> [!example] Evaluation Map Let $R$ be a commutative ring, and pick $c \in R$.  
> The kernel of $\operatorname{ev}_c : R[x] \to R$ is $I = {f \in R[x] : f(c) = 0}$.

Let’s double check the ideal conditions:

- $0 \in I$, so $I$ is non-empty.
    
- If $f, g \in I$ and $r \in R[x]$, then  
      
    So $rf + g \in I$.
    

> [!example] Evaluation at $c = 0$ Suppose $f(x) = \sum_{i=0}^n a_i x^i$. Then $f(0) = a_0$, so  
> $f(0) = 0 \Leftrightarrow a_0 = 0$.

So elements of $I = \ker \operatorname{ev}_0$ look like $a_1x + a_2x^2 + \dots$. Because $a_1x + a_2x^2 + \dots = x(a_1 + a_2x + \dots)$,  
we sometimes denote $I$ by $xR[x]$, or by $(x)$.

Intuition: if $f(x)$ has no constant term, then multiplying $f(x)$ by another polynomial can’t add in a constant term.

> [!lemma] 
> If $f(x) \in R[x]$ has degree $\le n$, and $c \in R$, then there are $a_0, \dots, a_n \in R$ such that  
> where $(x - c)^0 := 1$.

**Proof.**  
Clearly true if $n = 0$. Use induction on $n$.  
General case: if coefficient of $x^n$ in $f(x)$ is $a_n$, then $f(x)-a_{n}(x-c)^{n}=a_{n}x^{n}+\:$ lower terms - $(a_{n}x^{n}$ + lower terms) is a polynomial of degree $\le n - 1$.  
By induction,  $f(x)-a_{n}(x-c)^{n}=\sum_{i=0}^{n-1}a_{i}(x-c)^{i}$ 

> [!lemma] 
> If $f(x) \in R[x]$ has degree $\le n$, and $c \in R$, then there are $a_0, \dots, a_n \in R$ such that  
> and $\ker \operatorname{ev}_c = (x - c)R[x] = (x - c)$.

Because evaluation is a homomorphism,  
So if $f(x) = \sum a_i(x - c)^i$, then $f(c) = a_0$. Hence, $\ker \operatorname{ev}_c = (x - c)R[x] = (x - c)$.

**Caution:** $2x = 2(x - 2) \in (\mathbb{Z}/4)[x]$, so $2x \in \ker \operatorname{ev}_2$.

> [!lemma] 
> If $I$ is an ideal of a ring $R$ and $1 \in I$, then $I = R$.

**Proof.**  
If $r \in R$ and $1 \in I$, then $r = r \cdot 1 \in I$.  

So any ideal containing $1$ must be the whole ring $R$.
We typically want to look at **proper ideals**, i.e., ideals $I$ such that $I \subsetneq R$.