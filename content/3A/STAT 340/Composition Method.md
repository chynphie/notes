- $F(x)=\sum_{k=1}^{\infty} p_k F_k(x)$  where $\sum_{k=1}^{\infty} p_k=1$ 
-  **Proposition**：
	- Let $K$ be a discrete random variable with pmf $p_k=P(K=k)$, $k\in\mathbb{N}$, and let $F_k$, $k\in\mathbb{N}$, be cdfs.  
	- If $X|K=k\sim F_k$, $k\in\mathbb{N}$, then $X\sim F(x)=\sum_{k=1}^{\infty} p_k F_k(x)$.  
	Proof：
	We know that $P(X\leq x)=\sum_{k} P(X\leq x|K=k)P(K=k)$,  which simplifies to  $\sum_{k} F_k(x)p_k=F(x)$ .

-  **Algorithm**
	1. Sample $K$.
	2. Sample $X\sim F_K$.
	3. Return $X$.
- Example: 
	Given  $f(k)=\left(\frac{1}{2}\right)^{k+1}+\frac{2^{k-1}}{2 \cdot3^{k+1}}$,  this is a composition for a mixture of geometric distributions:  $=\frac{1}{2} \left(\frac{1}{1-\frac{1}{3}}\right)^{k-1}+\frac{1}{2} \left(\frac{1}{1-\frac{2}{3}}\right)^{k-1}$,  
	
	where  $\sim\text{Geo} \left(\frac{1}{3}\right)$  and  $\sim\text{Geo} \left(\frac{2}{3}\right)$.  
	
	For inverse transform sampling:  $F_1^{-1}(X)=\frac{\log(U)}{\log(1/3)}$,  $F_2^{-1}(X)=\frac{\log(U)}{\log(2/3)}$.  
	1. Sample $V\sim U(0,1)$.  
	2. Return  $X=\frac{\log(V)}{\log(1/3)}$ if $V\leq 1/2$, else $X=\frac{\log(V)}{\log(2/3)}$.  