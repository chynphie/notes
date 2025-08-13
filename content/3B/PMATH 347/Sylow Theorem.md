## Automorphisms

> [!definition] Definition 1  
> An automorphism of a group $G$ is an isomorphism $\varphi : G \to G$.

> [!lemma] Lemma 1  
> If $g \in G$, then $\varphi : G \to G,\ h \mapsto ghg^{-1}$ is an automorphism.

> [!proof]  
> $\varphi(h_1h_2) = gh_1h_2g^{-1} = gh_1g^{-1} \cdot gh_2g^{-1} = \varphi(h_1) \cdot \varphi(h_2)$. (1)

> [!corollary] Corollary 1  
> If $H \le G$ then $gHg^{-1} \le G$ for all $g \in G$.

## Sylow’s Theorem

> [!definition] Definition 2  
> Let $p$ be a prime. A **$p$-group** is a group of order $p^n$ for some $n \ge 0$. A **$p$-subgroup** of $G$ is a subgroup of $G$ which is a $p$-group.

Recall: If $p \mid |G|$, $G$ finite, $p$ prime, then $G$ has an element of order $p$ (Cauchy’s Theorem).

Suppose $|G| = p^k m$ where $p$ is prime, $k \ge 1$, $\gcd(p, m) = 1$.

If $H$ is a $p$-subgroup of $G$, then $|H| \mid |G| \Rightarrow |H| = p^\ell$ for some $\ell \le k$.

**Question:** What are the $p$-subgroups of $G$? In particular, what is the largest $\ell$ such that $G$ has a subgroup of order $p^\ell$?

> [!definition] Definition 3  
> Let $|G| = p^k m$, where $p$ is prime, $k \ge 1$, and $\gcd(p, m) = 1$. A **Sylow p-subgroup** of $G$ is a subgroup $H \le G$ with $|H| = p^k$.  
> We let $\text{Sylow}_p(G)$ denote the set of Sylow $p$-subgroups of $G$, and define $n_p(G) := |\text{Sylow}_p(G)|$.

> [!theorem] Theorem 1 (Sylow’s Theorems)  
> Let $|G| = p^k m$, where $p$ is prime, $k \ge 1$, and $\gcd(p, m) = 1$. Then:  
> 1.  $\text{Sylow}_p(G) \ne \emptyset$, i.e., $G$ has a Sylow $p$-subgroup.  
> 2.  If $Q$ is a $p$-subgroup of $G$ and $P$ is a Sylow $p$-subgroup, then there is a $g \in G$ such that $Q \le gPg^{-1}$.  
>     1. As a result, all Sylow $p$-subgroups are conjugate.  
> 3.  $n_p(G) \equiv 1 \mod p$, and $n_p = [G : N_G(P)]$ for any $P \in \text{Sylow}_p(G)$.

Proof of Sylow’s Theorem (1):

- The proof is by induction on $|G|$. In the base case, we have $|G| = 1$, and there is nothing to prove.
- Suppose that Sylow’s Theorem (1) holds for all groups of size smaller than $|G|$. Let $|G| = p^k m$ as in the theorem.

- **Case 1:** $p \mid |Z(G)|$. By Cauchy’s Theorem, $Z(G)$ has a subgroup $N$ of order $p$. Since $N \le Z(G)$, $N \trianglelefteq G$.

	- Then $|G/N| = p^{k-1}m$. By induction, $G/N$ has subgroup $P_0$ of order $p^{k-1}$. Let $P = q^{-1}(P_0) \supseteq N$.
	- By the Correspondence Theorem, $P_0 \cong P/N$, which implies that $|P| = p^k$.

- **Case 2:** $p \nmid |Z(G)|$. Let $T$ be a set of representatives for conjugacy classes of $G$ not contained in $Z(G)$.

	- Then  $|G| = |Z(G)| + \sum_{t \in T} |\text{Conj}(t)|$. (2)
	- As in the proof of Cauchy’s Theorem, this tells us that $p \mid |\text{Conj}(t)|$ for some $t \in T$, and  
	- $|\text{Conj}(t)| = \frac{|G|}{|C_G(t)|} \Rightarrow p^k \mid |C_G(t)|$. (3)
	- Since $|C_G(t)| \mid |G|$, we get that $|C_G(t)| = p^k r$ for some $r$. Since $t \notin Z(G)$, $|C_G(t)| < |G|$, and by induction, $G$ has a Sylow $p$-subgroup. This is a Sylow $p$-subgroup of $G$.

