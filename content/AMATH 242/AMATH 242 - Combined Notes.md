---
tags: [AppliedMath, FFT, FT, Interpolation]
---
[[AMATH242-Outline]]
### Errors and Error Propagation

- ***Theorem 1.1*** :
	-  For any floating point system $F$ under chopping,$$|\delta x| = \left|\frac{x - fl(x)}{x}\right| \le \epsilon_{mach}$$
- **Theorem 1.2 (Cauchy–Schwartz Inequality)**  
	- Let $\|\cdot\|$ be a vector norm over a vector space $V$ induced by an inner product. Then  
	$$
	|\vec{x}\cdot\vec{y}| \le \|\vec{x}\|\,\|\vec{y}\|
	$$

---
### Convergence Theory

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

---
### Numerical Linear Algebra

- **Theorem 3.1 (Existence and Uniqueness) : Consider $A\vec x = \vec b$.**  
	- Case 1: $\det(A)\neq0$ (rows/columns independent) ⇔ unique solution $\vec x = A^{-1}\vec b$.  
	- Case 2: $\det(A)=0$ ⇒  
		- If $\vec b\in\mathrm{range}(A)$ then infinitely many solutions.  
		- If $\vec b\notin\mathrm{range}(A)$ then no solution.
- **Theorem 3.2 (LU Factorization)**  
	- For all $A\in\mathbb R^{n\times n}$ there exist a permutation matrix $P$, a unit lower‐triangular $L$ and upper‐triangular $U$ such that  $$PA = LU.$$
- **Theorem 3.3 (Convergence of Jacobi & Gauss–Seidel)**  
	- Let $\vec x^{(0)}$ be any start. If $A$ is strictly diagonally dominant then both Jacobi and Gauss–Seidel iterations converge to the unique solution of $A\vec x = \vec b$.
- **Theorem 3.4 (Convergence of General Iterative Methods)** 
	- Consider $$\vec x^{(i+1)} = \vec x^{(i)} + B^{-1}(\vec b - A\vec x^{(i)})$$with $\det(A)\neq0$. If there is a matrix‐norm $\|\cdot\|_p$ such that  $$\|I - B^{-1}A\|_p < 1,$$then the iteration converges in that norm for any start $\vec x^{(0)}$.

---
### Polynomial Interpolation
- [[Hermite interpolating Polynomial]] :
	-  Method 1: 
		1. **List your “nodes” with multiplicity**
			- $z0​=a,z1​=a,z2​=b,z3​=b.$
		2. **Fill in the zeroth column** with 
			- $f[z0​]=f(a),f[z1​]=f(a),f[z2​]=f(b),f[z3​]=f(b).$
		3. **First divided differences**
			
			- For the repeated node at a:
				- $f[z1​,z0​]=f'(a)$
			- For the mixed node (a,b)
				- $f[z2​,z1​]=\frac{f(b)−f(a)​}{b−a}.$
			- For the repeated node at b:
				- $f[z3​,z2​]=f′(b).$
		4. **Second divided differences**
			- $f[z2​,z1​,z0​]=\frac{f[z2​,z1​]−f[z1​,z0​]​}{z2​−z0​}=\frac{\frac{f(b)−f(a)}{b−a}​−f′(a)}{b−a}​,$
			- $f[z2​,z1​,z0​]=\frac{f[z3​,z2​]−f[z2​,z1​]}{z3​−z1​}=\frac{\frac{f(b)−f(a)}{b−a}​−f′(a)}{b−a}​,$
		5. **Third divided difference**
			- $f[z3​,z2​,z1​,z0​]=\frac{​f[z3​,z2​,z1​]−f[z2​,z1​,z0​]​}{z3​−z0}=\frac{f[z3​,z2​,z1​]−f[z2​,z1​,z0​]}{b−a}$
		6. **Write the Newton form**
			- $H(x)=f[z0​]+f[z1​,z0​](x−z0​)+f[z2​,z1​,z0​](x−z0​)(x−z1​)+f[z3​,z2​,z1​,z0​](x−z0​)(x−z1​)(x−z2​)$
