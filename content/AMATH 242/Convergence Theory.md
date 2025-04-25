
- **Theorem 2.1 (Intermediate Value Theorem)**  
	- If $f(x)$ is continuous on a closed interval $[a,b]$ and $c\in[f(a),f(b)]$, then there exists $x^*\in[a,b]$ such that  $$f(x^*) = c$$
- **Theorem 2.2**  
	- If $f(x)$ is continuous on $[a_0,b_0]$ with $f(a_0)\,f(b_0)\le0$, define for $k\ge1$  $$
a_k = 
\begin{cases}
a_{k-1}, & \text{if }f\bigl(\tfrac{a_{k-1}+b_{k-1}}2\bigr)\,f(a_{k-1})\le0,\\
\tfrac{a_{k-1}+b_{k-1}}2, & \text{otherwise},
\end{cases}
\quad
b_k = 
\begin{cases}
b_{k-1}, & \text{if }f\bigl(\tfrac{a_{k-1}+b_{k-1}}2\bigr)\,f(a_{k-1})>0,\\
\tfrac{a_{k-1}+b_{k-1}}2, & \text{otherwise}.
\end{cases}
$$  Then $f(a_k)\,f(b_k)\le0$ for all $k$.

- **Theorem 2.3 (Contraction Mapping Theorem)**  
	- Let $g$ be a real-valued function, defined and continuous on $[a,b]$, with $g(x)\in[a,b]$ and suppose $g$ is a contraction on $[a,b]$. Then  
		1. $g$ has a unique fixed point $x^*\in[a,b]$.  
		2. The iterates $x_{k+1} = g(x_k)$ converge to $x^*$ for any $x_0\in[a,b]$.
- **Theorem 2.4 (Convergence Theorem for Newton’s Method) *(Atkinson p.60)***  
	- If $f(x^*)=0$, $f'(x^*)\neq0$, and $f,f',f''$ are continuous on $I_\delta=[x^*-\delta,x^*+\delta]$, then with $x_0$ sufficiently close to $x^*$ the Newton iterates converge quadratically, with  $$
	\lim_{i\to\infty}c_i = \left|\frac{f''(x^*)}{2\,f'(x^*)}\right|.
	$$
- **Theorem 2.5 (Convergence Theorem for Secant Method) *(Atkinson p.67)***  
	- If $f(x^*)=0$, $f'(x^*)\neq0$, and $f,f',f''$ are continuous on $I_\delta=[x^*-\delta,x^*+\delta]$, then the secant iterates converge with order  $$q = \tfrac12\,(1 + \sqrt5).$$
