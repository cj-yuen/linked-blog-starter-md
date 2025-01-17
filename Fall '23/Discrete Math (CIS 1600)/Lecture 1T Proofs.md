#proofs
## If the sum of 2 ints is even -> their difference is even
let $m$ and $n$ be part. but arb. ints | $m+n$ is even. 
$$\begin{align*} 
\text{by def. of even} \quad m+n &= 2k \quad \text{for some int k} \\
	m &= 2k - n
\end{align*}$$
Their difference $m-n$ can be written as 
$$\begin{align*} m-n &= (2k-n) - n \\
	&= 2(k-n) \\ 
	&= 2i \quad \text{where }i = k-n \text{ is an int}
\end{align*}$$
$\therefore m-n$ is even

## For all ints $n$, if $n$ is odd then $n^2 + n + 1$ is odd 
let $n$ be an arb. but part. int | by def. $n= 2k +1$ for some int k 
$$\begin{align*}
	n^2 + n + 1 &= (2k+1)^2 + (2k + 1) + 1 	\\
		&= 4k^2 + 4k + 1 + 2k + 2 \\ 
		&= 4k^2 + 6k + 2 + 1 \\
		&= 2(2k^2 + 3k + 1) + 1 \\ 
		&= 2l + 1 \quad \text{where }l=2k^2 + 3k + 1\text{ is an int}  
\end{align*}$$
$\therefore n^2 + n + 1$ is odd  

## Let x be an int, if x > 1 then $x^3 + 1$ is composite
let $x$ be an arb. but part. int | $x>1$. 
$x^3 + 1 = (x+1)(x^2-x+1)$ 
Since x is an int, both $(x+1)$ and $(x^2 - x + 1)$ are ints 
	$(x+1)|x^3 + 1$ & $(x^2-x+1) | x^3+1$ 
$$\begin{align*} 
	\text{by def} \quad  x &> 1 \\ 
	x^2 &> x \\ 
	x^2 - x &> 0 \\ 
	x^2 - x + 1 &> 1
\end{align*}$$
$$\begin{align*} 
	x^3 + 1 &= (x+1) (x^2 - x +1) \\ 
		&= a*b \quad text{where }a > 1 \text{ and } b > 1
\end{align*}$$
$\therefore x^3 + 1$ is composite  