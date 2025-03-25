>an image which is sampled to determine the color of an object at a particular point on the object's surface
>	most commonly a 2D image, but 1D/3D are also used on occasion
>	could use a "4D" image (an animated 3D texture)

==Problem:== The texture's pixels must be mapped to points on the object's surface before the texture can be sampled

![[Pasted image 20250206201045.png]]

## Texture Space
![[Pasted image 20250206201541.png]]

![[Pasted image 20250206201631.png]]

## [[Interpolation]] triangle UVs
![[Pasted image 20250206201839.png]]

## [[Normal Maps]]

## Shading vs. Reflection Models
![[Pasted image 20250207144901.png]]

### Specific Models
- [[Gouraud Shading Model]]
- [[Phong Shading Model]]
- [[Blinn-Phong Reflection Model]]

## Code
```C++
texelFetch()
// give me the int coordinates of the texture

texture()
// give me a UV coord
```

## Setting up a [[Texture]] in [[OpenGL]]
![[Pasted image 20250325140510.png]]

![[Pasted image 20250325140522.png]]

![[Pasted image 20250325141655.png]]

![[Pasted image 20250325142054.png]]

![[Pasted image 20250325143015.png]]

![[Pasted image 20250325143023.png]]
![[Pasted image 20250325143429.png]]
![[Pasted image 20250325143750.png]]
![[Pasted image 20250325143801.png]]

![[Pasted image 20250325144001.png]]

![[Pasted image 20250325144009.png]]
