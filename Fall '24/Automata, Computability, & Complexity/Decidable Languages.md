>a language $A$ is called <u>decidable/recursive</u> if there $\exists$ a [[Halting Turing Machines]] $M$ s.t. $L(M)=A$ 
>	there is a TM $M$ that given an input $w$, if $w$ is in $A$, halts in the accepting state & otherwise halts in the rejecting state 
>==Solvable problem== 
>	ie. PALINDROMES $=\{w | w \text{ is a palindrome} \}$ is [[Decidable Languages]] 


## Decidable
### Every[[ Regular Language]]
>a language $A$ is <u>regular</u> if there is a DFA $M$ s.t. $L(M) = A$$ 
>	a TM can do what a DFA can & guarantee halting 
>	![[Pasted image 20241022003356.png]]


## Closure 
### Proof
><u>Goal:</u> show that there $\exists$ [[Halting Turing Machines]] $M$ s.t. $M$ accepts input $w$ exactly when...

### Properties
- [[Intersection]] 
	if 2 languages are [[Decidable Languages]], then so is their <u>intersection</u> 
	==Proof:== show that there $\exists$ [[Halting Turing Machines]] $M$ s.t. $M$ accepts input $w$ exactly when both $M_1$ and $M_2$ do
		![[Pasted image 20241023004949.png]]
- [[Union]] 
	if 2 languages are [[Decidable Languages]], then so is their <u>union</u> 
	==Proof:== show that there $\exists$ [[Halting Turing Machines]] $M$ s.t. $M$ accepts input $w$ exactly when either $M_1$ or $M_2$ do
		![[Pasted image 20241023005045.png]]
- [[Complement]]
	if 2 languages are [[Decidable Languages]], then so is their <u>complement</u> 
	==Proof:== show that there $\exists$ [[Halting Turing Machines]] $M$ s.t. $M$ accepts input $w$ exactly when $M$ does not 
		![[Pasted image 20241023005149.png]]
- Concatenation
- Kleene-*
- Prefix/Suffix
- Shuffle 
- ...