-  *Definition*: 
	- A matrix A=$[a_{ij}]$ has
			1. *upper bandwidth*, q if $a_{ji}=0\:for\:j>j+q$ and
			2. *lower bandwidth*, p if $a_{ij}=0\:for\:i>j+p$
	- Factoring Banded Matrices If A is banded then so are the factorizations LU, LDMT, GGT.
- ==Theorem 1==
	- Let A=LU. If A has upper bandwidth q and lower bandwidth p, then 
		1. U has *upper* bandwidth **q** and 
		2. L has *lower* bandwidth **p**