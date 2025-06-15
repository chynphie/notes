### Definitions
- *Lateness*: $L_{i}=C_{j}-d_{j}$, early -> negative, late -> positive
- *Tardiness* $T_{i}$= $max\{ 0,\:L_{i} \}$
- *Maximum Lateness* $L_{max}$: The maximum lateness, $L_{max}$, is defined as $max(L_1,...,L_n)$. It measures the worst violation of the due dates
- *Basic Single machine model*:
	1. Has a bijection between *job sequence* and *feasible schedules* $\implies\:\#\:of\:feasuble\:schedules=n!$
- *Flow time* $F_{j}=C_{j}-r_{j}=W_{j}+p_{j}$, 
	- $F_{[i]}\:=\sum_{j=1}^{i}P_{[i]}$   and $\sum_{i=1}^{n}F_{[i]}=F$ the total flow time
	- the completion time of job j - its release date = Amount of time job j spends in the system
	- *Minimize* F means to
		1. *Minimize* the average # of jobs in the system 
		2. *Minimize* $P_{[1]\leq}P_{[2]}\leq\dots\leq P_{[n]}$
		![[Deterministic Models-1747153775776.png|319x255]]
- Total weighted completion time: $\sum w_{j}(1-e^{rC_{j}})$
- In the basic single machine model, there is a *bijection* between job sequence and feasible schedules
	- Thus # of feasible schedules = $n!$

#### SPT Schedule

> [!definition] SPT (shortest process time)
> Process the jobs in increasing order of processing time.
> 

> [!theorem] Theorem 6 SPT Optimal
> - Objective : min $\sum C_{j}$, total flow-time
> In the basic single machine model, a feasible schedule is **optimal** for minimizing F <u>iff</u> it is an **SPT**(Shortest Processing Time first) schedule

#### Minimizing Weighted Flow time

- **Weighted Flow time**:
	- *Minimize*: $F_{w}:=\sum_{j=1}^{n}w_{j}F_{j}$
	- $\frac{P_{[1]}}{w_{[1]}}\leq\:\frac{P_{[2]}}{w_{[2]}}\leq\dots\leq \frac{P_{[n]}}{w_{[n]}}$ 

> [!definition] Regular Performance measure
> Satisfy that if we take two schedules $S, S'$ , and the completion times are such that $C_{j}^{S} \leq C_{j}^{S'} \forall\:j$, then the **objective value** of $S\leq S'$
- The perf. Meas. $\sum U_{j}$ is regular

> [!theorem] Optimality of 1/prmp/$\gamma$
> For any Scheduling instance in above format where $\gamma$ is a **regular performance measure**, then there exists a **nondelay** schedule which is **optimal**

> [!definition] Nondelay Schedule
> - Has no unforced idleness
> 	- forced idleness: no machine processes jobs at that time constant
> 	- unforced idleness: otherwise
 