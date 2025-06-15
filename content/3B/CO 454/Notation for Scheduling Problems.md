- $\alpha$ := {**machine environment**} 
	- $\alpha=\alpha_{1}\alpha_{2}$
		- where $\alpha_{1}\in \{ P,Q,R \}$
			- P = parallel identical machines
			- Q = uniform machines *e.g. Q4 means 4 uniform machines and perform all jobs but there a scale factor, which means Q can performs x times better than other machines*
			- R= unrelated machines
	- $\alpha_{2}\in Z_{++}\text{ \# of machiens}$
		- $\alpha_{1}\in \{ F,J,O \}$
			- F = flow shop *(e.g. Each jobs has 5 operations that has the same order)*
			- J = job shop *(e.g route for each job is given may be different for different jobs)*
			- O = open shop *no routes are specified* 
- $\beta:=\{ job\:characterization \},\:\beta=\beta_{1}\beta_{2}\beta_{3}\dots$
	- $\beta_{1}\in \{ prmp \},\:\beta_{1}=\emptyset\implies\text{no preemption is allowed}$
	- $\beta_{2}\in \{ prec,chain,\:tree,intree,outtree \},\beta=\emptyset\implies no\:precedence\:constraint$
	- $\beta_{3}=\{ r_{j} \},r_{j}=0,\forall j\in \{ 1,2,\dots,n \}$
	- $\beta_{4}\in \{m_{j}\leq m\},m_{j}:=\text{number of operations}$
	- ...
	- ...
	- ...
- $\gamma:\:\text{optimality criterion or optimality criteria}$
	- Typically, in single objective scheduling problems we have $\gamma \in \left\{  h_{max},h_{w},\sum_{}^{}h_{j}  \right\}$ where these are regular performance measures
	- e.g. $h_{max}\in \{ L_{max},\:T_{max},C_{max},\dots \}$
 
 %% > [!Lemma] Lemma 12 
> - In the problem 1/chain/$F_{W}$, consider a further constrained version where all jobs in the same chain must be processed contiguously. 
> - Further suppose that we have only two chains: 1,2,...,k and $k+1,k_{2},\dots,n$
> - **=>** Then the sequence 1,2,...,n yield an optimal schedule iff $$
> 	\frac{\sum_{j=1}^{k}w_{j}}{\sum_{j=1}^{k}p_{j}}\geq \frac{\sum_{j=k+1}^{n}w_{j}}{\sum_{j=k+1}^{n}p_{j}}$$

- *Proof sketch*: There are two feasible schedules fo rthis very restrictive shceduling problem. We compute the obj fn values of thisese tow feasible schedules and compare them. Note that equality

- <u>Chain-WSPT</u>: 
	- suppose we have f chains. Chain-WSPT rule shedules all jobs in the same chain contiguously and orders the chains in non-increasing order of the ratios: $$\frac{\sum_{j\in chain_{i}}^{}w_{j}}{\sum_{j\in chain_{i}}^{}p_{j}},\:i\in \{ 1,2,\dots,f \}$$
> [!proposition] Proposition 13 
> - Consider a further constrained version of 1/chain/$F_{w}$ such that all jobs in the same chain must be processed contiguously. 
> - **=>** Then, a feasible schedule is optimall iff the chains are ordered with respect to **Chain-WSPT** order. 
 %%