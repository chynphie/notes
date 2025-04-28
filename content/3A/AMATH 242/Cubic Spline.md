1. Uses cubic polynomials between successive nodes
2. Satisfies specific interpolation and smoothness conditions

- **Boundary Conditions**
	1. Free Boundary (Natural Cubic Spline):
		- $S_1'(x0) = 0$
		- $S_n'(xn) = 0$
	2. Clamped Boundary:
		- Specifies first derivatives at endpoints
		- Generally leads to more accurate approximation
	3. Periodic Boundary:
		- Requires $f0 = fn$
		- First and second derivatives of first and last polynomials are equal
- **Cubic Spline Construction**
	- Requires determining 4n constants
	- Polynomial form:$Sj(x) = aj + bj(x - xj) + cj(x - xj)² + dj(x - xj)³$
	- Uses complex system of equations to determine coefficients