1. Formulate the LP in standard form
    - **Objective**: min⁡ or max⁡ a linear function
    - **Constraints**: All equations, with all variables ≥ 0
    - If you have “≤” constraints, add **slack** variables; for “≥” constraints, add **surplus** (and possibly **artificial**) variables.
```
Maximize   z = c₁x₁ + c₂x₂ + … + cₙxₙ
Subject to
  a₁₁ x₁ + a₁₂ x₂ + … + a₁ₙ xₙ ≤ b₁
  a₂₁ x₁ + …                     ≤ b₂
  …
  xⱼ ≥ 0  for all j
```
	
2. Convert to an initial tableau
    - Introduce slack variables sis_isi​ so that each constraint becomes an **equality**
    - Write the augmented matrix (**tableau**) with one row per constraint plus one for the (negated) objective.

| Basis      | $x1x_1x1​$      | $x2x_2x2​$      | …   | Slack / Surplus | RHS (bbb)  |
| ---------- | --------------- | --------------- | --- | --------------- | ---------- |
| $s1s_1s1​$ | $a11a_{11}a11$​ | $a12a_{12}a12​$ | …   | 1               | $b1b_1b1​$ |
| $s2s_2s2​$ | $a21a_{21}a21​$ | $a22a_{22}a22​$ | …   | 0               | $b2b_2b2​$ |
| …          | …               | …               | …   | …               | …          |
| **Obj**    | $−c1-c_1−c1​$   | $−c2-c_2−c2​$   | …   | 0               | 0          |
|            |                 |                 |     |                 |            |

3. Check for optimality
    - **Maximization**: if all entries in the **bottom row** (ignoring the RHS column) are ≥ 0, you’re optimal.
    - **Minimization**: if all are ≤ 0, you’re optimal.

4. Select the entering variable (pivot column)
    - **Max**: pick the most negative coefficient in the objective row.
    - **Min**: pick the most positive coefficient.
    - Call its column the **pivot column**.

5. Select the leaving variable (pivot row)   
    - For each row iii, compute the ratio bi/ai,jb_i / a_{i,j}bi​/ai,j​ where ai,j>0a_{i,j} > 0ai,j​>0.        
    - Choose the **smallest non-negative** ratio.        
    - That row is the **pivot row**.
        
6. Perform the pivot
    - **Normalize** the pivot row so that the pivot element becomes 1 (divide entire row).        
    - **Zero out** all other entries in the pivot column by row-operations:
        
        New rowk=Old rowk  −  ak,j×(Pivot row) \text{New row}_k = \text{Old row}_k \;-\; a_{k,j}\times(\text{Pivot row})New rowk​=Old rowk​−ak,j​×(Pivot row)
7. Update basis**    
    - Replace the old basic variable (slack or surplus) in the pivot row with the entering variable.
        
8. Repeat**    
    - Go back to **Step 3** with the new tableau.        
    - Stop when the optimality condition holds.
        
9. Read off the solution**    
    - Basic variables (one per row) have their values in the RHS column.        
    - Non-basic variables = 0.        
    - Objective value = RHS of the objective row.