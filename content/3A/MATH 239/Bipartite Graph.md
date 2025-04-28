- A graph is **bipartite**
	1. (A,B) has exactly one edge in a and one edge in B, expressed as $K_{m,n}$ (the graph can be non symmetric)
		
		![[/MATH 239/239PastedPhotos/image-16.png|100x111]]
	2. G and be seperated into exactly 2 set of vertex {A, B}
	3. If and only if each component is bipartite
	4. If it is 2 colourable
	5. ***Theorem 5.3.2.*** **if  and only if** it has no odd cycles. i.e. no odd length closed walk
- A **non-bipartite graph** contains at least one cycle of **odd** length.
- ***Theorem 7.5.6.***
	- In a bipartite planar graph G with $|V| \geq 3$ vertices and $|E|$ edges, we have $|E|\leq 2|V|-4$
- ***Theorem 7.7.2***: G is 2-colourable if and only if G is bipartite 
	
	![[/MATH-239/239PastedPhotos/image-14.png|98x79]]
- ***Theorem***:
	- Every regular-bipartite graph has a **perfect matching**
- ***Corollary 8.6.1:*** 
	- A bipartite graph with bipartition A,B has perfect matching **iff** $|A|=|B|$ and for all subset $X\:of\: A\:s.t.|N(X)|>|X|$
- ***Corollary***:
	- For $k\geq1$ every k-regular bipartite graph has a **Perfect Matching**
- ***Corollary***:
	- Every bipartite graph with max **degree k** has an edge **k-colouring**