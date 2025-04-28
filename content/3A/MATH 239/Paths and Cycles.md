- *Handshaking lemma:*  
	- $\sum_{v \in V} deg(V) = 2|E(G)|$
- *Theoreom 4.6.2*: 
	- $u$ to $v$ is a walk iff it is a path
- *Lemma*: 
	- let $u,v$ connected by a walk. Then for any vertices $w$ in $G$, there is a walk from u to w iff there is a walk from $v$ to $w$
- *Theorem 4.6*:
	- . If every vertex in G has degree at least 2, then G contains a cycle.
- *Theorem 4.8.2*: 
	- $G$ is connected if there is a *path* for each vertex w there's a path from $w, v$ 
- *Theorem*: 
	- In a connected graph $G=(V,E)$ with $|V|≥2$, there is a vertex $v$ such that $G-v$ is connected (v is an end vertex)
- *Theorem*: 
	- if a connected graph has n edges and m vertices, then $m \geq n-1$ *** read the proof again
- *Lemma*:
	- If $H_1$ , and $H_2$ are connected subgraphs of graph $G$ and $V(H_1) \bigcap V(H_2) ≠\emptyset$ then $V(H_1) \bigcup V(H_2)$ is connected.
- *Corollary 4.6.3* :
	- Let x,y,z be vertices of G. If there is a path from x-y and y-z then there's path x-z. 
- *Theorem 4.6.4:* 
	- If every vertex in G has degree ≥2, then G contains a cycle
- **Connected Graph** implies:
	1) There is a **path** between every pair of vertices. No vertex is isolated or unreachable
	2) The graph cannot be partitioned into two or more disjoint subgraphs.
- **Neighbor**:  
	- A vertex $v$ in a graph $G=(V,E)$, has a **neighbor** if it is connected to at least one other vertex by an edge. 
- **Planarity**:
	- A graph that does not have crossing edges; (to prove non-planarity: simply draw the vertices in a form of cycle and show it's impossible to have non-crossing edges)
	- iff each component is planar
- **Subgraph**:
	- $G \subseteq H$, more over, G is *spanning* if $V(G)=V(H)$
- **Multigraph**:
	- A *tuple* *(V,E,A)* V, E are a finite set. $A=(a_{ve})_{V \times E}$  is a matrix with entries of 0,1,2 s.t. each column sums up to 2.
 - **Connectivity**: $G$ is connected if all $v \in V$ are a walk
	 - iff it has one component
 - **Component**: A component of G is subgraph C of G such that
	a) C is connected
	b) No subgraph of G that properly contains C is connected

