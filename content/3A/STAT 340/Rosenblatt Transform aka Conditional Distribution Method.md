Key idea: Sampling each $W$ one after the other recursively, each time sample $X_{n+1} | X_n = x_n$.
### Example in Dimension 2: Sample $(X_1, X_2) \sim F$
1. Sample $U_1, U_2 \sim U(0,1)$.
2. Set $Y_1 = F_1^{-1}(U_1)$, then $(Y_1 \sim F_1)$.
3. Compute the distribution function of $X_2 | X_1 = y_1$, say  
   $$F_{X_2 | X_1 = x_1} (x_2) = P(X_2 \leq x_2 | X_1 = x_1)$$
4. Set $Y_2 = F_{X_2 | X_1 = y_1}^{-1}(U_2)$.
5. Return $(Y_1, Y_2)$.