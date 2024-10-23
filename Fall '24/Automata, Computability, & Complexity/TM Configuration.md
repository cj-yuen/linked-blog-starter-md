>State + Contents of tape + Position of read head 
![[Pasted image 20241022004021.png]]

## ie.
![[Pasted image 20241022004058.png]]
	$Q$ = finite set of states 
	$q_0$ = initial state
	$q_a$ = accepting state
	$q_r$ = rejecting state
	$\Gamma$ = tape alphabet
	$\sum$ = input alphabet (subset of $\Gamma$)
	__ = blank symbol 
	$\delta$ = transition function
___
	$u$ = string over $\Gamma$ (ie. tape contents left of curr head)
	$q$ = curr state of machine $q \in Q$ 
	$v$ = string over $\Gamma$ (starting @ & right of curr head)

## Successor Configuration