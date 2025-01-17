let collection of string $S$ be set of $|S|$ strings from alphabet $\sum$ s.t. ==**no** string in $S$ is a prefix of another string==

>is an <u>ordered tree</u> $T$ w/following properties:
>	each node of $T$ (besides root) is char of $\sum$ 
>	children of internal node of $T$ have ==distinct== labels
>	$T$ has $|S|$ leaves, each associated w/a string of $S$ s.t. the concatenation of the labels of the nodes on the path from root $\rightsquigarrow$ leaf $v$ of $T$ yields the string of $S$ associated w/$v$ 

given $S = \{\text{bear, bell, bid, bull, buy, sell, stock, stop}\}$
![[Pasted image 20240506214623.png]]

## Ways to Satisfy Assumption
<u>Assumption:</u> no string in $S$ is a prefix of another string
1) Special Character Way
	adding a $ or some other char $\not\in \sum$ @end of word
1) Special "end of word" marker 
	field/variable @last char node of each word