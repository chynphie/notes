# Graph theories:
[[ Paths and Cycles]]
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

## Eulerian Circuits:
- *Theorem 4.9.2*:
	- Let G be a connected graph. Then G has a Eulerian circuit **iff** every **vertex has even degree**
	- Eulerian trail exists iff there are **at most 2 odd degree**
- An **Eulurian circuit** of a graph G is a **closed walk** that contains every edge of G exactly once.
- An **Eulerian Trail** in a graph is a walk that traverses every edge in a graph exactly once 
	- guarantees connectivity and exactly two vertices with odd degrees.
## Bridges:
- *Lemma 4.10.2:* 
	- If e = {x, y} is a bridge of a connected graph G, then G - e has precisely two components; furthermore, x and y are in different components
-  *Theorem 4.10.3:*
	- An edge e is a bridge of a graph G iff it is not contained in any cycle of G
- *Corollary 4.10.4:*
	- If there are 2 distinct path from vertex u to vertex v in G then G contains a cycle
- an edge e of G is a **bridge** if G-e has more components than G
## Trees
- ***Lemma 5.1.3***: 
	- If $u,v \in T$ where T is tree, then $uv$ is a unique path
- ***Lemma 5.1.4***:
	- Every edge of a tree T is a bridge
-  ***Theorem 5.1.5***:
	- If T is a tree, then $|E(T)| = |V(T)|-1$
- ***Corollary 5.1.6**:*
	- If G is a forest with k components, then $|E (G)| = |V (G)|-k.$
- ***Theorem 5.1.8**:*
	- A tree with at least two vertices has at least two leaves.
- ==Definitions:==
	- A **tree** is a connected graph with no cycles
	- A **forest** is a graph with no cycles 
	- A **leaf** in a tree is a vertex of degree 1
#### Spanning trees
- ***Theorem 5.2.1***: 
	- A graph G is connected iff it has a spanning tree
- ***Corollary 5.2.2***: 
	- If G is connected with p vertices and $q=p-1$ edges, then G is a tree
- ***Theorem 5.2.3*:** 
	- If T is a spanning tree of G and e is an edge in T, then $T-e$ has 2 components. If e' is in the cut induced by one of the components, then $T+e-e'$ is also a spanning tree of G.
- ***Theorem 5.2.4.***
	- If T is a spanning tree of G and e is an edge in T , then $T-e$ has 2 components. If e 0 is in the cut induced by one of the components, then $T-e+f$ is also a spanning tree of G
- A **spanning tree** is a subgraph $H$ of $G$ that is a tree and $V(H)=V(G)$.  
#### Leaves of a Tree
- A **leaf** is a vertex of degree 1.  
- A tree with at least two vertices has at least **two leaves**.  
- Since $\sum_{v\in V}\text{deg}(v)-2=2$.

<div style="page-break-after: always;"></div>

## Bipartite Graph 
- A graph is **bipartite**
	1. (A,B) has exactly one edge in a and one edge in B, expressed as $K_{m,n}$ (the graph can be non symmetric)
		![[image-16.png|100x111]]
	2. G and be seperated into exactly 2 set of vertex {A, B}
	3. If and only if each component is bipartite
	4. If it is 2 colourable
	5. ***Theorem 5.3.2.*** **if  and only if** it has no odd cycles. i.e. no odd length closed walk
- A **non-bipartite graph** contains at least one cycle of **odd** length.
- ***Theorem 7.5.6.***
	- In a bipartite planar graph G with $|V| \geq 3$ vertices and $|E|$ edges, we have $|E|\leq 2|V|-4$
- ***Theorem 7.7.2***: G is 2-colourable if and only if G is bipartite 
	
	![[image-14.png|98x79]]
- ***Theorem***:
	- Every regular-bipartite graph has a **perfect matching**
- ***Corollary 8.6.1:*** 
	- A bipartite graph with bipartition A,B has perfect matching **iff** $|A|=|B|$ and for all subset $X\:of\: A\:s.t.|N(X)|>|X|$
- ***Corollary***:
	- For $k\geq1$ every k-regular bipartite graph has a **Perfect Matching**
- ***Corollary***:
	- Every bipartite graph with max **degree k** has an edge **k-colouring**
## Planar Graph
A **planar graph** is a graph that can be embedded in the plane without edges crossing.
- Proving non-planarity
	1. show it does not satisfy ***Planar face degree constraint***
	2. $deg(v)\leq5$

- **Planar Embedding Properties:**
		1. No two vertices are inside the same region.
		2. Edges only intersect at vertices.
- **Degree of a Face:**
	- The **degree of a face** is the length of its boundary walk, including edges and bridges.
	- Edges and vertices are **incident** with the faces they touch.
	- Two faces are **adjacent** if they share an edge.
	- The **boundary of a face** $F$ is the subgraph of $G$ consisting of edges and vertices incident with $F$.
	![[AMATH 242/Pasted Photos/image-8.png|483|538x62]]
	- The **boundary walk** of $F$ is a closed walk obtained by moving around the entire boundary.
	- $\text{deg}(F)=$ length of the boundary walk, i.e. $\leq girth(G)$
	![[MATH 239/Untitled/image-5.png|504x208]]
