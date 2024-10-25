$$E_{\text{DFA}} = \{ <M> | M \text{ is a DFA \& }L(M) \text{ is empty} \}$$
## Halting TM/Program $P$ for $E_\text{DFA}$ 
```
check if input is well-formed & encodes a DFA M
	if not, stop & reject
	if so, conpute set of state of M reachable from inital states
		if this set contains some accepting state of M
			stop & reject (M does accept some strings in this case)
		else stop & accept
```