---

---
### The first isomophism theorem
> [!theorem] Universal Property of Quotients  
> Suppose $\varphi : G \to K$ is a homomorphism, and $N \trianglelefteq G$. Let  
> $q : G \to G/N$ be the quotient homomorphism. Then there is a  
> homomorphism $\psi : G/N \to K$ such that $\psi \circ q = \varphi$ if and only if  
> $N \subseteq \ker \varphi$. Furthermore, if $\psi$ exists, then it is unique.

> [!definition]  
> If $G$, $K$ are groups, let $\text{Hom}(G, K)$ be the set of morphisms $G \to K$.

> [!corollary]  
> For any groups $G$, $K$, and $N \trianglelefteq G$, the function  
> $q^* : \text{Hom}(G/N, K) \to \{\varphi \in \text{Hom}(G, K) : N \subseteq \ker \varphi\} : \psi \mapsto \psi \circ q$  
> is a bijection.

 Comparison: Universal Property of Products

> [!theorem]  
> Let $\alpha : H \to G$ and $\beta : K \to G$ be homomorphisms, and let  
> $i_H : H \to H \times K$ and $i_K : K \to H \times K$ be the inclusions of $H$ and  
> $K$ in the product $H \times K$. Then there is a homomorphism  
> $\varphi : H \times K \to G$ such that $\varphi \circ i_H = \alpha$ and $\varphi \circ i_K = \beta$ if and only if  
> $\alpha(h)\beta(k) = \beta(k)\alpha(h)$ for all $h \in H$, $k \in K$.

> [!corollary]  
> There is a bijection between $\text{Hom}(H \times K, G)$ and  
> $\{(\alpha, \beta) \in \text{Hom}(H, G) \times \text{Hom}(K, G) : \alpha(h)\beta(k) = \beta(k)\alpha(h)$  
> for all $h \in H$, $k \in K\}$.

> [!theorem] Universal Property of Quotients  
> Suppose $\varphi : G \to K$ is a homomorphism, and $N \trianglelefteq G$. Let  
> $q : G \to G/N$ be the quotient homomorphism. Then there is a  
> homomorphism $\psi : G/N \to K$ such that $\psi \circ q = \varphi$ if and only if  
> $N \subseteq \ker \varphi$. Furthermore, if $\psi$ exists, then it is unique.

> [!lemma]  
> If $\alpha : G \to H$ is surjective, and $\psi_1, \psi_2 : H \to K$ satisfy  
> $\psi_1 \circ \alpha = \psi_2 \circ \alpha$, then $\psi_1 = \psi_2$.

- Proof:   
	- If $h \in H$, then there is $g \in G$ with $\alpha(g) = h$.  
	- So $\psi_1(h) = \psi_1(\alpha(g)) = \psi_2(\alpha(g)) = \psi_2(h)$.  
	- We conclude that $\psi_1 = \psi_2$.
	- If $\psi$ exists, and $n \in N$, then $\varphi(n) = \psi(q(n)) = \psi(e) = e$  
	- so $N \subseteq \ker \varphi$.  
	- Suppose $N \subseteq \ker \varphi$. Define $\psi : G/N \to K : [g] \mapsto \varphi(g)$.  
	- To show $\psi$ is well-defined, note that if $[g] = [h]$, then  
	- $g^{-1}h \in N \subseteq \ker \varphi$, so $\varphi(g)^{-1}\varphi(h) = \varphi(g^{-1}h) = e$,  
	- so $\varphi(g) = \varphi(h)$.
	- Clearly $\psi \circ q(g) = \psi([g]) = \varphi(g)$ for all $g \in G$, so $\psi \circ q = \varphi$.  
	- If $[g], [h] \in G/N$, then  
	- $\psi([g] \cdot [h]) = \psi([gh]) = \varphi(gh) = \varphi(g)\varphi(h) = \psi([g])\psi([h])$,  
	- so $\psi$ is a homomorphism.  
	- If $\psi' : G/N \to K$ is another homomorphism with $\psi' \circ q = \varphi$,  
	- then $\psi' \circ q = \psi \circ q \Rightarrow \psi' = \psi$ by Lemma.  
	- So uniqueness holds.

