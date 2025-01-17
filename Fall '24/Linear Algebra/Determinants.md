$$\begin{align*}
\text{det}(A) &= \text{det}(\begin{bmatrix}a & b \\ c & d\end{bmatrix}) \\&= |A| \\ &= \begin{vmatrix}a & d \\ c & d\end{vmatrix} \\ &= ad-bc\end{align*} 
$$
>==Geometric def.:== signed area of the parallelogram spanned by the vectors $[ a,c]$ & $[b,d]$
>	![[Pasted image 20240906121611.png]]

## Approach
go from [[Identity Matrix]] $\rightarrow$ $A$
$$\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \rightarrow \begin{bmatrix}a & b \\ c & d\end{bmatrix}$$
using steps...
1) $$\begin{bmatrix} a & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix}a & 0 \\ 0 & 1 \end{bmatrix}$$
2) $$\begin{bmatrix}1 & b \\ 0 & 1 \end{bmatrix}\begin{bmatrix} a & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix}a & b \\ 0 & 1 \end{bmatrix}$$
	a [[Shear Transformation]] 
3) $$\begin{bmatrix}1 & 0 \\ c/a & 1 \end{bmatrix} \begin{bmatrix}1 &0 \\ 0 & (ad-bc)/a \end{bmatrix}\begin{bmatrix} a & b \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix}a & b \\ c & d \end{bmatrix}$$
	scale the 2nd row by factor $\frac{ad-bc}{a}$ & add $\frac{c}{a}$ 
4) all of these transformation equate to $\frac{a(ad-bc)}{a}$ which equals $ad -bc$ (the [[Determinants]])

## Higher Dimensions
- relationship with [[Elementary Row Operations]] 
	![[Pasted image 20240907173137.png]]

- [[Diagonal Matrix]] 
	![[Pasted image 20240907173214.png]]
- [[Upper Triangular Matrix]] & [[Lower Triangular Matrix]] 

### Method: Row Reduction
Given:
![[Pasted image 20240907173407.png]]

![[Pasted image 20240907173435.png]]

### Method: Expansion Along a Row
![[Pasted image 20240909125127.png]]

![[Pasted image 20240909125229.png]]

## Properties
- $\text{det}(I) = 1$
	[[Identity Matrix]] 
- $\text{det}(A) = \text{ product of diagnoals}$ 
	[[Diagonal Matrix]], [[Upper Triangular Matrix]], [[Lower Triangular Matrix]] 
- ![[Pasted image 20240909133556.png]]
- ![[Pasted image 20240909133611.png]]
- $\text{det}(A^T) = \text{det}(A)$ 
	[[Matrix Transpose]] 
- ![[Pasted image 20240909133656.png]]
- ![[Pasted image 20240909133706.png]]
- for $n$-by-$n$ matrix $A$ multiplied by scalar $c$,
$$\text{det}(cA) = c^n\text{det}(A)$$
- for $n$-by-$n$ matrices $A$ & $B$,
$$\text{det}(AB) = \text{det}(A) \text{det}(B)$$
- a square matrix $A$ is [[Invertible]] $\leftrightarrow$ iff $\text{det}(A) \neq 0$ and...
$$\text{det}{A^{-1}} = \frac{1}{\text{det}(A)}$$
