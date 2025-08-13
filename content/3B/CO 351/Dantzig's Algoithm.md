> [!info] Dantzig's Algoithm
> input: digraph D = (N, A) with costs w ∈ ℜA. 
> Output: if D has a negative dicycle, then finds one, otherwise, finds a **tree of shortest dipaths** rooted from s. 
> - Step 0: Find an initial spanning tree T rooted from s. 
> - Step 1: For every node u ∈ N let yu := w(Pu). 
> 	- Try to find a non-tree arc uv such that yv > yu + wuv. 
> 	- If no such arc exists, STOP 
> 		- T is a tree of shortest dipaths. 
> 	- If v is a node of Pu then stop, 
> 		- the unique dicycle in T + uv is negative. 
> 	- Let zv be the last arc of Pv. T := T + uv − zv 
> 	- Go to step 1

Example:
![[Dantzig's Algoithm-1750254623125.png|610x349]]