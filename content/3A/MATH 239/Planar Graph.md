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
	![[content/3A/AMATH 242/Pasted Photos/image-8.png|483|538x62]]
	- The **boundary walk** of $F$ is a closed walk obtained by moving around the entire boundary.
	- $\text{deg}(F)=$ length of the boundary walk, i.e. $\leq girth(G)$
	![[content/3A/MATH 239/239PastedPhotos/image-5.png|504x208]]
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
