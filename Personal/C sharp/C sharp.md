#language 

## Differences w/[[(dot) NET]]
| **C#**               | **.NET**                              |
| -------------------- | ------------------------------------- |
| programming language | framework for building apps (Windows) |

## How it works 
C# $\rightarrow$ [[Intermediate Language (IL) Code]] $\rightarrow$ Native Code
![[Pasted image 20240523152401.png]]
- [[Just-In-Time Compilation (JIT)]] = process of [[Intermediate Language (IL) Code]] $\rightarrow$ Native Code

## Concepts
- [[Overflowing]] 
	by default no overflow checking

```C#
checked 
{
	byte number = 255; 
	number = number + 1;
}
```
	overflow will not happen @runtime & an exception will be thrown

- [[Scope]]

## Code Snippets in Visual Studio
| Shortcut | Code                  |
| -------- | --------------------- |
| cw       | `Console.WriteLine()` |

## Type Conversion
- [[Implicit Type Conversion]] 
- [[Explicit Type Conversion (Casting)]]
- [[Non-Compatible Type Conversion]] 