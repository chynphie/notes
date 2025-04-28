- *Theorem 3.26 (for forbidden string)* : 
	- let $k \in \{0,1\}^*$ := nonempty string of length n,
	- let $A=A^k$ :=set of binary string that avoid $k$;  
	- Let $C$ be the set of all nonempty suffixes $\gamma$ of $\kappa$ such that $\kappa\gamma = \eta \kappa$ for some nonempty prefix $\eta$ of $k$. 
	- Let $C(x)=\sum_{\gamma\in C} x^{l(\gamma)}$  
	=> Then $A(x) = \frac {1+C(x)}{(1-2x)(1+C(x)) + x^n)}$  
- ==Forbidden strings:==

	1. 
		- let T := set of all binary strings avoiding $\alpha$
		- let S:= the set of all binary strings containing exactly one copy of $\alpha$ in the end
		- Appending a 0 or a 1 to a string in $T$ either gives another string in $T$ or a string in $B$. Conversely, a nonempty binary string in $S \bigcup T$  can be uniquely written as a string in $T$ where a 0 or a 1 is appended. Thus, we obtain $S(x) + T(x) = 1+2xS(x)$
	2. 
		- if $\alpha$ don't have overlap string => $T=S*\alpha$  
		- otherwise => $T \subseteq S*\alpha$ 
	3. Determine the unambiguous string $\beta$ => $S*\alpha = T*\{\epsilon \smile \beta\}$ and $S\smile T=\epsilon \smile S(0\smile1)$ 
- **Prefix** decompositions: 
	 - a set of binary string is a regular expression of the form *A\*B or A(B\*)* 
- **Recursive** decompositions: 