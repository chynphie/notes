- $|S_{n}|=n!$
- ==Proposition 1.15==: $S_{X}$ is a group under $\circ$ 
> [!proposition] Proposition 1.15
> $S_{X}$ is a group under $\circ$ 

- **symmetric/permutation group**: 
	- Let $n\geq1$. The symmetric (permutation) group $S_{n}$ is the group $S_{X}$ with $X=\{ 1,\dots,n \}$ 
- Representation: 
	1. Two-line rep: $\pi=\begin{pmatrix}1&2&3&4&5&6\\6&5&1&4&2&3\end{pmatrix}$
	2. One-line rep: $\pi=651423$
	3. Since $\pi(1)=6,\pi(6)=3,\pi(3)=1\implies(163)$ is a cycle of $\pi$. So $\pi=(163)(25)(4)=(163)(25)$ (typically drop cycles of len=1)
- Multiplication: 
	- s = rotate once to the right, $s^{2}$ = rotate twice to the right. Etc
	- $\pi\sigma=\begin{pmatrix}i\\column\:of\:\pi\:of\:\sigma\:at\:column\:i\end{pmatrix}$ 
- Inversion: 
	- rotate counterclockwise of the cycle.
- **fixed points** of a permutation $\pi \in S_{n}$ are the number $1\leq i\leq n$ s.t.$\pi(i)=i$
- **Support set** of $\pi \in S_{n}$ is $supp(\pi)=\{ 1\leq i\leq n :\pi(i)\neq i\}$, $\pi\:and\:\sigma$ are disjoint iff $supp(\pi)\cap supp(\sigma)=\emptyset$ 

> [!lemma] Lemma:
> If $\pi,\sigma \in S_{n}\:are$ disjoint, then $\pi\sigma=\sigma \pi$ 

