> [!definition] Homomorphism
> Let $G,H$ be groups. A function $:G\to H$ is a **homomorphism** if $$(g\cdot h)=(g)\cdot(h)$$ for all $g,h\in G$

> [!lemma] Lemma 3.1
> Suppose $\phi :G\to H$ is a homomorphism. Then
> 1. $\phi(e_{H})=e_{H}$
> 2. $\phi(g^{-1})=\phi(g)^{-1}$
> 3. $\phi(g^{n})=\phi(g)^{n}$ for all $n\in \mathbb{Z}$
> 4. $|\phi(g)|\:|\:|g|,\:\forall g\in G\:(n|\infty \:\forall n\in N)$

> [!lemma] Lemma 3.2 & 3.3
> if $H\leq G$, and H is considered as a group with the induced operation from G, 
> - then $i:H\to G:x\to x$ is a homomorphism
> - 

- Notation
	- $f:X\to Y$ is a f, $S\subseteq X$
		- $f(S)=\{ f(x):x\:\in\:S \}$
> [!proposition] Proposition
> - If $a:G\to H$ is a hom., and $K\subseteq G$ then $\phi(K)\leq H$

> [!definition] 
> if $\phi :G\to H$ is a homomorphism, the <u>image</u> of $\phi$ is the subgroup $\phi(G)$ of H

> [!lemma] 
> if $\phi:G\to H$
>  is a homo. And $lm\phi\leq K\leq H$, then $\hat{\phi}:G\to K:\:g\to \phi(g)$

> [!corollary] 
> if $\phi:G\to H$ is a hom, then $\phi$ induces a surjective $\phi:G\to lm\phi$

> [!proposition] 
> if $\phi:G\to H$ is a hom., $S\subseteq G$, then $\phi(\langle S \rangle)=\langle \phi(S) \rangle$

- Proof $\phi(s^{-1})=\{ \phi(x^{-1}):x\:\in S \}=\{ \phi(x)^{-1}:x\in S \}=\phi(s)^{-1}$ 
- Notation $f:X\to Y$ function, $S\subseteq Y,\:f^{-1}(s)=\{ x\:\in X:f(x)\in S\}$

> [!definition] Kernel
> if $\phi:G\to H$ is a homo, the kernel of $\phi$ is the subgroup $Ker(\phi)=\phi^{-1}(\{ e_{H} \})$ of G. $(Ker(\phi)=\{ g\in G:\phi(g)=e_{H} \})$

- Eg: 
	1. $\phi: \mathbb{R}^{+}\to \mathbb{R}^{+}:x\to e^{x}$
		- $Ker(\phi)=\{ x\:\in \mathbb{R}:e^{x}=1 \}=\{ 0 \}$
	2. $\phi:\mathbb{Z}\to m\mathbb{Z}:x\to mx$
		- $Ker(\phi)= \mathbb{Z}\:if\:m=0\:otherwise\:=\{ 0 \}$
	3. $Ker(\det:GL_{n}\mathbb{R}\to \mathbb{R})=SL_{n}\mathbb{R}$

> [!proposition] 
> - A Homo $\phi:G\to H$ is inj. Iff $ker(\phi)=\{ e_{G} \}$
> 
> 