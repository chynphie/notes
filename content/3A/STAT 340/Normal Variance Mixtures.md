Generates normal distribution by introducing randomness into its variance. The variance itself follows another distribution.

Let $Z \sim \text{Normal}(0, I_d)$ independent of the scalar $W \sim F_W$ with $W \geq 0$, then $X$ is a normal variance mixture if its distribution:
$$X = \mu + \sqrt{W} A Z$$
- **Mean shift**: $\mu$
- **Scale parameter**: $\sqrt{W} A$

The scalar $W$ affects all components $X_1, \dots, X_d$, and conditional on $W$, $X | W \sim \text{Normal}(\mu, W\Sigma)$.

- If $W \sim \text{IG}(\nu/2, \nu/2)$ for some $\nu > 0$, then $X \sim t_{\nu}(\mu, \Sigma)$, the multivariate $t$ distribution with $\nu$ degrees of freedom.
- Use When:
	- Generalizing normal distribution by allowing for skewness and heavy tails.
	- Useful in finance.
	- Describes real-world data better than normal distribution, sometimes underestimating extreme values.
#### Algorithmn:
1. Sample $Z_{1},\dots, Z_{d} \sim N(0,1)$ from $W$
2. Return $\mu + \sqrt{ W }AZ$ 