## ie. Prove that for all ints $n\geq 1$ 
$$\sum_{i=1}^n i = \frac{n(n+1)}{2}$$
>Induction on n 
>	**Induction Hypothesis (I.H.):** Assume that the claim is true when $n=k$, for some int $k \geq 1$. In other words assume that $$\sum_{i=1}^k i = \frac{k(k+1)}{2}$$
>	**Base Case (BC):** $n=1$. $$\begin{align*}\sum_{i=1}^1 i &= \frac{1(2)}{2} \\ 1 &= \frac{2}{2} \end{align*}$$ The claim holds true for the base case. 
>	**Induction Step (I.S.):** Prove the claim holds true for $n=k+1$. In other words, show that $$\sum_{i=1}^{k+1} = \frac{(k+1)(k+2)}{2}$$ By the following $$\begin{align*} \sum_{i=1}^{k+1} i &= \sum_{i=1}^{k} i + (k+1) \\ &= \frac{k(k+1)}{2}+k+1 \quad \text{by I.H.} \\ &= \frac{k(k+1) + 2(k+1)}{2} \\ &= \frac{(k+1)(k+2)}{2} \end{align*}$$

