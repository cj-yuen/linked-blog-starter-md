>if a procedure can be broken down into $k$ steps 
>	the 1st step can be performed in $n_1$ ways 
>	the 2nd step can be performed in $n_2$ ways ==regardless of how the 1st step was performed==
>	$\vdots$ 
>	the $k^{th}$ step can be performed in $n_k$ ways ==regardless of how the preceding steps were performed==
>	then the entire procedure can be performed in $n_1 * n_2* \dots *n_k$ ways 

ie. An [[Ordered Pair]] $(a,b)$ | $M$ is an $m$-element set and $N$ is an $n$-element set. How many ordered pairs are there whose 1st members belongs to $M$ and whose 2nd member belongs to $N$? 
	Step 1: choose 1st member from set M (m ways)
	Step 2: choose 2nd member from set $N$ (n ways)
	by [[Multiplication Rule (M.R.)]] the # of ordered pairs is $m*n$ 

==ie. 3 officers (Pres., Treasurer, Sec.) are to be chosen among 4 people (Ann, Bob, Clyde, Dan). Ann cannot be the Pres. and either Clyde or Dan must be the secretary. How many ways can the officers be chosen?==
	Step 1: choose the Sec. (has to be first as most selective either Cylde or Dan) (2 ways)
	Step 2: choose the Pres. (cannot be Ann) (2 ways)
	Step 3: choose the Treasurer (2 ways )
	by [[Multiplication Rule (M.R.)]] the # of ways to choose officers is $2*2 *2 = 8$ 

ie. If $S = \{x_1, x_2, \dots, x_n \}$ what is $|P(S)|$?  
	Procedure with $n$ steps deciding whether each of the n elements is either in/out. There are 2 ways to do each of the $n$ steps and therefore by [[Multiplication Rule (M.R.)]] the total # of subsets of $S$, in other words the cardinality of the [[Power Set]] = $2^n$ 
