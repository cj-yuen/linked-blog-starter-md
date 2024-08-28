## ie. Prove that if $n$ is an int greater than 1 then either $n$ is a prime or it can be written as a product of primes 
let $P(n)$ be "$n$ can be written as a product of primes"
>**IH:** Assume that $P(j)$ is true for $1 < j \leq k$ 
>**BC:** $P(2)$ is true, the base case holds true
>**IS:**  show $P(k+1)$ is true 
>	**Case 1:** $k+1$ is prime (done)
>	**Case 2:** $k+1$ is composite 
>		$k+1 = a \times b$ for some $a$ & $b$ | $2 \leq a \leq b < k+1$ 
>		by I.H., $a$ is a prime or can be written as a product of primes (same applies to $b$). Since $k+1 = a \times b$, it can be also be written as a product of primes. 


