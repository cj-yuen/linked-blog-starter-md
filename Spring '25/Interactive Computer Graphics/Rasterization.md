>process of converting vector graphics into dot matrix graphics
>	derived from Latin *rastrum* = "a rake"


## Triangle Rasterization
![[Pasted image 20250131135513.png]]
>determine which pixels of the screen overlap w/a triangle
>	treat each pixel as a single point in space rather than a small area

### Different Approaches
==Naive:== iterate through each pixel in the image & test whether or not it falls within the bounds of each triangle
	<u>Problem:</u> unnecessarily looks at each & every pixels (testing each pixel against each triangle)
	![[Pasted image 20250131135719.png]]

==Better:== iterate through each triangle & determine which pixels it overlaps
	instead of performing point-in-triangle test, treat the images as a set of rows 
	![[Pasted image 20250131140344.png]]

#### Bounding Box
>compute the axis-aligned bounding box of each triangle
>	find min & max XYZ coordinates
>![[Pasted image 20250131140702.png]]

#### Intersection Testing
![[Pasted image 20250131140756.png]]

![[Pasted image 20250131140824.png]]
	x = (p1.y - q1.y + m * q1.x) / m

#### Overlapping Triangles 
>Multiple triangles will overlap the same pixels 
>	==Solution:== [[Painter's Algorithm]] (per-pixel basis)
>		![[Pasted image 20250131143733.png]]
>	use [[Z-Buffering]]