- Equivalent way to define $\psi$:  
	- $\varphi(gN) = \varphi(g)\varphi(N) = \varphi(g)\{e\} = \{\varphi(g)\}$  
	- So if $S \in G/N$, then $\varphi(S) = \{b\}$, a singleton set  
	- Can define $\psi(S) = b$ for $b \in K$ such that $\varphi(S) = \{b\}$

- The First Isomorphism Theorem
	- Recall: If $\varphi : G \to K$ is a homomorphism then $[G : \ker \varphi] = |\text{Im} \varphi|$  
	- **Proof:** There is a bijection $\psi : G/\ker \varphi \to \text{Im} \varphi$ defined by  
	- $\psi(S) = b$, where $b \in K$ is such that $\varphi(S) = \{b\}$  
	- This looks like what we just did!  
	- Now we know $G/\ker \varphi$ is a group, $|G/\ker \varphi| = [G : \ker \varphi] = |\text{Im} \varphi|$  
	- Maybe this bijection is an isomorphism?


> [!theorem] First Isomorphism Theorem  
> Suppose that $\varphi : G \to K$ is a homomorphism. Then there is an  
> isomorphism $\psi : G/\ker \varphi \to \text{Im} \varphi$ such that $\varphi = \psi \circ q$, where  
> $q : G \to G/\ker \varphi$ is the quotient homomorphism.

Proof: 
- $\ker \varphi \subseteq \ker \varphi$, so by universal property there is a homomorphism  
- $\psi : G/\ker \varphi \to K$ with $\psi \circ q = \varphi$.  
- $\psi([g]) = \varphi(g)$, so plainly $\text{Im} \psi = \text{Im} \varphi$. Thus we can regard $\psi$ as  
- surjective homomorphism $G/\ker \varphi \to \text{Im} \varphi$.  
- $\psi$ agrees with the function $G/\ker \varphi \to \text{Im} \varphi$ defined previously, so  
- $\psi$ is a bijection $\Rightarrow$ $\psi$ is an isomorphism.  
- Or if $\psi([g]) = e$, then $\varphi(g) = e$, so $g \in \ker \varphi \Rightarrow [g] = [e]$.  
- So $\psi$ is injective $\Rightarrow$ isomorphism.

> [!important] Examples
> The first isomorphism theorem is the best way to determine $G/N$:
> 
> - Recall $\text{SL}_n K \trianglelefteq \text{GL}_n K$ is defined as the kernel of  
>   homomorphism $\det : \text{GL}_n K \to K^\times$.  
>   The image of $\det$ is $\text{Im} \det = K^\times$.  
>   By first isomorphism theorem, $\text{GL}_n K / \text{SL}_n K \cong K^\times$
> 
> - Consider $\mathbb{Z} \trianglelefteq \mathbb{R}$. What is $\mathbb{R}/\mathbb{Z}$?  
>   Have homomorphism $\exp : \mathbb{R} \to \mathbb{C}^\times : x \mapsto e^{2\pi i x}$  
>   $e^{2\pi i x} = 1$ if and only if $x \in \mathbb{Z}$  
>   $\text{Im}(\exp) = \{a \in \mathbb{C} : |a| = 1\} =: S^1$ (the circle group)  
>   So $\mathbb{R}/\mathbb{Z} \cong S^1$

---
### The Second Isomorphism Theorem  
 
 Recall from products
> [!definition] Definition  
> We say that $G$ is the internal direct product of subgroups $H, K \le G$ if  
> (a) $HK = G$,  
> (b) $H \cap K = \{e\}$, and  
> (c) $hk = kh$ for all $h \in H$, $k \in K$.

