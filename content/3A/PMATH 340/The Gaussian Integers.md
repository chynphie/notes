- Integer $n$ is a **sum of two squares** $\iff$ n is the area of lattice square
- ***Proposition 59***:
	- Let $z,w\in \mathbb{Z}[i].$ Then
		1. $N(z)=0 \iff z=0$
		2. $N(zw)=N(z)N(w)$
- ***Proposition 60***: 
	- $\text{The group of units in the Gaussian integers is }\mathbb{Z}[i]^{*}=\{ 1,-1,i,-i \}$
- ***Theorem 61 (the division algorithm for the Gaussian integers)***:
	- $\text{Let }z,w\in \mathbb{Z}[i]\text{ with }w\neq0 \text{ Then there exists }q,r\in \mathbb{Z}[i]\text{ so that }z=qw+r\text{ and }N(r)<N(w)$
	Example: find gcd for $1+3i,2$ (use the large number on the LHS) $1+3i = 2i+(1+i), 2=(2+i)(1-i)+0$  the remainder becomes 0 => terminates
- ***Theorem 62 (Bezout's identity in the Gaussian integers)***
	- $Let\:z,w\in \mathbb{Z}[i],\:not\:both\:zero,\:and\:let\:d\:be\:a\:gcd\:of\:z\:and\:w\text{, Then there exist}\:u,v\in \mathbb{Z}[i]\:satifying\:d=zu+wu$
- ***Corrollary***: 
	- $\text{If } gcd(v_{0},\delta)=d, \text{ then }\{uw+vz: u_{0}v\in \mathbb{Z}[i]\}=\{ da:a\in \mathbb{Z}[i]\}$
- Let $z,w \in \mathbb{Z}[i]$, $z,w$ are **associates** if $z = w u$ with $u \in \mathbb{Z}[i]^*$ s.t. $z=wu$
- **Gaussian integers**:
	- $\mathbb{Z}[i] = \{a+bi \mid a,b \in \mathbb{Z} \}$
- **Complex conjugate** of $z = a+bi$: 
	- $\overline{z} = a - bi$
- $N(z) = z\overline{z} = a^2 + b^2$ is the **norm** of $z$

#### [[Greatest Common Divisors]]
- **Definition**: Let $w,z \in \mathbb{Z}[i]$ with $w, z \neq 0$. The $\gcd (w,z)$ is a **common divisor** of $\mathbb{Z}[i]$ of **maximum norm**.$\gcd(3+4i, 1+i) = \gcd(25,2) = 1 \Rightarrow d=1$
#### [[Gaussian Primes]]
- Let $\pi$ be a **Gaussian Integer** that is not a unit.  $\pi$ is a **Gaussian prime** if $z \mid \pi \Rightarrow z \in \mathbb{Z}[i]^{*}$ or $z$ is an **associate** of $\pi$. 
	- Example: $z = 1+i$, $N(z) = 2$. Suppose $z \mid w \Rightarrow N(z) \mid N(w) \Rightarrow N(z) = 1$ or $2$.  
		1. $N(z) > 1 \Rightarrow z$ is a unit  
		2. $N(z) > 2 \Rightarrow z \in \{ 1+i, i-1, -1+i, -i-1 \}$ which are **associates** of $z$  
		Thus, $z$ is **prime**!  
	- Example: $z = 2+i$, $N(z) = 5$. If $z \mid w \Rightarrow N(z) \mid N(w)$,  
		- $N(z) \mid 5$, so  
		- $N(w) = 1$ or $5$  
		- Need to check:  Associate if $zw = 7w$ and $w$ is:  $N(z)N(w) = N(zw)$ , $5N(w) = 5$ $\Rightarrow N(w) = 1, w \in \mathbb{Z}[i]^*$
		- **All satisfied**, so $z$ is **prime**  

- ***Proposition 66***  
	- If $z \in \mathbb{Z}[i]$ be s.t. $N(z)$ is **prime** in the integers, then $z$ is a **Gaussian prime**.  
	- **Proof**:  
			$N(z)$ is **prime**, find $w \in \mathbb{Z}$ . Suppose $w \mid z \Rightarrow N(w) \mid N(z)$, $N(w) = k N(z)$ . If **prime** $\Rightarrow N(w) = N(z)$ and $k=1$ $\Rightarrow$ $z$ is a **Gaussian prime**  
	- Note:
		- If p is an integer prime
			- 2 is not a Gaussain prime
			- $p\equiv{1}(mod\hspace{4px}{4})$ is not
			- **$p\equiv3(mod\hspace{4px}{4})$ is a Gaussian Prime**
- ***Theorem 2 (Euclid’s Lemma for Gaussian Primes)***  
	Let $π$ be a **Gaussian prime**, and suppose $π \mid z_1z_2$ for some $z_i \in \mathbb{Z}[i]$.  
	Then $π \mid z_1$ or $π \mid z_2$.  or more generally
	If $π \mid z_1z_2...z_k$, then $π \mid z_j$ for some $j$.  
- ***Fermat's Christmas Theorem***: 
	- Let $p$ be an odd integer prime. Then $p=a^{2}+b^{2}$ iff $p \equiv 1(mod \hspace{4px} 4)$
	- Proof: 
		Since $p$ is odd, $p\equiv1$ or $3\pmod{4}$. Suppose $p\equiv1$, then $-1\in\mathbb{Z}_p^*$ is a square, So $p\mid k^2+1$, $k\in\mathbb{Z}$  $\Rightarrow p\mid(k+i)(k-i)$, however $p\nmid k+i$ since $\frac{k+i}{p}= \frac{k}{p} \pm \frac{i}{p} \notin \mathbb{Z}[i]$ Then $p$ is not a Gaussian prime. $\Rightarrow \exists z\in\mathbb{Z}[i]$ s.t. $z\mid p$ and $1<N(z)<N(p)$  Since $z\mid p$ and $N(z)\mid N(p)=p^2$, so $N(z)=p$ Let $z=a+bi$, then $p=a^2+b^2$.
- Example: Prove if
- ***Proposition 69***: 
	- $Let\:a\in \mathbb{Z}_{\geq0},\:Then\:a\:\in \mathbb{Z}[i]\:is\:a\:Gaussian\:Prime\:\iff\:a\equiv3(mod\:4)$
- ***Theorem 70***: $Let\:\pi\:be\:a\:Gaussian\:prime,\:then\:\pi\:is\:either$
	- $an\:associate\:of\:1+i$
	- $an\:associate\:of\:an\:int eger\:prime\:p\:where\:p\equiv3(mod\:4)$
	- $N(\pi)=p\:where\:p\:is\:an\:integer\:prime\:such\:that\:p\equiv1(mod\:4)$ 
- ***Theorem 71***: 
	- Let p be an odd (integer) prime. Then the following are equivalent.  
		- $p ≡ 1 (mod\:4).$  
		- $p = a^2 + b^2 for\:some\:a,\:b\:\in \mathbb{Z}$  
		- $[−1]$ is a square in $\mathbb{Z}^{*}$  

 p is not a Gaussian prime
- ***Theorem 72****: 
	- Let $n\in \mathbb{Z}_{>0}\text{ be such that }n=2^{v}\prod p_{i}^{e_{i}}\prod q_{i}^{f_{i}}$ where $p_{i}\equiv1\:(mod\:4)\:and\:q_{i}\equiv3\:(mod\:4)$, then n is the sum of two squares iff every $f_{i}$ is even. 
		Eg: $n=k^{2}m,\text{where m has no square divisors }n=3^{3}5^{2}7=(2\cdot5)^{2}(3\cdot7)\:\text{m is a perfect square}$
	- **Proof**: 
		$(=>)\:let\:n=a^{2}+b^{2},\:write\:n=k^{2}m$ where m is square free. 
		We want to show that if $p|m\:\text{is a prime divisor, then }p\equiv1(mod\:4)$
		let d=gcd(a,b). Then $\frac{n}{d^{2}}=\left( \frac{a}{d} \right)^{2}+\left( \frac{b}{d} \right)^{2}\in \mathbb{Z}$
		$\implies d^{2}|n=k^{2}m$. Since m is square free, $d^{2}|k^{2}$, write $\frac{d^{2}t}{d^{2}}=\left( \frac{a}{d} \right)^{2}+\left( \frac{b}{d} \right)^{2}$
		$\implies\:lm=x^{2}+y^{2},x=\frac{a}{d},\:y=\frac{b}{d},gcd(x,y)=1$  
		let $p|m,\:p\neq2\in\:\mathbb{Z}_{p},\:[0]=[x]^{2}+[y]^{2},\:$ note $[x]=[0]\iff[y]=[0]$ 
		If $[x]=[0],\:then\:p|x\:\&\:p|y,$ which cannot happen since gcd(x,y)=1.
		So $[x]\neq[0],\:\&[x]^{-1}$ exists. Then $-[x]^{2}=[y]^{2}\implies[-1]=([y][x]^{-1})^{2}$ in $\mathbb{Z}_{p},$
		Since $[-1]$ is a square, $p\equiv1(mod\:4)$
#### [[Pythagorean triples]]
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
