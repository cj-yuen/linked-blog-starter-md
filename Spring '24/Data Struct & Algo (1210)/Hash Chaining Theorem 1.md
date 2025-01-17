#theorems 

>an <u>unsuccessful</u> search takes average-case time $\Theta(1 + \alpha)$ under the [[Simple Uniform Hashing Assumption (SUHA)]] 
>	average time to search for key $k$ is expected size of linked list $T[h(k)]$ 

$$\begin{align*}
\mathbb{E}[|T[h(k)]|] &= \sum_{i=1}^n Pr[X_i \text{ is mapped to }h(k)] \\
&= \sum_{i=1}^n \frac{1}{m} \\
&= \frac{n}{m} \\
&= \alpha

\end{align*}$$
