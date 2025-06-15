> [!info] Dijkstra's Algorithm
> - <u>input</u>: digraph D=(N,A) with arc costs $w_{a}\geq0$ and node s
> - <u>output</u>: finds a tree T of shortest dipaths rooted from s
> 1. $y_{u}=0,\forall u\in N$
> 	1. Let A' be the set of equality of arcs and let D'=(N,A')
> 	2. Let S be the set of nodes reachable from s in D′ . If S = N then go to step 2. 
> 	3. Increase uniformly the potential of each node in $\bar{S}$ until some arc in $A − A'$ (with tail in $S$ and head in $\bar{S}$) becomes an equality arc. Go to step 1. 
> 2. Let $T$ be any spanning tree rooted at s in $D'$

