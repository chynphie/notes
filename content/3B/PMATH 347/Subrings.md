#### Terminology: Unital vs Non-Unital Rings

> [!note]
> - *Rings with identity* are also called **unital rings**.
> - *Rings without identity* are called **non-unital rings**.
> - This distinction becomes especially useful when discussing subrings and homomorphisms.

> [!caution]
> The textbook uses terminology like:
> - **non-unital rings**
> - **non-unital subrings**
> - **non-unital homomorphisms**


#### Definition of Subring (Unital Version)

> [!definition] Subring
> Let $R$ be a ring. A subset $S \subseteq R$ is a *subring* if:
> 1. $S$ is a subgroup of $(R, +)$,
> 2. if $a, b \in S$, then $ab \in S$,
> 3. $1 \in S$.

> [!lemma] 
> If $S$ is a subring of $(R, +, \cdot)$, then $(S, +, \cdot)$ is itself a ring.

**Examples:**
- $\mathbb{Z} \subseteq \mathbb{Q} \subseteq \mathbb{R} \subseteq \mathbb{C} \subseteq \mathbb{H}$
- $R[x]$ is a subring of $\text{Fun}(R, R)$
- $M_n(\mathbb{Z})$ is a subring of $M_n(\mathbb{R})$


#### More Examples (and Non-Examples)

> [!examples]
> **Examples and Non-Examples:**
> - $\mathbb{Q}^\times$ is **not** a subring of $\mathbb{Q}$
> - $\text{span}\{1, x\}$ is **not** a subring of $\mathbb{R}[x]$ (not closed under multiplication)
> - $2\mathbb{Z}$ is **not** a subring of $\mathbb{Z}$ (does not contain $1$)
> - $\{0\}$ is **not** a subring of any non-trivial ring $R$


#### Alternative Definition: Non-Unital Subrings

> [!definition] (Non-Unital Version)
> Let $R$ be a *not-necessarily-unital* ring. A subset $S \subseteq R$ is a *subring* if:
> 1. $S$ is a subgroup of $(R, +)$,
> 2. if $a, b \in S$, then $ab \in S$.

> [!note]
> If $R$ is unital and $1 \in S$, then $S$ is a *unital subring*.  
> Sets satisfying only (1) and (2) are called **non-unital subrings**.

> [!important]
> In this course:
> - **"Ring"** means **unital ring**
> - **"Subring"** means **unital subring**


#### Example: Non-Unital Subring in $R[x]$

> [!example]
> Let $R = \mathbb{R}[x]$ (polynomials over $\mathbb{R}$). Define:
> $$
> x\mathbb{R}[x] = \{f \in \mathbb{R}[x] : \text{constant term of } f = 0\}
> $$

- Equivalent to: $f(0) = 0$
- Closed under subtraction: $f - g \in x\mathbb{R}[x]$
- Closed under multiplication: if $f, g \in x\mathbb{R}[x]$, then $(fg)(0) = f(0)g(0) = 0$
- $1 \notin x\mathbb{R}[x]$ ⟹ this is a **non-unital subring**

> [!exercise]
> Show that $(x\mathbb{R}[x], +, \cdot)$ is a non-unital ring.


#### Example: Compactly Supported Functions

> [!example]
> Let $R = \text{Fun}(\mathbb{R}, \mathbb{R})$. A function $f : \mathbb{R} \to \mathbb{R}$ is **compactly supported** if:
> $$
> \exists [a, b] \subseteq \mathbb{R} \text{ such that } f(x) = 0 \text{ for all } x \notin [a, b]
> $$

Let $S = \{$compactly supported functions$\}$
- If $f, g$ are compactly supported, so are $f - g$ and $fg$
- Identity in $\text{Fun}(\mathbb{R}, \mathbb{R})$ is the constant function $1$, which is not compactly supported
- $\Rightarrow$ compactly supported functions form a **non-unital subring**


#### Why It's Not a Ring

> [!claim]
> The compactly supported functions form a **non-unital ring**.

**Proof:**  
Suppose $f$ is an identity. Then $\exists [a, b]$ such that $f(x) = 0$ for $x \notin [a, b]$.

Let $g$ be compactly supported with $g(x) \ne 0$ for some $x \notin [a, b]$. Then:
$$
(fg)(x) = f(x)g(x) = 0 \ne g(x) \Rightarrow f \ne 1
$$

So no compactly supported function can be a multiplicative identity.
