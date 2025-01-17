#theorems 

>given an [[Open Addressing]] hash table w/[[Load Factor]] $\alpha = \frac{n}{m} < 1$, the expected # of probes in an unsuccessful search is $\le \frac{1}{1-\alpha}$ assuming [[Uniform Hashing Assumption (UHA)]]

$$\begin{align*}
\mathbb{E}(X) &= \sum_{i=1}^{\infty} Pr[X \ge i] \\
&= \sum_{i=1}^{\infty} \alpha^{i-1} \\
&= \sum_{i=0}^{\infty} \alpha^i \\
&= \frac{1}{1-\alpha}
\end{align*}$$
