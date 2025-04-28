- ***Proposition 2.4:***
	- Let $n$ be a positive integer and $a, b \in \mathbb{Z}$. Then $a \equiv b \pmod{n}$ if and only if $a$ and $b$ have the same remainder when divided by $n$.
- ***Proposition 26***
	- Let $n$ be a positive integer. If $[a] = [a']$ and $[b] = [b']$, then $[a] + [b] = [a'] + [b']$ and $[a][b] = [a'][b']$
	- *Proof.*
	If $[a] = [a']$ and $[b] = [b']$, then $n \mid a - a'$ and $n \mid b - b'$. Then $n \mid (a - a') + (b - b')$ so $n \mid (a + b) - (a' + b')$. Thus, $[a + b] = [a' + b']$.  For multiplication, we have $a = a' + kn$ and $b = b' + tn$ for some $k, t \in \mathbb{Z}$. Then:  $ab = (a' + kn)(b' + tn) = a'b' + n(kb' + ta' + nkt)$ so $[ab] = [a'b']$. 
- ***Proposition 27***
	-  Let $f(x) = a_n x^n + \cdots + a_1 x + a_0$ be a polynomial with integer coefficients, and let $n$ be a positive integer. If $[b] = [c]$ in $\mathbb{Z}_n$, then $[a_n][b]^n + \cdots + [a_1][b] + [a_0] = [a_n][c]^n + \cdots + [a_1][c] + [a_0]$ in $\mathbb{Z}_n$
- ***Lemma 28***
	- Let $m$ and $n$ be positive coprime integers. Then $a \equiv b \pmod{mn}$ if and only if $a \equiv b \pmod{n}$ and $a \equiv b \pmod{m}$.
	- Proof:
	    Suppose $a \equiv b \pmod{mn}$. Then $mn \mid a - b$ and since $m \mid mn$ and $n \mid mn$, we have $m \mid a - b$ and $n \mid a - b$.  
	    Conversely, suppose $a \equiv b \pmod{m}$ and $a \equiv b \pmod{n}$, so:
	    $mk = a - b$ and $nt = a - b$ for some $k, t \in \mathbb{Z}$.
	    Since $\gcd(n, m) = 1$, there exist $u, v \in \mathbb{Z}$ such that $mu + nv = 1$.  
	    Multiplying both sides by $a - b$ gives:   $$(a - b)mu + (a - b)nv = a - b \\
	    \Rightarrow (nt)mu + (mk)nv = a - b \\
	    \Rightarrow nm(tu + kv) = a - b$$Therefore, $a \equiv b \pmod{mn}$, completing the proof.