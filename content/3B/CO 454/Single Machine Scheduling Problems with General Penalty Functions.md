#### Minimizing maximum Penalty (1/prec/$h_{max}$)

> [!info] Algorithm 32:
> 0. Let J denote the set of unscheduled jobs with no unscheduled successors $P:=\sum_{j=1}^{n}p_{j}$
> 1. Pick Job $j\in J$ s.t. $h_{1}(P)=min_{j\in J}\{ h_{j}(P) \}$
> 2. Schedule job l at the latest available time slot (i.e. So that $c_{l}=p$)
> 3. Set $p:p-p_{l}$, update $J$, go to Step 1

The objective function is 
$$
\begin{align}
 & \text{min}\:\sum_{j=1}^{n}w_{j}T_{j}\\
 & s.t.\:T_{j}\geq p_{j}-d_{j}+\sum_{i=1}^{n}p_{j}x_{ij}\:\forall j\in \{ 1,2,\dots,n \}
\end{align}
$$

> [!theorem] Theorem 34
> For every instance of 1/1 Th  
E11/Zujtj for which every weight my is positive,  
every optimal solution of the integer programming  
-mem(IP-Th) yields an optimal schedule

Proof sketch:
- Let S be a feas. sched. For an arbitrary instance of $1//T_w$ then we set
$$
\bar{x}_{ij}=1\text{ if job i comes before job j in S},\:0\text{ if otherwise}
$$
$$
\bar{T}_{j}=max\left\{  0,p_{j}-d_{j}+\sum_{i=1,i\neq j}^{n}p_{j}\bar{x}_{ij}  \right\}\:\forall j\in \{ 1,2,\dots,n \}
$$
- Moreover, $\bar{T}_{j}=max\{ 0,C_{j}(S)-d_{j} \}=T_{j}(S)\forall j\in \{ 1,2,\dots,n \}$ therefore the obj. Val. Of this $(\bar{x},\bar{T})\:is\:\sum_{j=1}^{n}w_{j}\bar{T}_{j}=\sum_{j=1}^{n}w_{j}T_{j}(S)$ 
- We proved that for every feasible schedule S for $1//T_{w}$ there exists a feas. Soln $(\bar{x},\bar{T})$ of $(IP-T_{w})$ s.t. The obj. Val. Of $(\bar{x},\bar{T})$ of $(IP-T_{w})$ is the same as the obj. Val. Of schedule S in the problem $1//T_w$ 

- To finish the proof we will show that every optimal soln of $(IP-T_{w})$ corresponds to a feas. Sched. S for $1//T_w$ s.t. The obj. Val. Of the optimal soln of $(IP-T_w)$ and S are the same. 
- Note that $(IP,T_{w})$ always has optimal solutions
- In every opt. Sln ($\bar{x},\bar{T}$) of ($IP-T_{w}$), $\bar{T}_{j}=max\left\{  0,p_{j}-d_{j}+\sum_{i=1,j\neq i}^{n}p_{j}\bar{x})ij  \right\}\forall j\in \{ 1,2,\dots,n \}$
- $x^{\sim}:=x,\:T^{\sim}_{j}$ 
