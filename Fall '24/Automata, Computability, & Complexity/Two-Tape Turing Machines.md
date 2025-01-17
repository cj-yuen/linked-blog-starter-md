>states $Q$, initial state $q_0$, accepting state $q_a$, rejecting state $q_r$, tape alphabet $\Gamma$, input alphabet $\sum$, blank symbol $\_$, transition function $\delta : Q \times \Gamma \times \Gamma \rightarrow Q \times \{L,R\} \times \Gamma \times \{ L, R\}$ 
	![[Pasted image 20241022231449.png]]

## ie.
![[Pasted image 20241022225853.png]]
	2 tapes (potentially unbounded on right)
	2 read/write heads (move independently)
	single transition depends on curr state, contents of 2 tape cell heads, & update state (left or right)


## [[Two-Tape Turing Machines]] -> Standard TM
<u>Goal:</u> given 2-tape TM $M$, construct standard TM $M'$ s.t.
	one every input $w$, $M$ accepts/rejects/goes $\infty$ loop exactly when $M'$ accepts/rejects/goes $\infty$ loop respectively 

$$M\text{ is halting }\leftrightarrow M'\text{ is halting}$$
$$L(M) = L(M')$$
2-tape TM $M$ 
![[Pasted image 20241022232633.png]]
$\downarrow$ 
Standard TM $M'$
![[Pasted image 20241022232703.png]]
	state of $M'$ = state of $M$ + contents of 2 "curr" cells
	tape of $M'$ = # contents of Tape 1 of $M$ + # contents of Tape 2 of $M$ (marked w/x)
		changing initial input $w$ $\rightarrow$ $\# x\quad w \# \quad x$ 

### Simulate Single Transition of $M$ 
>$M'$ needs to scan entire tape & may even have to shift it