## Review: Quotient Groups

Recall that in group theory:
- Kernels of homomorphisms are normal subgroups, and  
- Normal subgroups are kernels of homomorphisms,  
  since if $N \trianglelefteq G$, the quotient map $G \to G/N$ has kernel $N$.

Suppose $G$ is an abelian group using additive notation. Then:
- Elements of $G/N$ are equivalence classes $[x] = x + N$ for $x \in G$.
- $[x] = [y]$ if and only if $x - y \in N$.
- Group operation is $[x] + [y] = [x + y]$.
- Quotient map $G \to G/N$ sends $x \in G$ to $[x]$.

---

## Are ideals always the kernel of some homomorphism?

In ring theory:
- Kernels of homomorphisms are ideals.  
- Is it true that **ideals are kernels** of homomorphisms?

If $I$ is an ideal of $R$, is there a “quotient ring” $R/I$?

Since $(R, +)$ is commutative and $I \trianglelefteq R$, the quotient group $R/I$ exists.  
Why not try to put a ring structure on $R/I$?

We want a multiplication operation $\cdot$ such that the quotient map  
$q : R \to R/I$ is a ring homomorphism.  
This would require:
$$
[xy] = q(xy) = q(x)q(y) = [x] \cdot [y]
$$

---

> [!theorem] Quotient Ring Construction  
> Let $I$ be an ideal of a ring $R$, and define operations $+$ and $\cdot$ on $R/I$ by:  
> - $[x] + [y] = [x + y]$  
> - $[x] \cdot [y] = [xy]$ for $x, y \in R$  
> Then $(R/I, +, \cdot)$ is a ring, and the quotient map $q : R \to R/I : x \mapsto [x]$ is a surjective ring homomorphism with $\ker q = I$.  
> $R/I$ is called the **quotient of $R$ by the ideal $I$**, or simply a **quotient ring**.

> [!corollary]  
> Every ideal is the kernel of some homomorphism.

> [!example]  
> $\mathbb{Z}/m\mathbb{Z}$ is a ring with operations:  
> - $[x] + [y] = [x + y]$  
> - $[x] \cdot [y] = [xy]$  
> We can use this as the **definition** of $\mathbb{Z}/m\mathbb{Z}$.

---

## Proof of the Theorem

We already know that $(R/I, +)$ is an abelian group.

### Well-definedness of $\cdot$:
Suppose $[x] = [x']$ and $[y] = [y']$ for $x, x', y, y' \in R$.  
We want to show that $[xy] = [x'y']$, i.e., $xy - x'y' \in I$.

Note:
$$
xy - x'y' = xy - x'y + x'y - x'y' = (x - x')y + x'(y - y')
$$

Since $x - x', y - y' \in I$, and $I$ is an ideal:
- $(x - x')y \in I$
- $x'(y - y') \in I$

Thus, $xy - x'y' \in I$, and $[x][y] = [xy]$ is a well-defined operation.

### Associativity:
If $x, y, z \in R$:
$$
[x] \cdot ([y] \cdot [z]) = [x] \cdot [yz] = [x(yz)] = [(xy)z] = [xy] \cdot [z] = ([x] \cdot [y]) \cdot [z]
$$

### Identity:
$$
[1] \cdot [x] = [1 \cdot x] = [x] = [x] \cdot [1]
$$
So $[1]$ is the identity for multiplication in $R/I$.

### Distributivity:
Let $x, y, z \in R$.

Left distributivity:
$$
[x] \cdot ([y] + [z]) = [x] \cdot [y + z] = [x(y + z)] = [xy + xz] = [xy] + [xz] = [x][y] + [x][z]
$$

Right distributivity:
$$
([y] + [z]) \cdot [x] = [y] \cdot [x] + [z] \cdot [x]
$$

---

## Conclusion:

- $(R/I, +)$ is an abelian group.  
- $\cdot$ is associative, has identity $[1]$, and is distributive over $+$.

Therefore, $(R/I, +, \cdot)$ is a **ring**.

> [!note]  
> $q(xy) = [xy] = [x][y] = q(x)q(y)$, and $q(1) = [1]$ is identity in $R/I$.  
> So $q$ is a **ring homomorphism**.
