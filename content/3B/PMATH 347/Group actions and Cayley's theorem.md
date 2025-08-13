### **Definitions and Concepts of Group Actions**
>[!definition]
**Let $G$ be a group.**  
A **left action** of $G$ on a set $X$ is a function $G \times X \to X$, written $(g, x) \mapsto g \cdot x$ such that:
> - $g(h \cdot x) = (gh) \cdot x$ for all $g, h \in G$, $x \in X$
> - $e \cdot x = x$ for all $x \in X$

**Examples:**
- All of the above: $S_n$, $D_n$, $GL_n(\mathbb{R})$
- Let $G$ be any group, $X$ any set: **Trivial action**: $g \cdot x = x$
- If $X$ is a set, then $S_{X} := \{f: X \to X \mid f \text{ bijective}\}$ acts on $X$ by $f \cdot x := f(x)$
- $D_n$ acts on $\mathbb{R}^2$ and on $V(P_n)=\{ v_{1},\dots,v_{n} \}$

>[!definition]
If $G$ acts on $X$, and $Y \subseteq X$, we say $Y$ is **invariant under the $G$-action** if $g \cdot y \in Y$ for all $g \in G$, $y \in Y$.

>[!lemma]
If $G$ acts on $X$ and $Y \subseteq X$ is invariant under the $G$-action, then $G$ acts on $Y$ via the action:
> - $G \times Y \to Y$
> - $(g, y) \mapsto g \cdot y$

**Example:**  
- $\mathbb{T}^n$ is a linear subset of the $GL_n(\mathbb{R})$ action on $\mathbb{R}^n$; $GL_n(\mathbb{R})$ acts transitively on $\{ \vec{0} \}$

>[!proposition]
If $G$ acts on $X$ and $Y$, then $G$ acts on $\text{Fun}(X, Y)$ via:
> - $G \times \text{Fun}(X, Y) \to \text{Fun}(X, Y)$  :$(g, f) \mapsto (x \mapsto g \cdot f(g^{-1} \cdot x))$

In many situations, we use the trivial action on $Y$, so the rule becomes:  $g \cdot f(x) = f(g^{-1} \cdot x)$
 
>[!definition]
Let $G$ be a group. A **right action** of $G$ on a set $X$ is a function $X \times G \to X$, written $(x, g) \mapsto x \cdot g$ such that:
> - $x \cdot (gh) = (x \cdot g) \cdot h$
> - $x \cdot e = x$ for all $x \in X$

**Example:**  
If $G$ acts on $X$ via a left action, and $Y$ is any set, then $G$ has a right action on $\text{Fun}(X, Y)$ via:  
$(f \cdot g)(x) = f(g \cdot x)$

>[!lemma]
If $X$ has a right action of $G$ on $X$, then $g \mapsto x \cdot g^{-1}$ is a left action of $G$ on $X$.

**Proof:**  
- $e \cdot x = x \cdot e = x$  
- $(gh) \cdot x = x \cdot (gh) = (x \cdot g) \cdot h$

>[!proposition]
If $G$ acts on a set $X$, then $G$ acts on $2^X$ by:  
$g \cdot S := \{g \cdot s \mid s \in S\}$

**Proof:**
- $(g \cdot h) \cdot S = \{gh \cdot s \mid s \in S\} = \{g \cdot (h \cdot s) \mid s \in S\} = g \cdot (h \cdot S)$

**Question:**  
How can we get a non-trivial action of a group $G$ on a set?

>[!proposition]
If $G$ is a group, then the group operation $G \times G \to G$ gives both:
> - a left action of $G$ on $G$
> - a right action of $G$ on $G$

These are called the **left regular** and **right regular** actions of $G$.

**Property:**  
If $H \leq G$, then $G$ acts on $G/H$ by:  
$g \cdot xH := gxH$ ■

>[!corollary]
If $H \leq G$, then $G$ acts on $G/H$ by:  
$g \cdot KH := gKH$

**Proof:**  
$G$ acts on $G$ via the left regular action, so $G$ acts on $2^G$ via:  
$g \cdot S := \{g \cdot s \mid s \in S\}$

If $S \in G/H \subseteq 2^G$, $g \in G$, then $g \cdot S \in G/H$.  
$(S = H \Rightarrow g \cdot S = gH)$ ⇒ So $G/H$ is an invariant subset of $2^G$, so $G$ acts on $G/H$.  
And this action satisfies $g(kH) = gkH$ ■
