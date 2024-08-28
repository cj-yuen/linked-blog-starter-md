$$\gamma$$
>function $\gamma$ for a set $S$ of letters
>	maps each letter $x\in S$ to some sequence of 0's & 1's s.t. for any distinct $x,y\in S$, the sequence $\gamma(x)$ is not a prefix of the sequence of $\gamma(y)$ 

ie. given set $S = \{ a,b,c,d,e\}$, one potential $\gamma$ is
	$\gamma(a) = 11$
	$\gamma(b) = 01$ 
	$\gamma(c) = 001$ 
	$\gamma(d)=10$ 
	$\gamma(e)=000$ 

ie. given a prefix-free text consisting of letters $x_1, x_2, \dots, x_n$, and encoding function $\gamma$ which is then used to concatenate all the bit sequences together to form $\gamma(x_1)\gamma(x_2)\dots \gamma(x_n)$, we can reconstruct the original text by
	scan from left to right & once you see enough bits to match an encoding of some letter, output the letter & delete corresponding bits from the front of the message & iterate

## Tree-Based Representation
>$T$ is a [[Binary Tree]] w/the $\#$ of leaves $=$ size of the alphabet $S$ & we label each leaf w/distinct letter in $S$  
>every left child is a 0 & right is a 1