- [[Cubic Spline]]:
	1. Uses cubic polynomials between successive nodes
	2. Satisfies specific interpolation and smoothness conditions
	
	- **Boundary Conditions**
		1. Free Boundary (Natural Cubic Spline):
			- $S_1'(x0) = 0$
			- $S_n'(xn) = 0$
		2. Clamped Boundary:
			- Specifies first derivatives at endpoints
			- Generally leads to more accurate approximation
		3. Periodic Boundary:
			- Requires $f0 = fn$
			- First and second derivatives of first and last polynomials are equal
	- **Cubic Spline Construction**
		- Requires determining 4n constants
		- Polynomial form:$Sj(x) = aj + bj(x - xj) + cj(x - xj)² + dj(x - xj)³$
		- Uses complex system of equations to determine coefficients

---
### Numerical Integration
- **Numerical Quadrature**: Approximating definite integrals numerically, using weighted sum of integrand value. i.e. $I(f)=∫_{a}^{b}f(x)dx\approx Q_{n}(f)=\sum(w_{i}f(x_{i}))$
	- Methods finding Nodes (xi) and weights (wi):
		1. *Method of Undetermined Coefficients*
			![[Pasted image 20250418094722.png|436|468x199]]
			![[Pasted image 20250418094629.png|435|484x165]]
	
		2. *Polynomial Interpolation*
		3. *Lagrange Interpolating Polynomial*
#### The Newton-Cotes Rules:
- Uses equally spaced points in interval [a, b]
- Node spacing: h = (b-a)/n

| **Rules**                | Conditions                                  | Formula                                            | **Truncation Error**                     | **Degree of Precision** |
| ------------------------ | ------------------------------------------- | -------------------------------------------------- | ---------------------------------------- | ----------------------- |
| Mid-point (deg $=1$)     | $x_{0}=\frac{a+b}{2}\:$                     | $\hat{I}(f)=(b-a)f\left( \frac{a+b}{2} \right)$    | $\frac{(b - a)^3}{24} \, f''(\xi)$       | 1                       |
| Trapezoid (deg $\leq2$)  | $x_{0}=a,\:x_{1}=b$                         | $\hat{I}(f)=\frac{1}{2}(b-a)[f(a)+f(b)]$           | $\frac{-(b - a)^3}{12} \, f''(\xi)$      | 2                       |
| Simpson's (deg $\leq$ 3) | $(x_{0},f_{0}),(x_{1},f_{1}),(x_{2},f_{2})$ | $\hat{I}(f)=\frac{1}{6}(b-a)[f(a)+4f(x_{1})+f(b)]$ | $\frac{(b - a)^5}{2880} \, f^{(4)}(\xi)$ | 3                       |


- **Composite Mid-point Rule:** 
	
	![[Pasted image 20250418111636.png | 400]]
	- $T(f)=h\sum_{i=1}^{n}f(x_{m_{j}}),\:m_{j}=a+\left( j-\frac{1}{2} \right)h$
	- $E(f)=\frac{b-a}{h}h^{2}f''(c)$
- **Composite Trapezoid Rule**: 
	
	![[Pasted image 20250418111838.png | 400]]
	- $T(f)=\frac{h}{2}[ f(a)\:+\sum_{i=1}^{n-1}2f(x_{i})+f(b)], h=\frac{b-a}{n}$
	- $|E(f)|\leq \frac{h^{2}}{12}(b-a)M,\:M=max|f''(x)|\:for\:a\leq x\leq b$
- **Composite Simpson's Rule (also 1/3 Simpsons Rule):**
	
	![[Pasted image 20250418111615.png | 400]]
	- Properties:
		1. Subintervals are **even** as we integrate 2 subsections at a time
		2. **Simpson’s 1/3 rule** is a special case of Newton–Cotes formulas and integrates up to degree 3 exactly
	- *Example*: Evaluate integral $∫_{0}^{1}\:\frac{1}{x+4}dx$ using the composite midpoint rule with n=6:
	- $T(f)=\frac{h}3\left[ f(x_{0})+2\sum_{i=1}^{n/2-1} f(x_{2j})+4\sum_{i=i}^{n/2}f(x_{2i-1})+f(x_{n})\right]$
	- $E(f)=-\frac{b-a}{180}h^{4}f^{(4)}(c)$

