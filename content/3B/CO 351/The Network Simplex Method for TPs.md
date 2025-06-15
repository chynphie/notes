Assumptions:
1. $\sum_{v\in N}^{}b_{v}=0$
2. The digraph is connected, D contains at least one spanning tree
3. For all node pairs $i,j\text{ such that}\:ij\in A\implies ji\not\in A$

**Tree solution**:
- Given a spanning tree T of D, the unique solution x of $Mx=b$ s.t. $x_{ij}=0$ for all arcs ij not in T
**Flow**
- A vector $x\:\in R_{+}^{A}$ s.t. Mx=b
**Reduced cost**: 
- Given node potentials $y\in R^{N}$, the reduced cost of an arc ij w.r.t y is $\bar{w}_{ij}=w_{ij}+y_{i}-y_{j}$

> [!info] NSM Algorithm:
> 1. Calculate node potentials $y\in \mathbb{R}^{N}$ such that $\bar{w}_{ij}=0$ for any arc $ij$ in T (Note: there are $|N|-1$ arcs but $|N|$ values of y so 1 free variable. Set $y_{v}=0$ for some $v$)
> 2. Calculate $\bar{w}_{ij}$ for each arc $ij$ not in the tree
> 3. If every arc satisfies $\bar{w}_{ij}\geq0$, then STOP, solution is optimal
> 4. Otherwise there exists arc $uv$ where $\bar{w}_{uv}<0$. Then
> 	1. $T+uv$ contains a cycle C. Consider the direction of C where uv is a forward arc
> 	2. Pick arc $pg$ where $x_{pg}=min\{ x_{ij}:ij \text{ is a backward arc in }C\}$. Let $t\in x_{pg}$
> 	3. For any forward arc $ij$ in C, add t to $x_{ij}$. For any backward arc ij in C, subtract t from $x_{ij}$
> 	4. Replace T with $T+uv-pg$
> 	5. Go to step 1
