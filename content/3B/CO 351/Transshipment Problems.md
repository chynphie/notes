- Given:
	1. A digraph D=(N,A)
	2. Node demands $d_{v}$ for each $v\in N$
		- Possitive => wants to get this units of goods
		- Negative => supplies this many units of goods
	3. Arc costs $w_{e}$ for each $e\in A$
- ![[Transshipment Problems-1747146335820.png|195x177]]
- **A Flow $x\in R_{+}^{A}$**: if $x\geq0$ and satisfies $Mx=b$
- **A node potential** $y\in \mathbb{R}^{N}$: 
	- feasible if $\bar{w}_{ij}\geq0$