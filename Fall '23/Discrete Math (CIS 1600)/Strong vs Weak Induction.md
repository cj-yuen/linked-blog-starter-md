## Strong Induction Structure 
**Want to Prove:** a statement $P(n)$ that involves $n$ is true for all $n \geq n_0$ 

**Base Case:** Show that $P(n_0)$ is true (maybe for other values of $n$)

**Induction Hypothesis:** Assume $P(j)$ is true $\forall$ ints $j$ | $n_0 \leq j \leq k$, for some int $k\geq m$ (where $m$ is the largest base case) 

**Induction Step:** Show that $P(k+1)$ is true using IH

## Weak vs Strong Induction
when the induction step (proving that $P(k+1)$ is true) requires that the claim be true for values of $n$ less than $k$ 

## Need Multiple Base Cases
when the induction step (proving that $P(k+1)$ is true) requires that the claim be true for specific values of $n$ less than $k$ (relative to $k+1$; ex $k-1$, $k-2$) 

## Tips for Induction Step 
- write out a WTS (what we want to show)
- try to reach a situation where the IH can be used 
- expand out operators ($\sum$, $\Pi$, $\cup$, $\cap$, !)
- for group, try to form a group of $k$ (or less than $k+1$ for strong induction)