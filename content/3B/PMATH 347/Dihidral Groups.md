- <u>Example</u>: $M_{n}\mathbb{R},\:n\:\times n$ matrices over $\mathbb{R}$. Matrix multiplication is associative. The identity matrix is identity.
- The set of invertible matrices forms a group called the **general linear group** (over $\mathbb{R}$) Denoted by $GL_{n}\mathbb{R}$ 
-  **n-gon**:
	- A regular polygon $P_{n}$ with $n\geq3$ vertices
	![[Dihidral and permutation groups-1747064131204.png|435x164]]
- H contains points $v_{k}=\left( \cos\frac{2\pi k}{2} ,\sin\frac{2\pi k}{2}\right),\:o\leq k\leq n$ 
- A **symmetry** of the *n-gon* $P_n$ is an invertible linear transformation  $T ∈ GL_2(R)$ such that $T (P_n) = P_n$.  
-  $D_{2n}:=\{ symmetries\:of\:P_{n} \}$ 
- Contains: 
	- $e=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ the identity matrix
	- Rotation s by $\frac{2\pi}{n}$ radian is on $s(v_{i})=v_{i+1}$ for $i=0,..,n-1$
	- Reflection r through the x-axis is on $r(v_{i})=v_{n-i}$ 

> [!proposition] Proposition 1.10
> $D_{2n}$ is a group under composition. Proof(in subgroups)

> [!lemma] Lemma 1.11
> 1. If $T\in D_{2n}$, then $(T(v_{0}),T(v_{1}))$ are adjacent
> 2. If $S,T\in D_{2n}$ and $S(v_{i})=T(v_{i}),\:i=0,1$ then S=T
> - Proof: 
> 	- $v_{0},\:v_{1}$ are adjacent, T is linear
> 	- $v_0$, and $v_1$ are lineary independent

> [!corollary] Corollary 1.12 $|D_{2n}|\leq 2n$ 
> For every pair of adjacent vertices $(v_{i},v_{j})$ if there is an element $T\in D_{2n}$ with $T(v_{0})=v_{i},\:T(v_{1})=v_{j}$ then $|D_{2n}|=2n$

> [!proposition] Proposition
> $D_{2n}=\{ s^{i}r^{j}:0\leq i< n,0\leq j<2 \}$ and $|D_{2n}|=2n$. Also $rs=s^{-1}r=s^{n-1}r$
	
- **Claim 3**: The function $D^{2n}\to V,\:T\to(T(v_{0}),T(v_{1}))$ is a bijection:
	- Proof: Injective by claim 1. Surjective by rotation. 
	- So $D_{2n}=|V|=2n$
- **Summary**:
	- $D_{2n}=\{ s^{i}r^{j}:\:0\leq i< n,0\leq j<2 \}$
	- $s^{n}=e,\:r^{2}=e,\:rs=s^{-1}r$
	- $|D_{2n}|=2n$