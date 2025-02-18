![[Pasted image 20250218145230.png]]

- given some N-dimensional noise function as a basis, we can create N-dimensional [[Fractal Brownian Motion (FBM) Noise]] 
	sum your noise function @different amplitudes, increasing the function's frequency as amplitude decreases
![[Pasted image 20250218145426.png]]

## 1D
![[Pasted image 20250218145743.png]]

![[Pasted image 20250218145938.png]]
![[Pasted image 20250218145947.png]]

## 2D 
![[Pasted image 20250218145437.png]]
- divide our space into $N \times N$ grid cells
- @each cell corner, sample our TV static noise function
- within each cell, interpolate the 4 corners' values across the square-shaped cell

![[Pasted image 20250218145752.png]]

- we need [[Bilinear Interpolation]]
	![[Pasted image 20250218145842.png]]
	![[Pasted image 20250218145849.png]]

### General 2D Interpolation
![[Pasted image 20250218145910.png]]
![[Pasted image 20250218145918.png]]

