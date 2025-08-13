> [!definition] Ring Homomorphism  
> Let $R$ and $S$ be rings. A function $\varphi : R \to S$ is a (unital) **homomorphism** if:  
> 1. $\varphi : (R, +) \to (S, +)$ is a group homomorphism,  
> 2. $\varphi(ab) = \varphi(a)\varphi(b)$ for all $a, b \in R$, and  
> 3. $\varphi(1_R) = 1_S$.  
>  
> If (1) and (2) are satisfied, but (3) is not, then $\varphi$ is a **non-unital homomorphism**.

**Standard warning:**  
In this class, homomorphism = unital homomorphism.  
Textbook uses non-unital homomorphisms by default.

> [!example] Examples of Homomorphisms  
> - If $S$ is a subring of $R$, then $i : S \to R : x \mapsto x$ is a homomorphism.  
> - The quotient maps $\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z} : x \mapsto [x]$ and  
>   $\mathbb{Z}/mn\mathbb{Z} \to (\mathbb{Z}/mn\mathbb{Z})/(m\mathbb{Z}/mn\mathbb{Z}) \cong \mathbb{Z}/m\mathbb{Z} : [x] \mapsto [x]$  
>   are homomorphisms since $[xy] = [x] \cdot [y]$.


> [!definition] Ring Isomorphism  
> A homomorphism $\varphi : R \to S$ is an **isomorphism** if $\varphi$ is bijective.

> [!proposition]  
> Let $R_0 = \mathbb{Z} \cdot 1_R$ be the prime subring of a ring $R$, and let $n = \text{char}(R)$.  
> Then $\varphi : \mathbb{Z}/n\mathbb{Z} \to R_0 : [x] \mapsto x \cdot 1$ is a ring isomorphism.

> [!proof]  
> We already showed that $\varphi$ is a well-defined group isomorphism, so $\varphi$ is bijective.  
> If $[a], [b] \in \mathbb{Z}/n\mathbb{Z}$, then  
> $\varphi([a] \cdot [b]) = \varphi([ab]) = ab \cdot 1 = a(1 \cdot b) = (a \cdot 1)(b \cdot 1) = \varphi([a]) \cdot \varphi([b])$  
> and since $\varphi([1]) = 1$, $\varphi$ is a homomorphism.

---

> [!proposition] Basic Properties of Ring Homomorphisms  
> Let $\varphi : R \to S$ be a homomorphism.  
> (a) If $a \in R$ and $n \ge 0$, then $\varphi(a^n) = \varphi(a)^n$.  
> (b) If $u \in R^\times$, then $\varphi(u) \in S^\times$ and $\varphi(u^n) = \varphi(u)^n$ for all $n \in \mathbb{Z}$.  
> (c) If $\varphi$ is an isomorphism, then $\varphi^{-1}$ is a ring homomorphism.

> [!proof]  
> (a) Standard proof by induction.  
> (b) $1 = \varphi(1) = \varphi(uu^{-1}) = \varphi(u)\varphi(u^{-1})$,  
> so $\varphi(u) \in S^\times$ and $\varphi(u^{-1}) = \varphi(u)^{-1}$.  
> Then by (a), $\varphi(u^n) = \varphi(u)^n$ for all $n \in \mathbb{Z}$.  
> (c) We already know $\varphi^{-1}$ is a group homomorphism.  
> $\varphi(1_R) = 1_S \Rightarrow \varphi^{-1}(1_S) = 1_R$.  
> For $a, b \in S$, write $a = \varphi(\varphi^{-1}(a))$, $b = \varphi(\varphi^{-1}(b))$, so:  
> $ab = \varphi(\varphi^{-1}(a))\varphi(\varphi^{-1}(b)) = \varphi(\varphi^{-1}(a)\varphi^{-1}(b))$  
> $\Rightarrow \varphi^{-1}(ab) = \varphi^{-1}(a)\varphi^{-1}(b)$  
> $\Rightarrow \varphi^{-1}$ is a homomorphism.

---

> [!proposition] Image and Kernel of a Ring Homomorphism  
> Let $\varphi : R \to S$ be a homomorphism, where $S$ is not the zero ring.  
> (a) $\text{Im} \varphi$ is a subring of $S$.  
> (b) $\ker \varphi$ is an ideal of $R$.

> [!proof]  
> (a) We know $\text{Im} \varphi$ is a subgroup of $(S, +)$.  
> Since $\varphi(1_R) = 1_S$, we have $1_S \in \text{Im} \varphi$.  
> If $a, b \in \text{Im} \varphi$, then $a = \varphi(x)$, $b = \varphi(y)$ for some $x, y \in R$, and  
> $ab = \varphi(x)\varphi(y) = \varphi(xy) \in \text{Im} \varphi$.

> (b) We’ll prove this properly when we do ideals.  
> Note: if $1 \in \ker \varphi$ and $\varphi$ is unital, then $1_S = \varphi(1_R) = 0_S$,  
> so $S$ must be the zero ring.
