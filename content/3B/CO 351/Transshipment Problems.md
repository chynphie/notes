> [!theorem] Fundamental Theorem of Linear Programming:
> Let (P) denote an LP problem
> 1. Either (P) is *infeasible*, or it is *unbounded*, or it has an *optimal* solution. Moreover, suppose that (P) is in standard equality form and its constraints matrix has full rank
> 2. If (P) has a **feasible** solution, then it has a feasible solution that is basic.
> 3. If (P) has an **optimal** solution, then it has an optimal solution that is basic.

> [!theorem] Theorem 1.16:
> - Consider a $TP$ with $b(N) = 0$. 
> - Then the TP is **infeasible** iff there exists a set of nodes S such that $b(S) < 0$ and $δ(S) = ∅$ (i.e., there exists a node set $S$ with negative demand such that the cut with shore S is empty).

> [!theorem] Theorem 1.17:
> - A TP is unbounded iff it has a feasible solution and its digraph has a dicylce of negative cost.

 - Given:
	1. A digraph D=(N,A)
	2. Node demands $d_{v}$ for each $v\in N$
		3- Possitive => wants to get this units of goods
		- Negative => supplies this many units of goods
	3. Arc costs $w_{e}$ for each $e\in A$
- ![[Transshipment Problems-1747146335820.png|195x177]]

> [!definition] Flow
> 
>  **A Flow $x\in R_{+}^{A}$**: if $x\geq0$ and satisfies $Mx=b$

> [!definition] Node potential
> 
> 
> - **A node potential** $y\in \mathbb{R}^{N}$: 
> 	- feasible if $\bar{w}_{ij}\geq0$