#### Gaussian Quadrature :
1. Key Ideas:
	- Chooses **optimal** evaluation points instead of equally spaced points
	- Aims to minimize approximation error
	- Provides exact results for polynomials up to specific degree
2. Advantages:
	- More **Accurate*** than Newton-Cotes formulas
	- Flexible node and coefficient selection
	- Higher precision for complex functions
- **Formula**: $\hat{I}(f)=\frac{b-a}{2}\left[ f\left( \left( \frac{b-a}{2} \right)\left( -\frac{1}{\sqrt{ 3 }} \right)+\frac{b+a}{2} \right)+f\left( \left( \frac{b-a}{2} \right)\left( \frac{1}{\sqrt{ 3 }} \right)+\frac{b+a}{2} \right) \right]$ is an approximation for $I=∫_{a}^{b}f(x)dx$ with degree of precision 3
	- one point is midpoint rule
![[Pasted image 20250418112846.png |600]]

<div style="page-break-after: always;"></div>

### Discrete Fourier Methods
#### [[Real Fourier Series]]
- Process of representing periodic functional data as a combination of trigonometric functions
- Fourier analysis is a method of approximating **periodic functional** data using combinations of sine and cosine waves, converting time or spatial information into frequency information.
- **Applications**:
	1. Identifying phone button sounds
	2. Storing images
	3. Optical information processing
	4. MP3 compres
- ***Euler's Formula***: 
	- $e^{i\theta}=\cos(\theta)+i\sin(\theta)$
	- $e^{-i\theta}=\cos(\theta)-i\sin(\theta)$
- ***[[Periodic Functions]]***: A function f(t) is periodic if $f(t + T) = f(t)$
	- **Fundamental period** $\frac{T}{k}$: Smallest positive T that satisfies the periodicity condition
	- **Frequency**: $f = 1/T$ (oscillations per second)
	- **Angular frequency**: $ω = 2πf$ (radians per second)
- Steps to Solve for Real **Fourier series**
	1. $f(t) = \frac{a_{0}}{2}+ \sum_{k=0}^{\infty}a_kcos\left( {2πkt}/{T} \right) + b_ksin\left( {2πkt}/{T} \right)$
	2. $a_{k}=\frac{2}{b-a}∫_{a}^{b}f(t)\cos\left( \frac{2\pi k}{b-a}t \right)dt$
		- If f(t) is odd, then odd * even = odd, $a_{k}=0$
	3. $b_{k}=\frac{2}{b-a}∫_{a}^{b}f(t)\sin\left( \frac{2\pi k}{b-a}t \right)dt$
	4. $a_{0}=\frac{2}{b-a}∫_{a}^{b}f(t)dt$
	Example:
	>![[AMATH 242/Pasted Photos/image-6.png|600|653x281]]
	![[AMATH 242/Pasted Photos/image-7.png|600|690x363]]

	- Properties to determine $a_{k},b_{k}$: if $N=2\pi\text{ and }t\:\in[0,2\pi]$ then
		1. $∫_{0}^{2\pi}\cos(kt)\sin(kt)dt=0$
		2. $∫_{0}^{2\pi}\cos(kt)\cos(jt)dt=0\:if\:k\neq j$ 
		3. $∫_{0}^{2\pi}\sin(kt)\sin(kt)dt=0,\:j\neq k$
		4. $∫_{0}^{2\pi}\cos(kt)=∫_{0}^{2\pi}\sin(jt)dt=0$ 
- Function properties:
	1. $f(x)=f(-x)\implies \text{Even function}$
	2. $f(x)=-f(-x)\implies \text{odd function}$