> [!lemma] Lemma  
> Suppose $G = HK$ for $H, K \le G$. Then every element $g \in G$ can  
> be written as $g = hk$ for unique $h \in H$, $k \in K$, if and only if  
> $H \cap K = \{e\}$.

The second isomorphism theorem
Suppose $H, K \le G$.

> [!lemma] Lemma  
> Every element of $HK$ can be written as $hk$ for unique $h \in H$,  
> $k \in K$, if and only if $H \cap K = \{e\}$.  
> If $H \cap K = \{e\}$, then $|HK| = |H| \cdot |K|$.

- What is $|HK|$ if $H \cap K \ne \{e\}$?
	- $HK = \bigcup_{h \in H} hK$, a union of cosets of $K$.
	- Let $X = \{hK : h \in H\} \subseteq G/K$.
	- Then $X$ is a partition of $HK$, so $|HK| = |X| \cdot |K|$.
	- How large is $X$?

> [!lemma] Lemma  
> Let $H, K \le G$. If $h_1, h_2 \in H$, then $h_1K = h_2K$ if and only if  
> $h_1(H \cap K) = h_2(H \cap K)$.

> [!proof]  
> $h_1K = h_2K \Leftrightarrow h_1^{-1} h_2 \in K \Leftrightarrow h_1^{-1} h_2 \in H \cap K$.  
> But $h_1^{-1} h_2 \in H \cap K$ if and only if $h_1H \cap K = h_2H \cap K$.

Rephrasing: Consider equivalence relations $\sim_K$ on $G$, $\sim_{H \cap K}$ on $H$.  
If $h_1, h_2 \in H$, then $h_1 \sim_K h_2 \Leftrightarrow h_1 \sim_{H \cap K} h_2$.

> [!corollary] Corollary  
> $H / H \cap K \to X : h(H \cap K) \mapsto hK$ is a bijection.

- Proof: 
	- Lemma $\Rightarrow$ well-defined, injective. Surjectivity obvious.

Summary: If $H, K \le G$, $X = \{hK : h \in H\}$ partitions $HK$, so $|HK| = |X| \cdot |K|$.

> [!corollary] Corollary  
> $H / H \cap K \to X : h(H \cap K) \mapsto hK$ is a bijection.  
> $|X| = [H : H \cap K]$, so $|HK| = [H : H \cap K] \cdot |K|$.

Using $[H : H \cap K] \cdot |H \cap K| = |H|$, we have:

> [!proposition] Proposition  
> If $H, K \le G$, then $|HK| \cdot |H \cap K| = |H| \cdot |K|$.

Another way to think about this formula if $H, K$ finite:  
$[H : H \cap K] = |X| = \frac{|HK|}{|K|} \quad \leftarrow \text{is this an index as well?}$  
**Problem:** $HK$ not necessarily a group

> [!proposition] Proposition  
> Let $H, K \le G$. Then $HK \le G \Leftrightarrow HK = KH \Leftrightarrow KH \subseteq HK$.

Proof: 
- If $HK \le G$, and $h \in H$, $k \in K$, then $h, k \in HK$, so $kh \in HK$.  
- Also $k^{-1} h^{-1} \in HK$, so $k^{-1} h^{-1} = h_0 k_0$.  
- Hence $hk = (k^{-1} h^{-1})^{-1} = k_0^{-1} h_0^{-1} \in KH$.  
- So $KH \subseteq HK$ and $HK \subseteq KH \Rightarrow HK = KH$.  
 
- Conversely, suppose $KH \subseteq HK$. We always have $e \in HK$.  
- If $x, y \in HK$, then $x = h_0 k_0$, $y = h_1 k_1$ for $h_0, h_1 \in H$, $k_0, k_1 \in K$.  
- Since $KH = HK$, $k_0^{-1} h_0^{-1} h_1 = h_2 k_2$ for $h_2 \in H$, $k_2 \in K$.  
- So $x^{-1} y = k_0^{-1} h_0^{-1} h_1 k_1 = h_2 k_2 k_1 \in HK$.

