> [!info] Bellman-Ford Algorithm
> Require: D = (N, A) directed graph, w ∈ ℜA, s ∈ N. 
> y (0) s = 0; y (0) u = ∞, pu = undef for all u ∈ N, u ̸= s 
> - for $i$= 1 to $|N| − 1$ 
> 	- do 
> 		- for all $v ∈ N$ (considered in any order) do 
> 			- $y_{v}^{(i)}$ = $min y_{v}^{(i-1)} , minu:uv∈A(y_{v}^{(i-1)} + w_{uv})$. 
> 			- If y (i) v < y(i−1) v then 
> 				- Let uv ∈ A be such that y (i) v = y (i−1) u + wuv 
> 				- pv = u 
> 			- end if 
> 		- end for 
> 	- End for 
> 	- If $y^{|N|-1}$ are feasible node potentials then 
> 		- return T = (N, {puu : u ∈ N \ {s}}) and y (|N|−1)
> 	- else
> 		- return D has a negative dicycle
> 	- end if
> 
> 

Example:
![[Bellman-Ford Algorithm-1750253650897.png|601x546]]
