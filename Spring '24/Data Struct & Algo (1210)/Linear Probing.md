$$h(k,i) = (h'(k) + i) \text{ mod } m$$
>given [[Auxiliary Hash Function]] $h'$
>key $k$ $\rightarrow$ probe $T[h'(k)]$ (the slot given by [[Auxiliary Hash Function]]) $\rightarrow$ next probe slot $T[h'(k) + 1]$ and the next until we reach slot $T[m-1]$ $\rightarrow$ wrap around to slots $T[0],T[1],\dots$ until we finally probe slot $T[h'(k) -1]$ 
>**Pros:** easy to implement
>**Cons** does not work well in practice due to [[primary clustering]] 
>==How it Looks:== https://www.youtube.com/watch?v=98Y0UDZ9vvs&t=204s&ab_channel=VisualHow
