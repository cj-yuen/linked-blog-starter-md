## RISC-V
```RISC-V
lw x5, 40(x6)   // x5 = *(x6 + 40)
```

### lw dest, imm12(sr1)
>dest - destination register
>sr1 - address in memory (aka base register)
>imm12 - 12 bit immediate value offset from sr1
- loads a [[Word (RISC-V)]] of memory from location **sr1 + imm12**
- ==sign== extends to entire register width

#### Example:
<u>C code:</u> `int x = arr[1]`
	x stored in x5 
	array's address in x6
<u>RISC-V:</u> `lw x5, 4(x6)` 
	pointer arithmetic works in increments based on size of the type 
		array of ints, arr + 1 moves pointer by 1 int (4 bytes)
	same as `int x = *(arr + 1);`

### lhu dest, imm12(sr1)
- loads unsigned byte types 
- ==0 extends== entire register width

#### Example:
<u>C code:</u> `unsigned short x = arr[1];`
<u>RISC-V:</u> `lhu x5, 2(x6)`

  