> [!theorem] THEOREM 2.20. 
> A digraph $D$ is **acyclic** if and only if it admits a topological ordering

> [!info] ALGORITHM. Topological Ordering. 
> - input: digraph D = (N, A). 
> - Output: if D has no dicycle then finds a topological ordering of the nodes. 
> 	- I := 1; 
> 	- **while** there is a node v with d(¯v) = 0 
> 		- do v gets label i; 
> 		- i := i + 1 delete v and all arcs with tail v 
> 	- **end while;**
> 	- if no nodes are left 
> 		- then output the ordering **$i_1, . . . , i_n$** 
> 	- else there exists a dicycle

