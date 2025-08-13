> [!definition] Group Ring
> Let $G$ be a group, and let $R$ be a ring. The group ring $RG$ of $G$  
> with coefficients in $R$ is the set of formal sums  
> $\left\{\sum_{g \in G} c_g \cdot g : (c_g)_{g \in G} \subseteq R \text{ such that there is a finite subset } X \subset G \text{ with } c_g = 0 \text{ for all } g \notin X \right\}$.  
> with operations  
> $\left(\sum_{g \in G} a_g g\right) + \left(\sum_{g \in G} b_g g\right) = \sum_{g \in G} (a_g + b_g)g$  
> and  
> $\left(\sum_{g \in G} a_g g\right)\cdot\left(\sum_{g \in G} b_g g\right) = \sum_{g,h \in G} a_g b_h gh = \sum_{k \in G} \left(\sum_{g \in G} a_g b_{g^{-1}k} \right)k$

> [!note] What’s a formal sum?
> A formal sum $\sum_{g \in G} a_g g$ with coefficients in $R$ is a fancy way of  
> writing a finitely supported function $G \to R : g \mapsto a_g$  
> Finitely supported: 0 except at finitely many points of $G$  
> The group elements $g \in G$ are “placeholders” in this formal sum

> [!example] Example
> $R = \mathbb{Z},\ G = D_6 = \{e, r, s, sr, s^2, s^2r\}$.  
> Here are some examples of elements of $\mathbb{Z}D_6$:  
> $1e + 7s - 2r + sr - s^2r$  
> $2e + 2s + 2s^2$  
> General element of $RD_6$ is $a_e e + a_r r + a_s s + a_{sr} sr + a_{s^2} s^2 + a_{s^2r} s^2r$  
> where $a_e, a_r, a_s, a_{sr}, a_{s^2}, a_{s^2r} \in R$.

> [!note] $G$ versus $RG$
> Group elements $g \in G$ can be regarded as elements of $RG$  
> i.e. $g = 1 \cdot g + \sum_{h \ne g} 0 \cdot h$  
> Technically speaking, however, $g \in G$ and $1 \cdot g \in RG$ are different  
> Sometimes write $g$ for $g$ considered as an element of $RG$  
> (this helps emphasize the difference)  
> Can also write $\sum_{g \in G} a_g g$ as $\sum_{g \in G} a_g g$ if it’s helpful

> [!example] Example
> Consider $G = \mathbb{Z}_+$ and $R = \mathbb{Z}$. Elements of $RG = \mathbb{Z}\mathbb{Z}$ look like:  
> $3 \cdot 0 - 2 \cdot 1 + 5 \cdot 10 - 6 \cdot (-6)$  
> $1 + 2 + 3$  
> $0$ (note: not equal to $0 = 0 \cdot 0 + 0 \cdot 1 + \dots$)

> [!note] What are the ring operations?
> Use component-wise addition:  
> **Example**: In $\mathbb{Z}D_6$,  
> $(2 \cdot e - s + 3 \cdot s^2r) + (3 \cdot e + s + r) = 5 \cdot e + r + 3 \cdot s^2r$  
>  
> For multiplication, use principle that $g \cdot h = gh$  
> Extend to $RG$ so distributivity holds:  
> **Example**: In $\mathbb{Z}D_6$ again,  
> $s \cdot (e + 2s + 3r + 4s^2r) = s + 2s^2 + 3sr + 4r$  
> $(e + 2s)(2e - 3r) = 2e + 4s - 3r - 6sr$  
> $(e - r)^2 = (e - r)(e - r) = e - r - r + r^2 = 2e - 2r = 2(e - r)$  
>  
> **Example**: $\mathbb{Z}\mathbb{Z}$,  
> $(0 + 2 \cdot (-6))(3 \cdot 1 - 4 \cdot 2) = 3 \cdot 1 - 4 \cdot 2 + 6 \cdot (-5) - 8 \cdot (-4)$

> [!proposition] Group Ring Structure
> Let $R$ be a ring, and $G$ a group. Then $RG$ is a ring with identity $e$.  
> If $G$ is commutative then $RG$ is commutative.  
> Group rings are very important examples of noncommutative  
> (more accurately, not-necessarily-commutative) rings.  
> However, since we’re focusing on commutative rings in this course,  
> we won’t prove this proposition.  
>  
> Let’s check that $e$ is an identity:  
> $e \cdot \left(\sum_{g \in G} a_g g\right) = \sum_{g \in G} a_g e \cdot g = \sum_{g \in G} a_g g$  
> and right identity is similar.  
> Remainder of proof reduces to fact that $\cdot$ is associative.

> [!proposition] Homomorphisms
> Let $R$ be a ring, and $\varphi: G \to H$ be a group homomorphism. Then  
> $\psi: RG \to RH$ defined by  
> $\psi\left(\sum_{g \in G} a_g g\right) = \sum_{g \in G} a_g \varphi(g)$  
> is a ring homomorphism.

> [!proof]  
> **Exercise**: check well-definedness  
> ($\sum_{g:\varphi(g)=h} a_g$ is finite for $h \in H$,  
> and $\psi(x)$ is finitely supported for all $x \in RG$)  
> $\psi(e_G) = \varphi(e) = e_H$, so $\psi$ is unital.  
> Let $x = \sum_{g \in G} a_g g,\ y = \sum_{h \in G} b_h h$  
> Then  
> $\psi(x + y) = \psi\left(\sum_{g \in G} (a_g + b_g)g\right) = \sum_{g \in G} (a_g + b_g)\varphi(g)$  
> $= \sum_{g \in G} a_g \varphi(g) + \sum_{g \in G} b_g \varphi(g) = \psi(x) + \psi(y)$

> [!proof] Continued
> $\psi(xy) = \psi\left(\sum_{g,h} a_g b_h gh\right) = \sum_{g,h} a_g b_h \varphi(gh)$  
> $= \sum_{g,h} a_g b_h \varphi(g)\varphi(h) = \left(\sum_g a_g \varphi(g)\right)\left(\sum_h b_h \varphi(h)\right)$  
> $= \psi(x)\psi(y)$  
> So $\psi$ is a homomorphism.
