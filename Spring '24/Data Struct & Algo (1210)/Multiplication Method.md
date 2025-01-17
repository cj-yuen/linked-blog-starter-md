$$h(k) = \lfloor m (kA \text{ mod } 1 \rfloor$$
>multiply key $k$ by constant $A$ ($0 < A < 1$) $\rightarrow$ extract fractional part of $kA$ $\rightarrow$ multiply this value by $m$ $\rightarrow$ floor result
>**Pro:** value of $m$ is not important 
>	typically choose a power of 2 ($m = 2^p$ for some int $p$)
>empirically best value for constant $A \approx \frac{\sqrt{5}-1}{2} = 0.6180339887\dots$ 

