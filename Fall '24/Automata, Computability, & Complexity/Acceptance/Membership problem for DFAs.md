$$A_{\text{DFA}} = \{<M,w> | M \text{ is a DFA and }M \text{ accepts } w\}$$
>Given a DFA $M$ & string $w$, does $M$ accept $w$?
>	==decidable==

$<M>$ : encoding of DFA $M$ as a string
	DFA = set $Q$ of states, input alphabet $\sum$ , initial state $q_0$, accepting states $F$, transition function $\delta$ (encoded as a list of triples consisting of <u>old-state, symbol, new-state</u>)

$<M,w>$ : input is a pair...
	1) encodes DFA $M$ 
	2) input for $M$ 

## Halting TM/Program $P$ for $A_{\text{DFA}}$ 
```
First check if input is well-formed & encodes a DFA M
	if not, stop & reject
	if so, execute DFA M on w & check if M ends up in an accepting state 
		if so, stop & accept
		else reject
```
>machine $P$ is not a DFA but a TM 
>	language $A_{\text{DFA}}$ is decidable, but <u>not regular</u>

