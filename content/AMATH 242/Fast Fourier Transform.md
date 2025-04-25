- Algorithm
```
Fast Fourier Transform
	function F = FastFT(f, N)
		m = log N
		if m = 0
			F = f
		else
			build g[N]
			build h[N]
		F[even] = (1/2) FastFT(g, N/2)
		F[odd] = (1/2) FastFT(h, N/2)
	end
```
- Assume the factors $W_{N}^{kn}$ are precomputed and stored in a table
- use Formula directly to compute N coefficients $F[k]$. Amount of work is then $W=(N-1)A+(N+1)M=2N\:flops/coefficient\implies Total\:work\:is\:then\:N(2N)=2N^{2}$
- **Theorem 4.4**:
	- If $N=2^{m}$ for some integer m, then the length N DFT F[k] of discret Time signals f[n] can calculated by combining two length $\frac{N}{2}$ DFT. we define
		- $g[n]=f[n]+f\left[ n+\frac{N}{2} \right]$
		- $h[n]=\left( f[n]-f\left[ n+\frac{N}{2} \right] \right)W_{N}^{-n}$
		Then
		- $F[2l]=\frac{1}{2}DFT\{ g[n] \}$ (even indices)
		- $F[2l+1]=\frac{1}{2}DFT\{ h[n] \}$ (odd indices)
