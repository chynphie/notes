#### Motivation: Examples
- Examples of familiar sets with addition and multiplication:
	- $\mathbb{Z}$
	- $\mathbb{Q}$
	- $\mathbb{R}$
	- Functions $\mathbb{R} \to \mathbb{R}$
	- Polynomials over $\mathbb{R}$
	- $\mathbb{C}$
	- $M_n(\mathbb{R})$, $M_n(\mathbb{C})$
	- $\mathbb{Z}/n\mathbb{Z}$

- All of these support two operations: addition $+$ and multiplication $\cdot$.
- Rings are an abstract structure that generalizes what these sets have in common.

> [!definition] Ring
> A **ring** is an ordered triple $(R, +, \cdot)$ where:
> - $R$ is a non-empty set;
> - $+$ and $\cdot$ are binary operations on $R$;
>
> which jointly satisfy the following conditions:
> 1. $(R, +)$ is an abelian group;
> 2. $\cdot$ is associative;
> 3. There exists $1 \in R$ such that $1 \cdot a = a \cdot 1 = a$ for all $a \in R$;
> 4. (**Distributive laws**): for all $a, b, c \in R$,
>    - $(a + b) \cdot c = (a \cdot c) + (b \cdot c)$  
>    - $a \cdot (b + c) = (a \cdot b) + (a \cdot c)$

- If $\cdot$ is commutative, i.e., $a \cdot b = b \cdot a$ for all $a, b \in R$, then $R$ is called a *commutative ring*.
#### Examples of Rings
- $\mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}$ are all commutative rings.
- $(\mathbb{N}, +, \cdot)$ is **not** a ring (since $\mathbb{N}$ is not a group under $+$).
- $\mathbb{Z}/n\mathbb{Z}$ is a commutative ring.
- If $R$ is a ring and $X$ is a set, then $\text{Fun}(X, R)$ (functions from $X$ to $R$) is a ring with pointwise operations.
- If $R$ is a (commutative) ring, then $R[x]$ (polynomials over $R$) is a ring.
- $M_n(R)$: $n \times n$ matrices over $R$ form a ring.
- Let $\circ: M_n(\mathbb{C}) \times M_n(\mathbb{C}) \to M_n(\mathbb{C})$ given by:
  $$(A, B) \mapsto \frac{AB + BA}{2}$$  
  Then $(M_n(\mathbb{C}), +, \circ)$ is **not** a ring (since $\circ$ is not associative).

#### Notation

- We usually denote $(R, +, \cdot)$ simply by $R$.
- Addition uses standard notation: $+$, inverse is $-x$, identity is $0$.
- Multiplication is often just written as juxtaposition: $ab$.
- Alternative multiplication symbols include: $\cdot, \times, \otimes, *$, etc.


#### Basic Properties

> [!proposition]
> If $R$ is a ring, then for all $a, b \in R$:
> 1. $0 \cdot a = a \cdot 0 = 0$
> 2. $(-a) \cdot b = a \cdot (-b) = -(a \cdot b)$
> 3. $(-a) \cdot (-b) = a \cdot b$

**Proofs:**

1.  $0 \cdot a = (0 + 0) \cdot a = 0 \cdot a + 0 \cdot a \Rightarrow 0 \cdot a = 0$  Similarly, $a \cdot 0 = 0$.
2. $0 = 0 \cdot b = (a + (-a)) \cdot b = a \cdot b + (-a) \cdot b \Rightarrow (-a) \cdot b = - (a \cdot b)$
3. $(-a)(-b) = -[a(-b)] = -[-(ab)] = ab$


#### Multiplicative Identity

> [!definition] Ring with identity
> A *ring with identity* is a ring $(R, +, \cdot)$ where $\cdot$ has a multiplicative identity $1$, i.e.:
> $$1 \cdot x = x \cdot 1 = x \quad \text{for all } x \in R$$

> [!note]
> The identity is **unique** if it exists.

In this course, *ring* means *ring with identity* unless stated otherwise.
#### Terminology
- A ring *without* identity is sometimes called a **rng** (a "ring" without an "i").
- All previously mentioned examples are rings *with* identity.
- For rings like $\text{Fun}(X, R)$, $R[x]$, or $M_n(R)$, we assume $R$ has an identity.

#### Additional Property

> [!proposition]
> If $R$ is a ring with identity, then for any $a \in R$:
> $$-a = (-1) \cdot a$$

**Proof:**  
- $0 = 0 \cdot a = (1 + (-1)) \cdot a$
- $= 1 \cdot a + (-1) \cdot a = a + (-1) \cdot a \Rightarrow (-1) \cdot a = -a$
