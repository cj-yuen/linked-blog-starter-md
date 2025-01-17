## ie. Prove that the [[Membership Problem for TMs]] is undecidable
>given: that we know [[Halting Problem for TMs]] is undecidable already

Suppose for contradiction $A_{\text{TM}}$ is decidable.
There exists a [[Halting Turing Machines]] $R$ s.t. $L(R) = A_{\text{TM}}$ 
	Given input <M,w>
		if M accepts w, R stops & accepts <M,w>
		else R stops & rejects <M,w>

Then there also exists a [[Halting Turing Machines]] $T$ s.t. $L(T) = HALT_{\text{TM}}$ 
```
Given input <M>
	if H accepts (<M>,<M>), stop & reject
	else stop & accept
```

![[Pasted image 20241024103233.png]]