- ***Faceshaking Lemma:***
	For a **planar embedding** $G=(V,E)$: $\sum_{f\in Faces(G)}\text{deg}(F)=2|E|$
- ***Planar face degree constraint***: $|E|\leq \frac{d^{*}}{d^{*}-2}(|V|-2)$
-  ***Euler’s Formula:***
	- For a planar graph $G=(V,E)$: 
		- $v-e+f=c+1=2$
- ***Average degree of G***: $\frac{\sum_{v\in V}deg(v)}{|V|}=\frac{2|E|}{|V|}\leq\frac{4(|V|-2)}{|V|}\:if\:bipartite\:or\:\leq\frac{6(|V|-3)}{|V|}\:otherwise$
- The **boundary of each face** contains a cycle.
- ***Theorem 7.5.2***: 
	- If G = (V , E ) is a planar embedding whose faces all have degree at least $d≤3$, Then 
- ***Theorem 7.5.3:***
	- If all faces have **degree $\geq3$**, then $|E|\leq3|V|-6$
- Maximum **degree constraints**:
	- $\text{deg}(v)\leq5$ or $\text{deg}(f)\leq2$ (prove it by assuming $deg(f)>3$, then there's a $deg(v)>6$)
	- $deg(v)\leq 3 \text{ or } deg(f)\leq 3$ (prove it by assuming $deg(f)>4$, then there's a $deg(v)>4$)
	- For a **planar graph** with $|V|=3$, edges satisfy certain inequalities.
- ***Edge Subdivision***
	- Replacing an **edge** with a path of **length ≥ 1** is called **edge subdivision**.
- ***Kuratowski’s Theorem***
	- A graph is **non-planar** **iff** it contains a subgraph that is an **edge subdivision** of $K_5$ or $K_{3,3}$.
- A **planar subdivision** remains planar.

## Colouring 
- ***Proposition***: 
	1. Every **nonempty planar** has a vertex $degree\leq5$
	2. Every **Planar** embedding has a **vertex degree at most 5** or a **face of degree at most 2**
	3. Every **Planar** embedding has a **vertex degree at most 3** or a **face of degree at most 3**
- *Template* for minimal-counterexample assumption:
	- "Assume for contradiction that some graph G is a counterexample of minimum size. In other words"
		1. G itself fails the property we want, and
		2. every strictly smaller graph **does** satisfy the property.”
		Then found a subgraph H = G-v has less vertices that satisfy 2, and try to extend H to G but realizing that it contradicts the fact in 1.
- ***Six-colour theorem***: Every planar is 6-colourable
	- **Proof**: 
		Suppose otherwise and consider a counterexample $G=(V,E)$ with $|V|$ minimum.
		Then:
		1. $G$ is planar but not 6-colourable and
		2. Every planar graph with fewer vertices is 6-colourable
		
		By above prop. $G$ has a vertex $V$ with $deg(V)\leq5$ By (2) $H\:=G-v$ has a 6-colouring
		The neighbours of $v$ has at most 5 of the 6 available colours, so the colouring of $H$ can be extended to 6-colouring of $G$
		![[image-15.png|149x139]]This contradicts (1).

- **Edge contraction**:
	  $V := (V \setminus \{u,v\}) \cup \{z\}$
	  $E := \{h \in E \text{ if h is not incident to u or v}\} \cup \{x z \text{ where x is incident w/ u or v}\}$

<div style="page-break-after: always;"></div>

## Matching
- **M** := A set of matched edges no two of which are incident with a common vertex
- **C** := the cover is a set of vertices that incident to all the edges in graph G
- **M-saturated** if a vertex is incident with an edge in M and **M-exposed** otherwise
- M is **Perfect** if all vertices are M-saturated.
- **(un)saturated vertex**: A vertex is in (not) the matching M
- Facts:
	-  The union of two matching $M\cup M'$ in graph G is a combination of **edges** and **cycles**
- ***Theorem*** : 
	- M is not maximum matching if and only if there exist an augmenting path
	Proof:
	![[MATH 239/Untitled/image-6.png|745x228]]
- **Augmenting Path**: (consisted of alternating path, a path between $M$ and $\bar{M}$)
	![[MATH 239/Untitled/image-7.png|598x222]]
- ***Konig's Theorem:*** 
	- Conditions:
		1. Bipartite Graph
	- Then $|M| = |C|$, M is the maximum matching, otherwise $|M'|<|C|$ 
- ***Hall's Theorem***: 
	- Conditions:
		1. Bipartite Graph G = (A,B)
	- Then all vertices in |A| is saturated **if and only if $|N(D)|\geq|D|$**
## Bipartite Matching Algorithm

![[image-17.png|589x159]]
![[image-18.png|591x113]]

- Example:
	![[image-19.png|344x159]]
	1. draw a graph that start with unsaturated vertex in X, and connects its neighbours in Y
	2. connected the vertex of neighbours in Y that is a matching in A
	3. repeat the process and will find an augmented path
	4. after finding the augmented path and make sure no other augmented path exists, we are able to find the $C=A\setminus\\X\cup\:Y$ where $|C|=|M|$ 

<div style="page-break-after: always;"></div>

# Enumeration Methods:

## Basic Principles of Enumeration:
- *Binomial Theorem*: For any natural Number $n\in N$ $(1+x)^n = \sum_{k=0}^n {n \choose k} x^k$ 
- *Negative Binomial Theorem:* 
- *Theorem 1.2*. 
	- For every n  1, the number of lists of an n-element set S is n(n -1)(n -2) · · · 3 · 2 · 1.
- *Theorem 1.3*. 
	- For every n  0, the number of subsets of an n-element set is 2 n .
- *Theorem 1.4*. 
	- For n, k  0, the number of partial lists of length k of an n-element set is n(n  1) · · · (n  k + 2)(n  k + 1).
- *Theorem 1.5.* 
	- For $0 \leq k \leq n$, the number of k-element subsets of an n-element set is ${n\choose k} = \frac {n!}{k!(n  k)!}$.
- *Theorem 1.9*. 
	- For any $n\geq0$ and $t \geq 1$, the number of n-element multisets with elements of t types is ${n+t-1 \choose t-1}$
- **Multisets**: 
	- Let n  0 and t  1 be integers. A multiset of size n with elements of t types is a sequence of nonnegative integers $(m_1 , ..., m _t)$ such that $m 1 + m 2 + · · · + m t = n$
 - **Bijective Proofs** ( $\forall a \in A$ ( $\forall b \in B$ ) has a unique representation in $B$ ($A$) )
	- a) Find relationship of the two sets
	- b) create a mapping function such that $f(a)=b$ and $g(b)=a$ where $a \in A$ and $b \in B$ => $|A| = |B|$
