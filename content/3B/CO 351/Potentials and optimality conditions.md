- The node potential y is feasible if $w_{uv}+y_{v}\geq y_{u}$
- Equality arc: if $w_{uv}+y_{u}= y_{v}$

All the statement below based on the conditions:
- Let D=(N,A)
- Q be an st-diwalk
- P be an st-dipath
- $y$ be a node potential
- $w\in \mathbb{R}^{A}$ be weights

> [!lemma] Lemma 2.3
> for a digraph satisfy the condition above, then **$w(Q)\geq y_{t}-y_{s}$** and **$w(Q)= y_{t}-y_{s}$** iff every arc of $Q$ are equality arc.

Proof idea: 
- List out all the inequalities of node potential y based on the arcs in Q, then sum up to cancel out some redundant var -> got result $y_{v_{k}} − y_{v_{1}} ≤ w(Q)$ 
- The equality satisfied **iff** when all the equalities on arc in Q $w_{uv}+y_{v}= y_{u}$ are satisfied 

> [!theorem] Theorem 2.4 (Optimality for the shortest dipath)
> P is the **shortest** st-dipath **if** $\exists$ feasible potential $y$ s.t. all arcs of P are equality arc

![[Potentials and optimality conditions-1749230735091.png|522x171]]
- Note, we are not able to find shortest st-dipath using feasible potential $y$ as they are not always feasible

> [!lemma] Lemma 2.5
> If D has a negative dicycle then D has no feasible potentials

> [!lemma] Lemma 2.6
> let all nodes in graph D be reachable from a node $s$, and for every $v\in N$, $y_{v}$ be the shortest path from s. 
> If $D$ has no negative dicycles then $y$ are feasible potentials 

Proof idea:

> [!theorem] Theorem 2.7 (Existence of feasible potentials)
> There exists feasible potentials if and only if there are no negative dicycles

Proof idea:

> [!theorem] Theorem 2.8 (Proving a dipath is shortest)
> Let $D = (N, A)$ be a digraph where all nodes are reachable from s, let $w ∈ ℜ^A$ be weights, and suppose D has no negative dicycles. 
> - If $P$ is a shortest $st$-dipath then there exists feasible potentials $y ∈ ℜ^N$ such that every arc of $P$ is an equality arc.

Proof idea: 
> 