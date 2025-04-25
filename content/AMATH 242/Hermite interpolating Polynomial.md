- Method 1: 
	1. **List your “nodes” with multiplicity**
		- $z0​=a,z1​=a,z2​=b,z3​=b.$
	2. **Fill in the zeroth column** with 
		- $f[z0​]=f(a),f[z1​]=f(a),f[z2​]=f(b),f[z3​]=f(b).$
	3. **First divided differences**
		
		- For the repeated node at a:
			- $f[z1​,z0​]=f'(a)$
		- For the mixed node (a,b)
			- $f[z2​,z1​]=\frac{f(b)−f(a)​}{b−a}.$
		- For the repeated node at b:
			- $f[z3​,z2​]=f′(b).$
	4. **Second divided differences**
		- $f[z2​,z1​,z0​]=\frac{f[z2​,z1​]−f[z1​,z0​]​}{z2​−z0​}=\frac{\frac{f(b)−f(a)}{b−a}​−f′(a)}{b−a}​,$
		- $f[z2​,z1​,z0​]=\frac{f[z3​,z2​]−f[z2​,z1​]}{z3​−z1​}=\frac{\frac{f(b)−f(a)}{b−a}​−f′(a)}{b−a}​,$
	5. **Third divided difference**
		- $f[z3​,z2​,z1​,z0​]=\frac{​f[z3​,z2​,z1​]−f[z2​,z1​,z0​]​}{z3​−z0}=\frac{f[z3​,z2​,z1​]−f[z2​,z1​,z0​]}{b−a}$
	6. **Write the Newton form**
		- $H(x)=f[z0​]+f[z1​,z0​](x−z0​)+f[z2​,z1​,z0​](x−z0​)(x−z1​)+f[z3​,z2​,z1​,z0​](x−z0​)(x−z1​)(x−z2​)$