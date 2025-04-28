- if ($X_{t}$) is a stochastic process
	- for fixed t, $X_{t}$ is a random vairable $X_{t}:\to\:R$
	- for a fixed 
## Brownian Motion
Most important model in MF, process continuous over time: $\{W_t, t > 0\}$
- **Properties**:
	1. $W_0 = 0$
	2. $\forall n \in \mathbb{N}, 0 < t_0 < t_1 < \dots < t_n < \infty$,  
	   the increments $W_{t_i} - W_{t_{i-1}}$ are independent.
	3. $\forall 0 \leq s \leq t$,  
	   $W_t - W_s \sim N(0, t-s)$, and $W_t \sim N(0,t)$.
	4. The sample paths $t \mapsto W_t(\omega)$ are continuous (no jumps).