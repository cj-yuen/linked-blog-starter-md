#theorems 

>every positive # can be uniquely represented as a product of primes 
>	given any int $n>1$, there $\exists$ a positive int $k$, distinct prime #'s $p_1,p_2,\dots ,p_k$, & positive ints $e_1,e_2,\dots,e_k$ such that 
>		$n={p_1}^{e_1}{p_2}^{e_2}\dots {p_k}^{e_k}$ 

ie. Prove that $\sqrt{2}$ is irrational using unique factorization theorem
	**Assume for the Contradiction** that $\sqrt{2}$ is rational, then there are ints $a$ and $b$ ($b\neq 0$) such that 
		$\sqrt{2} = \frac{a}{b}$ 
		$2 = \frac{a^2}{b^2}$ 
		$a^2 = 2b^2$ 
	we an assume that $a >1$ and $b>1$ 
	$S(m)$ = the sum of the # of times each prime factor occurs in the unique factorization of $m$ 
		$S(a^2)$ and $S(b^2)$ is even 
			# of times prime factors appear in $a^2$ and $b^2$ is twice the # of times they appear in $a$ and $b$ 
		$S(2b^2) = 1 + S(b^2)$ 
			which is odd 
	There is a contradiction as we need the $S(a^2)$ must be even but $2b^2$ has an odd # of prime factors 
	$\therefore$ we have reached a contradiction and so we have proven the claim to be true 
