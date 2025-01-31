>store the Z-coordinate of the portion of the triangle that is overlapped
>	stored as part of the a <u>data bundle</u> known as [[Fragments]]
>iterate through each pixel & use its [[Fragments]] to determine its colors

## Solutions
==Easiest:== use the color of the fragment w/smallest Z-coordinate

==Transparency:== sort [[Fragments]] by depth & combine colors based on transparency


## Problems
![[Pasted image 20250131144234.png]]
