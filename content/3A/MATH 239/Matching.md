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
	![[content/3A/MATH 239/239PastedPhotos/image-6.png|745x228]]
- **Augmenting Path**: (consisted of alternating path, a path between $M$ and $\bar{M}$)
	![/content/3A/MATH 239/239PastedPhotos/image-7.png|598x222]
- ***Konig's Theorem:*** 
	- Conditions:
		1. Bipartite Graph
	- Then $|M| = |C|$, M is the maximum matching, otherwise $|M'|<|C|$ 
- ***Hall's Theorem***: 
	- Conditions:
		1. Bipartite Graph G = (A,B)
	- Then all vertices in |A| is saturated **if and only if $|N(D)|\geq|D|$**