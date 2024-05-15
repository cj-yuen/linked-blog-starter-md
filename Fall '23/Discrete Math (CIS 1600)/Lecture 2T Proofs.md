#proofs 
## if $x$ and $y$ are ints where $x+y$ is even, then $x$ and $y$ are either both odd or both even 
**Proof by Contrapositive**
"if exactly one of x or y is even then x+y is odd" WLOG, for some ints $k$ and $l$, let $x=2k$ be even and $y=2l + 1$ be odd 
$$\begin{align*} x+y &= 2k+2l + 1 \\ &= 2(k+l) + 1 \end{align*}$$
$\therefore$ x+y is odd given that x is even and y is odd. 

## at least 3 of any 25 days chosen must fall in the same month of the year 
**Assume for Contradiction** that "at least 3 of the 25 days chosen must fall in the same month of the year" is not true
	there are 12 months meaning that there can be at most 24 days that must be chosen
	this contradicts the premise that 25 days are chosen 
	$\therefore$ we have reached a contradiction proving the proposition 

## if $3n+2$ is odd then $n$ is odd 
**Proof by Contradiction**
assume that $3n+2$ is odd and $n$ is even 
	since $n$ is even, $n=2k$ for some int $k$ 
		$3(2k) + 2 = 6k + 2 = 2(3k+1)$ 
	we have reached that $3n+2$ is even which contradicts the premise the $3n+2$ is odd 
	$\therefore$ we have proven the claim

## for all real #'s $a$ and $b$, if $ab$ is irrational, then either $a$ or $b$ or both must be irrational 
**Proof by Contrapositive**
"if both $a$ and $b$ are rational #' then their product $ab$ is a rational #."
let $a = p/q$ and $b = r/s$, where $p,q,r,s$ are ints and $q\ne 0$ and $s \ne 0$. 
$$ab = \frac{p}{q}* \frac{r}{s} = \frac{pr}{qs}$$
$pr$ and $qs$ are both ints. Also since $q\ne 0$ and $s \ne 0$, $qs \ne 0$. Thus $ab$ is a rational #. 

## Let $A = \{ 2^1,2^2,2^3,\dots \}$ and $B = \{ 2,4,6,\dots\}$. Prove that $A\subseteq B$ 
let $x$ be an arb. but part. element in $A$. $x$ is in the form $2^j$ for some positive int $j$. Element in $B$ is of the form $2 \cdot i$, for some $i\in \{ 1,2,3,\dots\}$. Since $x = 2^j = 2 *i$ where $i=2^{j-1}$. Since $j$ is positive, $j-1 \geq 0$ and hence $i \geq 1$. Thus $x \in B$ and therefore $A \subseteq B$. 

## Sets $A$ and $B$. $A = B$ iff $A\subset B$ and $B \subseteq A$ 
Let x be any element in A. Since A ⊆ B, x is also an element in B. Similarly, if an element y ∈ B, since B ⊆ A, y is also an element in A. Thus there is no element in A that is not in B and there is no element in B that is not in A, that is, A and B have the same elements. By definition, A = B.

## Let A = {n | n = 2k + 5 for some k ∈ N} and B = {n | n = 2j + 1 for some j ∈ N}. Is A ⊆ B? 
let $x$ be any arb. but part. element in $A$. Then, 
$$\begin{align*} x &= 2k+5 \\ &= 2(k+2) +1\end{align*}$$
Since k ∈ N, k + 2 ∈ N, and hence we have proved that any arbitrary element x ∈ A also belongs to the set B. Thus A ⊆ B

## Let A = {n ∈ N | n = 2k 2 − 3, for some k ∈ N} and B = {n ∈ N | n = j 2 + 3 for some j ∈ N}. Prove that A $\not \subseteq$ B
Note that 5 ∈ A, since 5 = 2 · 2 2 − 3. Observe that for 5 to be an element of B, 5 = j 2 + 3, that is, j 2 = 2, which is impossible since j must be a natural number. Thus we have found an element of A that does not belong to B and hence A 6⊆ B

## Let A = {n ∈ N | n ≥ 2 and n = 4j − 5, for some j ∈ N} and B = {n ∈ N | n ≥ 0 and n = 2k + 1 for some k ∈ N}. Prove that A ⊂ B.
Let x be an arbitrary but particular element of A. We know that x is of the form 4j − 5, where j ∈ N. Thus we get
$$\begin{align*} x &= 4j-5 \\ &= 2 \cdot 2j - 6 + 1 \\ &= 2 (2j-3) + 1 \end{align*}$$
Since x ≥ 2, it must be that 4j − 5 ≥ 2. Solving for j gives us j ≥ 7/4. Since j ∈ N, we have j ≥ 2. Thus the integer 2j − 3 ≥ 1. Thus x ∈ B and hence A ⊆ B. Note that the element 1 ∈ B, but it does not belong to A. Hence A ⊂ B.

## Screenshots
![[Pasted image 20231014164213.png]]

