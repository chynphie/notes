- ==Theorem 3.1.1== If A is SPD, then there exists unique $G_{L}$ with strictly positive entires on its diagonal s.t. $A=GG^T$, G is called *Cholesky factor*
- Constructing the Cholesky Factor 
	1. $A=\begin{bmatrix}1&0\:\\\frac{v}{\alpha}&I\end{bmatrix}\:\begin{bmatrix}\alpha\:&v^{T}\\0&B-\frac{vv^{T}}{\alpha}\end{bmatrix}$ 
	2. Dsd

```python
Algorithm 1 : Cholesky Factorization 

for k = 1,...,n 
	a_kk = sqrt(a_kk) 
	for i = k+1,...,n 
		a_ik = a_ik/a_kk 
		diagonal (v/√α) 
	end for 
	
	for j = k +1,...,n 
		for i = j,...,n 
			aij = aij − aik ∗ ajk 
			B −vvT/α 
		end for
	end for 
end for
```
- Runtime.= $\frac{n^{3}}{3}+O(n^{2})$