## The Idea of Generating Series:
- *Theorem 3.26 (for forbidden string)* : 
	- let $k \in \{0,1\}^*$ := nonempty string of length n,
	- let $A=A^k$ :=set of binary string that avoid $k$;  
	- Let $C$ be the set of all nonempty suffixes $\gamma$ of $\kappa$ such that $\kappa\gamma = \eta \kappa$ for some nonempty prefix $\eta$ of $k$. 
	- Let $C(x)=\sum_{\gamma\in C} x^{l(\gamma)}$  
	=> Then $A(x) = \frac {1+C(x)}{(1-2x)(1+C(x)) + x^n)}$  
- ==Forbidden strings:==

	1. 
		- let T := set of all binary strings avoiding $\alpha$
		- let S:= the set of all binary strings containing exactly one copy of $\alpha$ in the end
		- Appending a 0 or a 1 to a string in $T$ either gives another string in $T$ or a string in $B$. Conversely, a nonempty binary string in $S \bigcup T$  can be uniquely written as a string in $T$ where a 0 or a 1 is appended. Thus, we obtain $S(x) + T(x) = 1+2xS(x)$
	2. 
		- if $\alpha$ don't have overlap string => $T=S*\alpha$  
		- otherwise => $T \subseteq S*\alpha$ 
	3. Determine the unambiguous string $\beta$ => $S*\alpha = T*\{\epsilon \smile \beta\}$ and $S\smile T=\epsilon \smile S(0\smile1)$ 
- **Prefix** decompositions: 
	 - a set of binary string is a regular expression of the form *A\*B or A(B\*)* 
- **Recursive** decompositions: 
##  Binary Strings and Recurrence Relations: 
- Step:
	1) write out the recurrence relation in terms of $\sum a_nx^n = \sum a_{n-1}x^{n-1} + \sum a_{n-2}x^{n-2}+...+\sum a_{n-k}x^{n-k}$ 
	2) $A(x)-a_0-a_1x-a_2x^2-...-a_kx^k =$ plug in the initial values given for $a_0, a_1,...,a_k$ 
	3) solve for $A(x)$
- *Proposition 4.22:*
	$\sqrt {(1-4x)} =1-2\sum_{k-1}^\infty \frac {1}{k} {2k-2 \choose k-1} x^k$
- *Theorem 4.21*
- **Catalan Numbers**: $C_n=\frac {1}{n+1}{2n\choose n}$ 

## Formal Power Series
- *Theorem 3.1:*
	- The inverse of a formal power series A(x) exists if and only if A(0) 6 = 0. Moreover, if the inverse exists, then it is unique.
- *Theorem 3.2:*
	- Let A(x) and B(x) be formal power series. If B(0) = 0, then A(B(x)) is a well-defined formal power series
-  *Theorem 4.1.* 
	- If A(x) is a formal power series such that A(x)2 = 1 + x, then A(x) is not rational
- *Theorem 4.2.*
	- If A(x) is a rational formal power series and A(x)2 is a polynomial, then A(x) is itself a polynomial



