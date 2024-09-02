1) interchange 2 rows of the matrix
2) multiple a row by a nonzero constant
3) add a multiple of 1 row to another row

## Example:
$5x + 3y - 3z = -1$
$3x + 2y -2z =-1$
$2x - y + 2z = 8$ 

1) form [[Augmented Matrix]] 
$$\left[
\begin{array}{ccc|c}
	5 & 3 & -3 & -1 \\
	3 & 2 & -2 & -1 \\
	2 & -1 & 2 & 8
\end{array}
\right]$$
2) use elementary row operations
	$R_1 = R_1/5$ 
	$$\left[
\begin{array}{ccc|c}
	1 & 3/5 & -3/5 & -1/5 \\
	3 & 2 & -2 & -1 \\
	2 & -1 & 2 & 8
\end{array}
\right]$$
	$R_2 = R_2 - 3R_1$ & $R_3 = R_3 - 2R_1$ 
	$$\left[
\begin{array}{ccc|c}
	1 & 3/5 & -3/5 & -1/5 \\
	0 & 1/5 & -1/5 & -2/5 \\
	0 & -11/5 & 16/5 & 42/5
\end{array}
\right]$$
	$R_2 = 5R_2$ 
	$$\left[
\begin{array}{ccc|c}
	1 & 3/5 & -3/5 & -1/5 \\
	0 & 1 & -1 & -2 \\
	0 & -11/5 & 16/5 & 42/5
\end{array}
\right]$$
	$R_3 = R_3 + 11/5R_2$ 
	$$\left[
\begin{array}{ccc|c}
	1 & 3/5 & -3/5 & -1/5 \\
	0 & 1 & -1 & -2 \\
	0 & 0 & 1 & 4
\end{array}
\right]$$
	which now result in a [[Row Echelon Form]] 
3) 2 methods 
	use [[Back Substitution]] 
		$z=4$ 
		$y - 4 = -2 \rightarrow y = 2$ 
		$x + 3/5(2) - 3/5(4) = - 1/5 \rightarrow x + 6/5 - 12/5 = -1/5 \rightarrow x = -1/5 + 6/5 \rightarrow x = 1$ 
	proceed to [[Reduced Row-Echelon Form]] 
		![[Pasted image 20240831214329.png]]