> [!lemma] Lemma 2  
> Suppose $P \in \text{Sylow}_p(G)$, $Q$ a $p$-subgroup. Then $Q \cap N_G(P) = Q \cap P$.

Proof: 
- We know $P \subseteq N_G(P)$, so $Q \cap P \subseteq Q \cap N_G(P)$. Let $H = Q \cap N_G(P)$.  
- Then $H \le Q$, so $H$ is a $p$-subgroup and $H \le N_G(P)$. By the Second Isomorphism Theorem:  
- $|HP| = \frac{|P||H|}{|P \cap H|}$ (a power of $p$) (4)  
- So $HP$ is a $p$-group, and $P \subseteq HP$. Since $P$ is a Sylow $p$-group, $HP = P \Rightarrow H \subseteq P \Rightarrow H = Q \cap P$.

 Proof of (2) and (3)

- Suppose $P$ is a Sylow $p$-subgroup of $G$, and let $\mathcal{O}_P = \{gPg^{-1} : g \in G\}$ be the orbit of $P$ in the conjugation action on $2^G$. All elements of $\mathcal{O}_P$ are Sylow $p$-subgroups.

- Suppose $Q \le G$ is a $p$-subgroup. $Q$ acts on $\mathcal{O}_P$ by conjugation. Let $T$ be a set of representatives for this action. Then  
- $|\mathcal{O}_P| = \sum_{P' \in T} |Q \cdot P'|$, (5)  where  $Q \cdot P' = \{qP'q^{-1} : q \in Q\}$ (6)  is the $Q$-orbit of $P'$ in $T$ under the conjugation action.
- The stabilizer of $P'$ in the same action is  $C_Q(P') = \{q \in Q : qP'q^{-1} = P'\} = Q \cap N_G(P') = Q \cap P'$. (7) So  $|Q \cdot P'| = [Q : Q \cap P']$.
- In particular, if $Q \cap P' \ne \{e\}$, then $|Q \cdot P'| > 1$, and hence $p \mid |Q \cdot P'|$.

-  Claim 1: $|\mathcal{O}_P| \equiv 1 \mod p$
	- proof : Take $Q = P$ and choose $T$ such that $P \in T$. Then $P \cap P = P$ so $|Q \cdot P| = 1$.  For $P' \in T \setminus \{P\}$, $p \mid [P : P \cap P']$. Thus,  $|\mathcal{O}_P| = \sum_{P' \in T} |Q \cdot P'| \equiv 1 \mod p$. (9)
- Claim 2 : Every $p$-subgroup $Q$ is contained in $P'$ for some $P' \in \mathcal{O}_P$.
	- Proof:
		- If $Q \nsubseteq P'$ for all $P' \in T$, then $p \mid [Q : Q \cap P']$ for all $P'$, so:  
		- $|\mathcal{O}_P| = \sum_{P' \in T} [Q : Q \cap P'] \equiv 0 \mod p$, (10)  contradicting Claim 1. Thus, $Q \subseteq P'$ for some $P'$.
- This proves (2). Also, (2) implies that every Sylow subgroup is contained in $\mathcal{O}_P$, which means that  $n_p = |\mathcal{O}_P| \Rightarrow n_p \equiv 1 \mod p$ (11)  by Claim 1. Also  $n_p = [G : N_G(P)]$ (12)  by the orbit-stabilizer theorem, because $N_G(P)$ is the stabilizer of $P$ in the $G$-action, so $|\mathcal{O}_P| = [G : N_G(P)]$.

> [!corollary] Corollary 2  
> If $n_p(G) = 1$, then $G$ has a unique Sylow $p$-subgroup, and it is normal.
