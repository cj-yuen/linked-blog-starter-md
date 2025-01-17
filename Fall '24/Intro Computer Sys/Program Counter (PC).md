>special register that keeps track of the address of the current instruction executing
>	![[Pasted image 20241115231806.png]]
>every instruction increments the [[Program Counter (PC)]] 


## Accessing the Program Counter 
### auipc rd, imm20
**rd** - register contains the result
**imm20** - 20 bit immediate
![[Pasted image 20241115232036.png]]


### jalr rd, imm12(rs1)
**rd** - register that contains pc + 4 (next instruction)
**imm12** - 12 bit immediate 
**rs1** - base address
![[Pasted image 20241115232257.png]]

