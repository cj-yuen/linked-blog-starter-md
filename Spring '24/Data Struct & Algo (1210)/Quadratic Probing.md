$$h(k,i) = (h'(k) + c_1 i + c_2 i^2) \text{ mod } m$$
>given [[Auxiliary Hash Function]] $h'$, positive auxiliary constant $c_1$ & $c_2$, and $i=0,1,\dots, m-1$ 
>initial probe $T[h'(k)]$ $\rightarrow$ later positions probed by amounts that depend in a quadratic manner on the probe # $i$ 
>**Pros:** better than [[Linear Probing]] 
>**Cons:** $c_1, c_2, m$ are constrained & [[secondary clustering]] 
>==How it looks:== https://www.youtube.com/watch?v=0CFJAkpnhBg&ab_channel=VisualHow

