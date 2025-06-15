> [!proposition] Proposition 2.1. 
> let $D=(N,A)$ be a digarph, with weights $w\in \mathbb{R}^{A}$m which has no $w(C)<0$. 
> let $Q$ be a st-diwalk, s≠t. 
> Then there exists an st-dipath P with $w(P)\leq w(Q)$.

Proof: Q is a collection of dipaths and dicycles by prp1.4 then $w(Q)=w(P)+\sum_{j=1}^{n}w(C_{j})$ since all $w(C_{j})\geq0$ thus $w(P)\leq w(Q)$

> [!proposition] Proposition 2.2
> Suppose D=(N,A) has no negative dicycles and let P is the shortest st-dipath and Q the shortest st-diwalk
> Then $w(Q)=w(P)$

Proof: $w(P)\leq w(Q)$ by prop2.1 and since $\forall w(P)<w(P')$ as P is shortest st-dipath->$w(P')\leq w(Q)$ thus it must be  $w(Q)=w(P)$
