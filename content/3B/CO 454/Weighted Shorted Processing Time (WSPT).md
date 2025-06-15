- Sequence the jobs in decreasing order of process time to weight ratios

> [!theorem] Theorem 7
>- Let n be a positive integer and $w\in \mathbb{R}_{+}^{n}$ be given. Consider minimizing $F_{w}$ in the basic single machine model.
> - *Then* a feasible schedule is optimal *iff* it is a **WSPT** schedule

- ***Proof:*** 
		- By contradiction. Suppose a shedule $S$ that is not WSPT is optimal => there must be $\geq2$ adjacent jobs that has property $\frac{w_{j}}{p_{j}}<\frac{w_{k}}{p_{k}}$. 
		- Assume that job j starts processing time at t and the schedule looks like
		
	![[WSPT-1748743059933.png|387x191]]
		- Total weighted completion time of 
			- S = $(t+p_{j})w_{j}+(t+p_{j}+p_{k})w_{k}$
			- S' = $(t+p_{k})w_{k}+(t+p_{k}+p_{j})w_{j}$
		- if  $w_{j}/p_{j}\:<w_{k}/p_{k}$ total weighted completion time (S') < Total weighted completion time (S) since => contradicts the optimality of S. 

- **Schedule** processes after an entire chain

#### Precedence Constraints **Chain-WSPT** 

> [!lemma] Lemma 11
> - If $\frac{\sum_{j=1}^{k}w_{j}}{\sum_{j=1}^{k}p_{j}}\geq(\leq)\frac{\sum_{j=k+1}^{k}w_{j}}{\sum_{j=k+1}^{k}p_{j}}$ 
> - Then it is **optimal** to process the chain of jobs 1,...,k before (after) the chain of jobs k+1,..,n

Proof idea: using contradiction and compare all their weights

- Note: the equality holds iff both feasible schedules are optimal. 

> [!tip] Proving techniques
> Construct contradiction by using **Adjacent Sequence Interchange**, i.e. interchange between two adjacent chain of jobs
> 

> [!proposition] Proposition 13 
> - Consider a further constrained version of $1/Chain/F_{w}$ s.t. All jobs in the same chain must be processed contiguously.
> - Then, a feasible schedule is optimal **iff** the chains are ordered w.r.t Chain-WSPT order. 

Let $l^{*}\text{ be the largest index s.t. }\frac{\sum_{j=1}^{l^{*}}w_{j}}{\sum_{j=1}^{l^{*}}p_{j}}=max_{1\leq l\leq k}\frac{\sum_{j=1}^{l}w_{j}}{\sum_{j=1}^{l}p_{j}}$
- LHS = $p\:factor$ of chain $1,..,k$ denoted by $p(1,\dots,k)$ 

> [!lemma] Lemma 14
> If job $l^{*}$ determines $p(1,..,k)$, then $\exists$ an optimal sequence that process jobs $1,\dots,l^{*}$ one after another without any **interruption** by jobs from other chains.
- Proof idea: Build a contradiction on another optimal the schedule $S:=\{ 1,..,u,v,u+1,..,n \}$ where $v$ is the interruption schedule from another chain. Then by showing $S'=\{ 1,..,u,v \}$ and $S''=\{ v,u+1,..,n \}$ is optimal (has less weighted schedule) then $S$ complete the proof. 



> [!info] Algo. 16 for 1/Chain/$F_{w}$
> whenever m/c is free
> 1. Choose among the remaining chains with the largest $p-factor$
> 2. Process the jobs in this chain without interrumption up to and including the job determining the $p$ factor of that chain
> 3. Recompote the $p$ factor of the remaining jobs in that chain-> Repeat from 1

> [!example] 
> ![[WSPT-1748788865734.png|621x454]]



> [!definition]   <u>Definition 8:</u> 
> - A function $f:\mathbb{R}_{+}^{n}\to \mathbb{R}$ of the form $f(c_{1},c_{2},..,c_{n})$ involved in the objective function of a schedulling problme is a regular performance measure if
> 1.  The objective of the scheudling prob is $$min\:f(c_{1},c_{2},\dots,c_{n})$$ and 
> 2. For every pair of feasible schedules $S'$ and $S''$ with completion times $c_{1}',c_{2}',\dots,c_{n}'$ and $c_{1}'',c_{2}'',\dots,c_{n}''$ 
> 3. $c_{k}'\leq c_{j}''$ for every $j\in\:\{ 1,2,..,n \}$ implies $f(c1',c2',\dots,cn')\leq f(c1'',c2'',\dots,cn'')$

> [!definition] <u>Definition 9</u>:
> - Let D be a subset of feasible schedules. D is called a *dominant se*t for regular performance measures if for every feasible schedule S (with completion times c1,c2,..,cn), there exists a schedule $S'\in D$ (with completion times c1',c2',..,cn') such that $c_{j}'\leq c_{j},\:\forall j\in \{ 1,2,\dots,n \}$ 

> [!theorem]  Theorem 10</u>: 
> - In the basic single machine model, remove the assumption abt the idle time,
> - Then in this more general SM env, feas. Schedules without idle time consitute a dominant set

> [!theorem] ==Theorem 11:==
> - In the basic single machine model, remove the assumptions abt the **idle time** and **pre-emption**. 
> - Then in this more general single machine environment, feasible schedules without idle time and without pre-emption constitute a dominant set. 

**Proof Sketch:** 
- Let D denote the set of feasible schedules without **idle time** & **pre-emption**
- Let $\bar{S}$ be a feasible schedule that is not in the set D. 
- If $\bar{S}$ has some idle time, we can apply the steps described in the proof of [theorem 10] and arrive at a feasible schedule $S$ without idle time s.t. 
$$
C_{j}(S)\leq C_{j}(\bar{S} )\:\forall j\in \{ 1,2,\dots,n \}
$$
- If $S$ has no preemption, we are done. So we may assume some job(s) in S are pre-empted.
- Let $l$ be the last job to finish in $S$
	
	![[Weighted Shorted Processing Time _WSPT_-1749069914229.png|442x159]]
- That is, remove all the pieces of job l from the schedule S, shift all the jobs to left when possible. Then schedule job l as the last job in one piece, without creating any new idle time. Then argue that $$
C_{j}(S')\leq C_{j}(S),\:\forall \{ 1,2,\dots,n \}
$$ Then repeat the idea with the second last job to finish in S'. 


