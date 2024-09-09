$$aa^{-1} = a^{-1}a = 1$$
for matrices:
$$AA^{-1} = A^{-1}A = I$$

## To Solve [[System of Linear Equations]] 

$$A^{-1}Ax = A^{-1} b$$
$$x = A^{-1}b$$

## How to get
think of the inverse $A^{-1}$ as...
$$A^{-1} = 
\begin{bmatrix} c_1 \:\vert\: c_2\:\vert\: c_3 \:\vert\: \dots \:\vert\: c_n   
\end{bmatrix}$$
then $AA^{-1}$ can be...
$$AA^{-1} = 
\begin{bmatrix} Ac_1 \:\vert\: Ac_2\:\vert\: Ac_3 \:\vert\: \dots \:\vert\: Ac_n   
\end{bmatrix}$$
in which...
$$Ac_1 = \begin{bmatrix}1 \\ 0 \\ 0 \\ \vdots \\ 0 \\ 0\end{bmatrix} 
\qquad Ac_2 = \begin{bmatrix}0 \\ 1 \\ 0 \\ \vdots \\ 0 \\ 0\end{bmatrix} 
\qquad \dots \qquad Ac_n = \begin{bmatrix}0 \\ 0 \\ 0 \\ \vdots \\ 0 \\ 1\end{bmatrix}$$
which we achieve by performing [[Extreme Row Reduction]] 

## [[Invertible]] 
>an $n\times n$ matrix $A$ is [[Invertible]] $\leftrightarrow$ iff the [[Rank of a Matrix]] $A$ = $n$ 
>$A$ is [[Invertible]] $\leftrightarrow$ iff $\text{det}(A) \neq 0$ 

## [[Involutive]] 
$$(A^{-1})^{-1} = A$$ 
## Given...
$$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$$ the inverse is...
$$A^{-1} = \begin{bmatrix} a & b \\ c & d \end{bmatrix}^{-1} = \frac{1}{ad - bc} \begin{bmatrix}d & -b \\ -c & a \end{bmatrix}$$
provided 
$$ad - bc \neq 0$$ 
### Term 
- [[Determinants]] 