- Uses equally spaced points in interval [a, b]
- Node spacing: h = (b-a)/n

| **Rules**                | Conditions                                  | Formula                                            | **Truncation Error**                     | **Degree of Precision** |
| ------------------------ | ------------------------------------------- | -------------------------------------------------- | ---------------------------------------- | ----------------------- |
| Mid-point (deg $=1$)     | $x_{0}=\frac{a+b}{2}\:$                     | $\hat{I}(f)=(b-a)f\left( \frac{a+b}{2} \right)$    | $\frac{(b - a)^3}{24} \, f''(\xi)$       | 1                       |
| Trapezoid (deg $\leq2$)  | $x_{0}=a,\:x_{1}=b$                         | $\hat{I}(f)=\frac{1}{2}(b-a)[f(a)+f(b)]$           | $\frac{-(b - a)^3}{12} \, f''(\xi)$      | 2                       |
| Simpson's (deg $\leq$ 3) | $(x_{0},f_{0}),(x_{1},f_{1}),(x_{2},f_{2})$ | $\hat{I}(f)=\frac{1}{6}(b-a)[f(a)+4f(x_{1})+f(b)]$ | $\frac{(b - a)^5}{2880} \, f^{(4)}(\xi)$ | 3                       |

#### [[The Newton-Cotes Rules]]

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
