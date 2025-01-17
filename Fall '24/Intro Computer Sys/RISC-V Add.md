## C
```C
b = (a + 5)
a = a + b;
```

## RISC-V
```RISC-V
addi x6, x5, 5
add x5, x5, x6
```
### addi rd, rs1, imm12
- add **rs1** & **imm12 (12 bit immediate)** -> stored in **rd** 
- [[Immediate-Type (I-type)]] 

### add rd, rs1, rs2
- add 2 registers, **rs1** & **rs2** -> stored in **rd**
- [[Register-Type (R-type)]] 
