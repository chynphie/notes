> [!definition] Bi-criteria Optimization: 
> - Minimize  $T_{max}$ first,
> - Minimize $F$ second
> - denoted as $1//Lex(T_{max},F)$

> [!info] Algorithm 22 Smith's Rule
> 1. Apply EDD algo, and compute $T_{max}^{*},\:P:=\sum_{i=1}^{n}p_{j},\:j=\{ 1,..,n \}$. Among all jobs $j\in J$ with $d\geq P-T_{max}^{*}$ find a job j s.t. $p_{k}$ is max. 
> 2. Schedule job k at the latest position $P:=P-p_{k},\:J:=J-\\\{ k \}$ 
> 3. Repeat until $J=\emptyset$ 