> [!corollary]  
> If $KH \subseteq HK$, then $[H : H \cap K] = [HK : K]$.

- When is $KH \subseteq HK$?
	- **Sufficient condition:**  
	- For all $h \in H$, there is $h' \in H$ such that $Kh = h'K$.  
	- Recall: if $Kh = h'K$, then $h'K = hK$.
	
	- **Rephrase condition:** $hKh^{-1} = K$ for all $h \in H$, i.e., $H \subseteq N_G(K)$

> [!corollary] Corollary  
> If $H \subseteq N_G(K)$, then $HK \le G$, and hence $[H : H \cap K] = [HK : K]$.

- What else does the condition $H \subseteq N_G(K)$ imply?
	- We know $hKh^{-1} = K$, $kKk^{-1} = K$, so  
	- $H, K \subseteq N_{HK}(K) \Rightarrow N_{HK}(K) = HK \Rightarrow K \trianglelefteq HK$.
	
	- If $k \in H \cap K$, $h \in H$, then $hkh^{-1} \in H \cap K$  
	- So $H \cap K \trianglelefteq H$.

> [!theorem] Theorem (Second isomorphism theorem)  
> Suppose $H \subseteq N_G(K)$. Then $HK \le G$, $K \trianglelefteq HK$, and $H \cap K \trianglelefteq H$.  
> Furthermore, if $i_H : H \to HK$ is the inclusion, $q_1 : H \to H / H \cap K$  
> and $q_2 : HK \to HK / K$ are the quotient maps, then there is an  
> isomorphism $\psi : H / H \cap K \to HK / K$ such that $\psi \circ q_1 = q_2 \circ i_H$.


---
### The Third Isomophism Theorem
Suppose $N \trianglelefteq G$ and $N \le K \le G$.

**Correspondence theorem (homework):**  
$K \trianglelefteq G$ if and only if $K/N \trianglelefteq G/N$.

Suppose $K/N \trianglelefteq G/N$. What’s $(G/N)/(K/N)$?

> [!theorem] Third Isomorphism Theorem (Informal Version)  
> $(G/N)/(K/N) \cong G/K$

> [!example] Example  
> Suppose $n \mid m$, so that $m\mathbb{Z} \le n\mathbb{Z}$.  
> Then $(\mathbb{Z}/m\mathbb{Z})/(n\mathbb{Z}/m\mathbb{Z}) \cong \mathbb{Z}/n\mathbb{Z}$.  
> $$(\mathbb{Z}/20\mathbb{Z})/(5\mathbb{Z}/20\mathbb{Z}) \cong \mathbb{Z}/5\mathbb{Z}$$

Formal Statement

> [!theorem] Third Isomorphism Theorem  
> Let $N \trianglelefteq G$ and $N \le K \trianglelefteq G$. Let:  
> - $q_1$ be the quotient map $G \to G/N$,  
> - $q_2$ be the quotient map $G/N \to (G/N)/(K/N)$, and  
> - $q_3$ be the quotient map $G \to G/K$.  
> Then there is an isomorphism $\psi: G/K \to (G/N)/(K/N)$ such that  
> $\psi \circ q_3 = q_2 \circ q_1$.

G ──q₁──▶ G/N  
│        │  
q₃       q₂  
▼        ▼  
G/K ──ψ──▶ (G/N)/(K/N)

- Proof of Third Isomorphism Theorem  
	- Note that  
	- $\ker(q_2 \circ q_1) = (q_2 \circ q_1)^{-1}({e}) = q_1^{-1}(q_2^{-1}({e})) = q_1^{-1}(K/N) = K$  
	- $\text{Im}(q_2 \circ q_1) = (G/N)/(K/N)$
	
	- By the First Isomorphism Theorem, there is an isomorphism  
	- $\psi : G/K \to (G/N)/(K/N)$ such that $\psi \circ q_3 = q_2 \circ q_1$.
