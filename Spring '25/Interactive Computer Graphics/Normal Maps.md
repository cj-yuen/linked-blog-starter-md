>an RBG texture used to alter the local-space normal found at a given point on an object
>works on the assumption that the untransformed normal at a given point in object space is <0,0,1>, which is obviously untrue most of the time
>	i n order to use a normal map properly, a matrix that transforms vectors from texture space to object space must be computed
>the "identity" color of an object-space normal map is <128,128,255>, which corresponds to a texture-space normal of <0,0,1>
>	in a normal map, 0 corresponds to -1 and 255 corresponds to 1 for any color channel
![[Pasted image 20250206202630.png]]

![[Pasted image 20250206202651.png]]

![[Pasted image 20250206202901.png]]

![[Pasted image 20250206203255.png]]

