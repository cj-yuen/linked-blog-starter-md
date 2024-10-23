![[Pasted image 20241022235713.png]]
>change in syntax def.:
>	Transition function $\Delta$ : $Q \times \Gamma \rightarrow 2^{Q \times \Gamma \times \{ L, R\}}$ 
>		assume $\Gamma(q, \gamma)$ always contains 2 choices: 
>			$\delta_0$ : $Q \times \Gamma \rightarrow Q \times \Gamma \times \{L, R\}$ 
>			$\delta_1$ : $Q \times \Gamma \rightarrow Q \times \Gamma \times \{L, R\}$ 

![[Pasted image 20241022235928.png]]

## Simulating NTM w/Deterministic TM
![[Pasted image 20241023000919.png]]

## NTM $M$ $\rightarrow$ 3-Tape Deterministic TM $M'$ 
![[Pasted image 20241023001131.png]]
	![[Pasted image 20241023001144.png]]
	![[Pasted image 20241023004430.png]]


## Summary
given NTM $M$, there $\exists$ equivalent standard DTM $M'$ 
	if NTM $M$ has accepting execution of $n$ steps on input $w$, DTM $M'$ needs to explore all paths in execution tree up to depth $n$ so ==exponential slow down==
