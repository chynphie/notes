 - Definition: 
	- $D=(N,A)$ consists a set of nodes N, and a set of arcs A that are ordered pairs of nodes. (ab $\neq$ ba)
- For **<u>arc</u>** uv, u = tail, v = head
- The **<u>out-degree</u>** of a node v is the number of arcs whose tail = v, denoted $d_{v}$
- The **<u>in-degree</u>** of a node v is the number of arcs whose head = v, denoted $d_{\bar{v}}$
- **A directed walk** (diwalk) is a sequence of nodes $v_{1},\dots,v_{k}$ such that $v_{i}v_{i+1}$ are arcs
- **A directed path** (dipath) is a *diwalk* where all nodes are distinct
- **A directed cycle** (dicycle) is a diwalk $v_{1},\dots,v_{k},v_{1}$ where $v_{1},\dots,v_{k}$ are distinct and $k\geq3$ 
	- ![[image-1.png|207x113]]
- The **node-arc incidence matrix** of a digraph D=(N,A) is an |N|x|A| matrix M such that
	- rows $\iff$ nodes of D
	- colomns $\iff$ arcs of D and
	- the entry for node v and arc ij, $m_{v,ij}$ is given by 
		- ![[Undirected and directed graphs-1746910995270.png |346|224x65]]

		- ![[Undirected and directed graphs-1746911014548.png|346|326x111]]
	
- **Cuts**: for $S\subseteq N$, the cut induced by S is the set of all arcs whose tails $\in\:S$, heads $\not\in S$. $\delta(S)=\{ uv\in A:u\in S,v\not\in S \},\:\delta(\bar{S})=\{ uv\in A,\:u\not\in S,v\in S \}$
	- ![[image-2.png|277x113]]
> [!theorem] Theorem 1.1:
> There exists an s,t-dipath **if and only if** every s,t-cut is non-empty
- Proof: 
	- (=>) Let $s=v_{1},v_{2},\dots,v_{k}=t$ be an s,t-dipath. Let $\delta(S)$ be an s,t-cut.  Since $v_{1}\in S,v_{k}\not\in S$, there exists a largest index i such that $v_{i}\in S\:and\:i<k$. Then $v_{i+1}\not\in S$. So $v_{i}v_{i+1}\in\delta(S)\:and\:\delta(S)\:is\:$non-empty.
	![[Undirected and directed graphs-1746891595702.png|215x145]]
	- (<=) Assume every s,t-cut is non-empty. Let S be the set of all nodes v such that an s,v-dipath exists. If $t\in S$, then an s,t-dipath exists, and we are done. Otherwise, $t\not\in S$ and $\delta(S)$ is an s,t-cut. By assumption there exists an arc $uv\in\delta(S)$. Since $u\in S$, there exists an $s,u$-dipath $P$. Then $P+uv$ is an $s,v$-dipath, so $v\in S$. This contradicts the fact that $v\not\in S$. 
		- ![[Undirected and directed graphs-1746891760890.png|423x116]]
- An example with no st-path:
	- ![[Directed graphs-1747315599519.png|336x163]]
- **Acyclic**: a digraph D that contains NO dicycle.
- **Reach**: For nodes s, v of digraph D, v can be reached from s if v=s or D has an sv-diwalk.
	- Set of nodes reachable from s = $\{ s \}\cup \{ v:D\:has\:sv\:diwalk \}$ 
- **Subdigraph** $D'=(N',A')$ : if $N'\subseteq N\:and\:A'\subseteq A$
- **Spanning subdigraph** $D'=(N',A')$: if $N'=N\:and\:A'\subseteq A$

> [!proposition] Proposition 1.4
> Let $Q$ be an st-diwalk.
>  - If $s = t$ then $Q$ can be decomposed into a collection of dicycles. 
>  - If $s\neq\:t$ then $Q$ can be decomposed into an st-dipath and a collection of dicycles.

> [!corollary] corollary 1.5
>  If there exists a $uv$-dipath and a $vw$-dipath, then there exists an $uw$-dipath.

> [!proposition ] proposition 1.6
> If every node of $D$ has in-degree at least one then $D$ has a directed cycle.

