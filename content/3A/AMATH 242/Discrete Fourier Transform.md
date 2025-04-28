- The **DFT of a discrete-time signal $f[n]$** with $0 \le n \le N-1$ is$$F[k] = \mathrm{DFT}\{f[n]\}= \sum_{n=0}^{N-1} f[n]\,W_N^{-kn},\quad0 \le k \le N-1.$$
- T**he inverse DFT is**$$f[n] = \mathrm{IDFT}\{F[k]\}= \sum_{k=0}^{N-1} F[k]\,W_N^{kn},\quad0 \le n \le N-1.$$

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

	![[content/3A/AMATH 242/Pasted Photos/image-4.png|800|432x119]]


	![[content/3A/AMATH 242/Pasted Photos/image-5.png|469x236]]
#### Complex Fourier series:
- $f(t)=\sum_{k=-\infty}^{\infty}c_{k}e^{ikt}dt$  with f(t) defined on $[-\pi,\pi]$ and
- $c_{k}=\frac{1}{2\pi}∫_{-\pi}^{\pi}f(t)e^{-ikt}dt=\frac{1}{2}(a_{k}-ib_{k})$ 
- The real an complex coefficients have the following properties
	1. $\bar{c_{k}}=c_{-k}$
	2. $a_{-k}=a_{k},b_{-k}=-b_{k}$
	3. $b_{0}=0,c_{0}=\frac{1}{2}a_{0}$
	4. $a_{k}=2\mathrm{Re}(c_{k}),\:b_{k}=-2Im(c_{k})$
	5. If f(t) is even, Im($c_{k}$) =0. f(t) odd, Re($c_{k}$)=0
![[image-1 2.png]]
