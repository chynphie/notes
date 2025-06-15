> [!definition] Positive definite
> A matrix A is pos. Def. **iff** $\forall\:x\neq \vec{0}\in \mathbb{R}^{2}\:s.t.\:x^{T}Ax>0$
> 

- Remarks:
	1.  Determine if A is pos. Def. If we know A is symmetric
	2. The $k^{th}$ pivot of a matrix $A$ is $d_{k}=\frac{\det(A_{k})}{\det(A_{k-l})}$, $A_{k}$ is the kth leading principal matrix. 
	3. A is pos. Def. **iff** it can be written as $A=RR^{T}$

> [!theorem] SPD (symmetric positive definite matrix)
> If A is **SPD**, then there exists unique lower triangular $G$, with strictly **positive** entries on its diagonal, such that $A = GG^T$