### **[[Discrete Fourier Transform]]**:
 - The DFT of a discrete-time signal $f[n]$ with $0 \le n \le N-1$ is$$F[k] = \mathrm{DFT}\{f[n]\}= \sum_{n=0}^{N-1} f[n]\,W_N^{-kn},\quad0 \le k \le N-1.$$
- The inverse DFT is$$f[n] = \mathrm{IDFT}\{F[k]\}= \sum_{k=0}^{N-1} F[k]\,W_N^{kn},\quad0 \le n \le N-1.$$

- Nth Roots of Unity: 
	- The $N$th roots of unity are the integer powers of$$W_N := \exp\!\biggl(i\frac{2\pi}{N}\biggr).$$We may write the $N$ distinct $N$th roots of unity as$$W_N^k = \exp\!\biggl(i\frac{2\pi k}{N}\biggr),\quad k = 0,1,\dots,N-1.$$
- Proposition
	- The $N$th roots of unity satisfy:
		1. $(W_N^k)^N = 1$, since
		   $$(W_N^k)^N = \exp\!\Bigl(i\frac{kN\,2\pi}{N}\Bigr)= \exp(i k\,2\pi)= 1.$$
		2. The complex conjugate of a root is$$\bigl(W_N^k\bigr)^* = W_N^{\,N-k}.$$
- **Proposition**
	- The frequency-domain signal $F[k]$ is periodic with period $N$:$$F[k] = F[k + sN],\quad\:s \in \mathbb{Z}.$$
- **Theorem (Avoid Aliasing):**  
	- To avoid aliasing error, the sampling frequency $f_s$ should be at least twice the largest frequency present in the continuous signal.
	>Human-audible sound falls in the range 20 Hz to 20 kHz.  Thus we require$$f_s \ge 2 \times 20{,}000\text{ Hz} = 40\text{ kHz}$$

- ***Fundamental convergence theorem for Fourier series***: 

	![[AMATH 242/Pasted Photos/image-4.png |800|432x119]]


	![[AMATH 242/Pasted Photos/image-5.png|469x236]]
#### Complex Fourier series:
- $f(t)=\sum_{k=-\infty}^{\infty}c_{k}e^{ikt}dt$  with f(t) defined on $[-\pi,\pi]$ and
- $c_{k}=\frac{1}{2\pi}∫_{-\pi}^{\pi}f(t)e^{-ikt}dt=\frac{1}{2}(a_{k}-ib_{k})$ 
- The real an complex coefficients have the following properties
	1. $\bar{c_{k}}=c_{-k}$
	2. $a_{-k}=a_{k},b_{-k}=-b_{k}$
	3. $b_{0}=0,c_{0}=\frac{1}{2}a_{0}$
	4. $a_{k}=2\mathrm{Re}(c_{k}),\:b_{k}=-2Im(c_{k})$
	5. If f(t) is even, Im($c_{k}$) =0. f(t) odd, Re($c_{k}$)=0
![[AMATH 242/Pasted Photos/image-1 2.png]]

### [[Fast Fourier Transform]]
- Assume the factors $W_{N}^{kn}$ are precomputed and stored in a table
- use Formula directly to compute N coefficients $F[k]$. Amount of work is then $W=(N-1)A+(N+1)M=2N\:flops/coefficient\implies Total\:work\:is\:then\:N(2N)=2N^{2}$
- **Theorem 4.4**:
	- If $N=2^{m}$ for some integer m, then the length N DFT F[k] of discret Time signals f[n] can calculated by combining two length $\frac{N}{2}$ DFT. we define
		- $g[n]=f[n]+f\left[ n+\frac{N}{2} \right]$
		- $h[n]=\left( f[n]-f\left[ n+\frac{N}{2} \right] \right)W_{N}^{-n}$
		Then
		- $F[2l]=\frac{1}{2}DFT\{ g[n] \}$ (even indices)
		- $F[2l+1]=\frac{1}{2}DFT\{ h[n] \}$ (odd indices)
