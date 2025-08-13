
> [!definition] Unit
> Let $R$ be a ring. An element $x \in R$ is called a *unit* if $x$ has a multiplicative inverse, i.e., there exists $y \in R$ such that $xy = yx = 1$.
> The set of units in $R$ is denoted $R^\times$.

- If $x$ is a unit, the inverse is unique and denoted $x^{-1}$.
- $R^\times$ forms a group under multiplication — called the *group of units*.

**Examples:**
- $\mathbb{Z}^\times = \{\pm1\} \cong \mathbb{Z}/2\mathbb{Z}$
- $\mathbb{Q}^\times = \{x \in \mathbb{Q} : x \ne 0\}$

#### The Trivial Ring

- The smallest ring is $R = \{0\}$ with multiplication $0 \cdot 0 = 0$.  
- This ring has identity $1 = 0$.
- This is called the *trivial ring* or *zero ring*.

> [!lemma]
> Let $R$ be a ring. Then $1 = 0$ if and only if $R$ is trivial.

**Proof.**  
- If $1 = 0$, then for all $x \in R$:  $x = 1 \cdot x = 0 \cdot x = 0 \Rightarrow x = 0$
- Hence $R = \{0\}$.
#### Fields and Division Rings
- If $R$ is a ring with $1 \ne 0$, then for all $y \in R$:
  $$0 \cdot y = 0 \ne 1 \Rightarrow 0 \notin R^\times$$

> [!definition] Division Ring and Field
> A *division ring* is a ring $R$ with $1 \ne 0$ such that $R^\times = R \setminus \{0\}$.  
> A *field* is a commutative division ring.

Examples:
- $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$ are all fields.
- Reminder: For $\alpha = a + bi \in \mathbb{C}$,  $\alpha \bar{\alpha} = |\alpha|^2 = a^2 + b^2,\quad \text{and } \alpha^{-1} = \frac{\bar{\alpha}}{|\alpha|^2}$ if $\alpha \ne 0$.
#### Example: $\mathbb{Z}/n\mathbb{Z}$

- We usually consider $\mathbb{Z}/n\mathbb{Z}$ as a group under $+$.  
- But it also has multiplication:$$[x] \cdot [y] = [xy]$$making it a ring.

> [!lemma]
> $[x]$ is a unit in $\mathbb{Z}/n\mathbb{Z}$ if and only if $\gcd(x, n) = 1$.

**Proof.**  
If $\gcd(x, n) = 1$, then there exist $a, b \in \mathbb{Z}$ such that $ax + bn = 1$  
$\Rightarrow [ax] = 1$ in $\mathbb{Z}/n\mathbb{Z}$.

Conversely, if $[ax] = 1$, then $ax - 1 = bn$  
$\Rightarrow \gcd(x, n) = 1$.

> [!corollary]
> $\mathbb{Z}/n\mathbb{Z}$ is a field **if and only if** $n$ is prime.

> [!note]
> In particular, there exist finite fields.


#### Division Rings

> [!theorem] **Wedderburn’s Theorem.**  
> Any *finite* division ring is a *field*.

> [!definition] Ring of quaternions
> The *ring of quaternions* is the ring Q = $(\mathbb{R}^4, +, \cdot)$ where:
> 
> - Basis: $1, i, j, k$
> - Relations: $i^2 = j^2 = k^2 = -1$ and $ijk = -1$
> 
From this:
> - $ij = k$, $jk = i$ ⟹ $ji = -k$
> 
> So $\mathbb{H}$ is a non-commutative division ring.

