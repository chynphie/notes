$1//U,\:\delta(C_{j})=1\text{ if }C_{j}>d_{j,}\:and\:=0\text{ otherwise}$ 

> [!proposition] Proposition 24: 
> If an EDD schedule S satisfies $U(S)\in \{ 0,1 \}$, then S is optimal for the underlying $1//U$ instance

> [!proposition] Proposition 25
> For every instance of $1\text{//}U$, there exists an optimal schedule $S^{*}$ s.t. $S^{*}=\{ A,B \}$ where every job in A is early or on-time and all jobs in B are tardy. 
> Moreover, the jobs in A are in EDD order and jobs in B are in any order. 
> We can convert every optimal schedule into the above form without changing the set of tardy jobs

> [!info] Algorithm 26:
> 1. Order jobs in EDD in $A$, set $B:=\emptyset$
> 2. Compute $T_{j}$ for every $j\in A$,
> 	1. If $T_{j}=0$->STOP (already optimal)
> 	2. Else, Let $l\in A$ be the largest processing time before the first tardy job in A (include tardy job itself)
> 3. Set $B:=B\cup \{ l \},\:A:=A-\{ l \}$  Go to step 2

> [!example] 
> ![[Minimizing the Total Number of Tardy Jobs-1749048896569.png|731x240]]

> [!lemma] Lemma 28
> Consider an instance of $1//U$
> Let k denote the first tardy job among all of the jobs that come before k in the EDD order, include job k in set J as well.
> Then, there exists an optimal schedule for this instance of $1//U$ in which a job $l\in J$ with $p_{l}=max_{j\in J}\{ p_{j} \}$ is tardy

Proof: 
![[Minimizing the Total Number of Tardy Jobs-1749048849351.png|876x327]]

> [!lemma] Lemma 29
> - Consider an instance of $1//U$ with n jobs s.t. Job $l$ is tardy in some optimal schedule S with partition $(A,B)$
> - Let $S'$ be an optimal schedule with partition $(A', B')$ for the instance with the same data except job $j$ and its data are removed. 
> - Then the schedule $S''$ identified by the partition $(A', B'\cup \{ l \}$ ) is also optimal for the original instance.

Proof: 
![[Minimizing the Total Number of Tardy Jobs-1749048834378.png|877x116]]

> [!theorem] Theorem 30:
> Algorithm 26 delivers the optimal schedule for every instance of 1//U


> 