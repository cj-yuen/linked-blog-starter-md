![[Pasted image 20241115230257.png]]
>identify the instruction, registers used, any constants 
- many instructions are grouped into categories (arithmetic, logical, shift instructions...)
	[[Op-codes]] identifies this group

![[Pasted image 20241115230704.png]]


## [[Register-Type (R-type)]] Example: Op-code, Funct3, Funct7
![[Pasted image 20241115230549.png]]
>**Opcode:** 0110011 (R-Type & Arithmetic Group)
>**funct3 & funct7:** all 0's


## [[Immediate-Type (I-type)]] Example:
![[Pasted image 20241115231048.png]]
>**Opcode:** 0x03 (I-Type & Load Group)
>**funct3:** 0b010 (word size load)
>**Destination:** 0b01001 (x9)
>**Register Source 1:** 0b10100 (x20)
>**immediate:** 4


## [[Store-Type (S-type)]] Example:
![[Pasted image 20241115233246.png]]

## Other Types:
![[Pasted image 20241115233606.png]]

