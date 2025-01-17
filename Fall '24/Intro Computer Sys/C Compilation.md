## Simplest Compilation
```C
clang-15 example.c
```
>default produces executable called: `a.out`
>	run executable by: `./a.out` 
>		if in directory "test" do: `./test/a.out`
>			first `.` = "start looking in curr directory"


## Options
### Compilar Flag `-o`
>specify what output should be called 
>	ie. compile file `hello.c` $\rightarrow$ executable called `hello` do: `clang-15 -o hello hello.c`

### Debugger `-g3`
>have compiler output maximum debugging info
>to turn on "all" warning use: `-Wall` (==W==arnings ==all==)

### Together
```C
clang-15 -g3 -Wall -o hello hello.c
```
