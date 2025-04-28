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
		![[/MATH-239/239PastedPhotos/image-15.png|149x139]]This contradicts (1).

- **Edge contraction**:
	  $V := (V \setminus \{u,v\}) \cup \{z\}$
	  $E := \{h \in E \text{ if h is not incident to u or v}\} \cup \{x z \text{ where x is incident w/ u or v}\}$
