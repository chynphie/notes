> [!definition] Group  is a pair $(G,\boxtimes)$ where 
> 1. G is a set
> 2. $\boxtimes$ is an associative binary operation  G such that 
> 	1. $\boxtimes$ has an identity e, and
> 	2. Every element $g\in G$ is invertible respect to $\boxtimes$

- **Order** of G is $|g|=min\{ k\geq1:g^{k}=e_{G}\}$ 
	- Ex: $|e|=1,\:|g|=1\iff g=e$
		- $In\:\mathbb{Z}^{+},\:|1|=\infty,\:k1=0\iff k=0$
		- in $\mathbb{Z}/n\mathbb{Z}$ under +, $|[1]|=n$ (the congruence class)
- Notation: let G be a. Group $g\in G$
	- $g^{n}=g\cdot g\cdot\cdot\cdot\cdot g,and\:\:g^{-n}=g^{-1}\cdot g^{-1}\cdot \cdot \cdot g^{-1}$ 
	- $g^{0}=e$  (identity)
- Prove: For any $m,n\in \mathbb{Z},(g^{m})^{n}=g^{mn}$, $g^{m}\cdot g^{n}=g^{m+n}$ 
- **Additive notation**: We write $g^{n}\:as\:ng=g+\dots+g$
	- but not nessarily the case the $(gh)^{n}=g^{n}h^{h}$ if operation is non abelian
- ==lemma(Properties of order)==: 
	1. If $g^{n}=e$, then $g^{n-1}g=e\implies g^{n-1}=g^{-1}$ . In particular if $|g|=n<+\infty$ then $g^{n-1}=g^{-1}$
	2. $g^{n}=e\iff(g^{n})^{-1}=e\:\iff(g^{-1})^{n}=e$ 
	- Ex: $-[1]=(n-1)[n]=[n-1]\:in\:\mathbb{Z}/n\mathbb{Z}$  