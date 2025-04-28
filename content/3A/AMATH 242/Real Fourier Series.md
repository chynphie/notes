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
	>![[content/3A/AMATH 242/Pasted Photos/image-6.png|600|653x281]]
	![[content/3A/AMATH 242/Pasted Photos/image-7.png|600|690x363]]

	- Properties to determine $a_{k},b_{k}$: if $N=2\pi\text{ and }t\:\in[0,2\pi]$ then
		1. $∫_{0}^{2\pi}\cos(kt)\sin(kt)dt=0$
		2. $∫_{0}^{2\pi}\cos(kt)\cos(jt)dt=0\:if\:k\neq j$ 
		3. $∫_{0}^{2\pi}\sin(kt)\sin(kt)dt=0,\:j\neq k$
		4. $∫_{0}^{2\pi}\cos(kt)=∫_{0}^{2\pi}\sin(jt)dt=0$ 
- Function properties:
	1. $f(x)=f(-x)\implies \text{Even function}$
	2. $f(x)=-f(-x)\implies \text{odd function}$