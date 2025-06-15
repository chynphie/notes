
Recall that $\mathbb{Z}/n\mathbb{Z}$ is a group under “addition mod $n$”:  
$$
(a + n\mathbb{Z}) + (b + n\mathbb{Z}) \;=\; (a + b) + n\mathbb{Z}.
$$

>**Question:**  Given $H \le G$, how can we make $G/H$ into a group using the operation from $G$?

If $S,T \subseteq G$, define 
$$
S\,T \;:=\; \{\,s\,t : s \in S,\; t \in T\,\}.
$$

---

>[!lemma]  **Lemma 4.**  
> 1. If $H \le G$, then $H\,H = H$.  
> 2. If $N \triangleleft G$, then for any cosets $gN$ and $hN$, one has 
>    $$
>    (gN)\,(hN) \;=\; (gh)\,N.
>    $$

**Proof:**  
1. If $H \le G$, then $H\,H = \{\,h_1\,h_2 : h_1,h_2 \in H\} = H$, since $H$ is closed under multiplication.  
2. If $N \triangleleft G$, then $gN\,hN = \{\,g\,n_1\;h\,n_2 : n_1,n_2\in N\} = \{\,g\,h\,(h^{-1}n_1 h)\,n_2 : n_1,n_2\in N\}$, but $h^{-1}n_1 h\in N$ since $N$ is normal.  Hence 
   $$
   gN\,hN 
   = gh\,N \,.  
   $$

Therefore these coset‐multiplications are well‐defined.  $\quad \blacksquare$  

>[!theorem]  **Theorem (Quotient Group).**  
Let $N \triangleleft G$.  Then the set of left cosets 
$$
G/N \;=\;\{\,g\,N : g \in G\,\}
$$ 
is a group under the multiplication  
$$
(gN)\,(hN) \;=\; (g\,h)\,N.
$$  
Moreover, the map 
$$
\pi: G \;\longrightarrow\; G/N, 
\qquad \pi(g) \;=\; g\,N
$$ 
is a group homomorphism with $\ker \pi = N$.  We call $G/N$ the **quotient group** (or **factor group**) and $\pi$ the **quotient homomorphism**.  

**Proof:**  
1. **Closure & Associativity.**  
   - If $gN,\,hN \in G/N$, then by normality of $N$, $(gN)\,(hN) = (gh)N \in G/N$.  
   - Associativity follows from associativity in $G$:
     $$
     \bigl((gN)(hN)\bigr)(kN)
     = \bigl((g\,h)N\bigr)(kN)
     = (g\,h\,k)N
     = (gN)\bigl((h\,k)N\bigr)
     = (gN)\bigl((hN)(kN)\bigr).
     $$
2. **Identity.**  
   The coset $e_G N = N$ acts as the identity: for any $gN \in G/N$,  
   $$
   N\,(gN) = (e_G g)N = gN, 
   \qquad
   (gN)\,N = (g e_G)N = gN.
   $$
3. **Inverses.**  
   If $gN \in G/N$, then $(gN)\,\bigl(g^{-1}N\bigr) = (g\,g^{-1})N = e_G N = N$.  Similarly, $\bigl(g^{-1}N\bigr)(gN)=N$.  Thus $(g^{-1}N)$ is the inverse of $(gN)$.

Hence $G/N$ is a group.

4. **Quotient homomorphism & kernel.**  
   Define $\pi: G \to G/N$ by $\pi(g) = gN$.  Then  
   $$
   \pi(g_1 g_2) = (g_1 g_2)\,N = (g_1 N)\,(g_2 N) = \pi(g_1)\,\pi(g_2),
   $$
   so $\pi$ is a homomorphism.  By definition,
   $$
   \ker \pi \;=\; \{\,g \in G : \pi(g) = N\}
   \;=\;\{\,g \in G : gN = N \,\}
   \;=\; N.
   $$

Therefore $\pi$ is a surjective homomorphism with kernel $N$, and $G/N$ is called the quotient group.  $\quad \blacksquare$  

---

>[!corollary]  **Corollary 4.1.**  
If $N \triangleleft G$, then there is a group $H$ and a homomorphism $\varphi: G \to H$ such that $\ker \varphi = N$.  In fact, one can take $H = G/N$ and $\varphi = \pi$ the quotient map.

>_Note:_ Another way to think about the quotient group is that each coset $gN$ “represents” the equivalence class $\{\,g\,n : n \in N\,\}$, and multiplication of classes is inherited from $G$: 
>$$
>gN = \{g\,n : n \in N\}, 
>\quad 
>g'N = \{g'\,n' : n' \in N\}, 
>\quad 
>(gN)\,(g'N) = (g\,g')\,N.
>$$
