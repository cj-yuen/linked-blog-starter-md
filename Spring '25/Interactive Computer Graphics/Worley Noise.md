![[Pasted image 20250218150604.png]]

## Generation
![[Pasted image 20250218150843.png]]
![[Pasted image 20250218150850.png]]
>==Time Complexity:== $O(XYN)$
>	$X,Y$ - image width & height
>	$N$ - # of random points

### Optimization
![[Pasted image 20250218151219.png]]

![[Pasted image 20250218151248.png]]
![[Pasted image 20250218151301.png]]
1) get frag's UV coords on screen
2) multiply UV by $MN$ 
3) floor your $MN$ coords to map to a grid 

## in Shader
![[Pasted image 20250220142301.png]]
![[Pasted image 20250220142307.png]]

![[Pasted image 20250220142319.png]]

## Perturbing Noise Input Coordinates
![[Pasted image 20250220142348.png]]
![[Pasted image 20250220145602.png]]

