## Background
- arose from translating English text to strings of bits 
	$\therefore$ need the encoding to be prefix-free which is done through a [[Prefix-Code]]
- to save space: letters w/greater frequencies $\rightarrow$ smaller encodings & letters w/lower frequencies $\rightarrow$ larger encodings
	$\therefore$ [[Optimal Prefix Code]]

## Notation
- given alphabet $S$ 
- for each char $x \in S$ $\rightarrow$ 
	==frequency $f_x$== - representing the fraction of letters in the text equal to $x$ 
- in a text w/$n$ letters 
	$n f_x$ are expected to be $=x$ 
- all frequencies must sum to 1
	$\sum_{x\in S} f_x =1$
- [[Encoding Length]] 
- [[Average bits per letter]]

## Lemmas
- [[Huffman Lemma 1]]
- [[Huffman Lemma 2]]
- [[Huffman Lemma 3]]
- [[Huffman Lemma 4]]
