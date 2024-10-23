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
>Consider $M = (Q, q_0, q_a, q_r, \Gamma, \_, \delta)$ & Configuration $C = (u, q,v)$ 
>Given Case $q \neq q_a$ and $q \neq q_r$ & curr symbol is $\_$:
>	Case $\delta(q, \_) = (q', \gamma, R)$ ==right move==
>		then Next$(C)$ $= (u\gamma, q', \epsilon)$ 
>	Case $\delta(q, \_) = (q', \gamma, L)$ ==left move==
>		if $u = \epsilon$, then $M$ is @left end, so Next$(C)$ is undefined
>		else $u$ is non-empty, let $u=u'\sigma'$ (ie. $\sigma'$ is last symbol of $u$)
>			then Next$(C) = (u', q', \sigma',\gamma)$ 