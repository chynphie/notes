- Definition: A **pythagorean triple** is a triple $(a,b,c)$ of positive integers such that $a^{2}+b^{2}=x^{2}$,such a triple is primitive if $gcd(a,b,c)=1$
- Exercise: Let a, b, c be a Pythagorean triple. Prove that $3 | a, 3 | b, or\:3 | c$
	- Proof sketch:
		1. $(a,b,c)\text{ primitive }$
		$\implies(a+bi),(a-bi)\:coprime,\:(a+bi)=u(m+ni)^{2}$
		$\implies a=u(m^{2}-n^{2}),\:b=u(2mn)i$ <br>Since $2|b\implies\:U=\pm1\implies U=1$ check $gcd(m,n)=1$
		
		Converse, show $(m^{2}-n^{2})^{2}+2mn=(m^{2}+n^{2})^{2}\:$ and $gcd(m^{2}-n^{2},2mn,m^{2}+n^{2})=1$ 


*Example* question: How many elements of order 4 are there in $Z^{*}_{17}$?
1. Determine $\phi(17)=17-1=16$
2. Check if $4\:|\:16$: 
	- Yes $\implies$ there are exactly $\phi(4)=2^{2}-2=2$ elements in $Z_{17}^{*}$
	- No $\implies$ none
