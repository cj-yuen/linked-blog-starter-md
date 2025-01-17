## RISC-V
```RISC-V
sw x5, 40(x6)   \\ *(x6 + 40) = x5
```

### sw rs2, imm12(rs1)
>rs2 - source register that contains what we'll store
>rs1 - source register containing base address in memory
>imm12 - 12 bit immediate offset from rs1
>[[Store-Type (S-type)]] 

### sh rs2, imm12(rs1)
>for ==half-word==


### sb rs2, imm12(rs1)
>for ==byte== 



