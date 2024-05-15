#lecture_notes [[HW 1T]] [[Lecture 1T Proofs]]
## Intro to Logic
[[Proposition]] 
	ie. "2 + 2 = 4" 

### Logical Operators 
1) [[Negation]] ($\neg p$ or $\bar p$ ) 
2) [[Conjunction]] ($p \land q$) 
3) [[Disjunction]] ($p\lor q$)
4) [[Exclusive Or]] ($p \oplus q$) 
5) [[Implication]] ($p \rightarrow q$) 
6) [[Biconditional]] ($p\leftrightarrow q$)

### Logical Equivalence
compound propositions are considered [[logically equivalent]] if they always have the same truth value

ie. $p\rightarrow q \equiv\neg p \lor q \equiv\neg q \rightarrow \neg p$

| p | q | $\neg p$ | $\neg q$ | $p\rightarrow q$ | $\neg p \lor q$ | $\neg q \rightarrow \neg p$ |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | 
| T | T | F | F | T | T | T | 
| T | F | F | T | F | F | F | 
| F | T | T | F | T | T | T | 
| F | F | T | T | T | T | T |

## Quantified Statements
P(x) : 
	P is the [[Predicate]] w/ x as the variable
		ie. P = "is less than 15" & P(x) = "x < 15"
	can turn predicates -> propositions through [[Quantification]] 

## Proofs
### Definitions:
n is ==even==
	iff n = 2k for some int k 
$$\text{n is even} \leftrightarrow \exists \text{ an int }k \mid n =2k$$

n is ==odd== 
	iff n = 2k + 1 for some int k 
$$\text{n is odd} \leftrightarrow \exists \text{ an int k } \mid n = 2k + 1$$

n is ==prime== 
	iff n > 1 & for all positive integers r & s, if n = r * s then either r = 1 or s = 1
	otherwise n is ==composite==

$\lfloor x \rfloor$ 
$$\lfloor x \rfloor = n \leftrightarrow n \leq x < n+1, \text{ where }n \text{ is an int}$$

$\lceil x \rceil$
$$\lceil x \rceil = n \leftrightarrow n-1 < x \leq n,\text{ where }n\text{ is an int}$$

real # is ==rational==
	iff can be expressed as a ratio of 2 ints with non-zero denominator
	other is ==irrational==
$$r\text{ is rational} \leftrightarrow \exists \text{ integers a and b} \mid r = \frac{a}{b} \text{ and } b \neq 0$$

