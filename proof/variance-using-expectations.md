## Deriving Variance from Expectations
Consider the standard deviation equation that we all know:

$$
\sigma=\sqrt{\frac{\sum_{i} (x_{i} - \mu)^2}{n}}
$$

The variance is simply the square of the standard deviation, which can be re-written as:

$$
Var(X)=\frac{\sum_{i} (x_{i} - \mu)^2}{n} = E[(X-\mu^2)]
$$

Note that we could also have defined $Var(X)$ as $E[(X-E(X))^2]$. The problem here is that 
dealing with squares are often complicated. We can separate $X$ and $E(X)$ from the squaring operation
as follows:

$$
\begin{split}
Var(X) = E[(X-\mu)^2] \\
= E[X^2-2X\mu+\mu^2] \\
= E[X^2]-2E[X]\mu + \underbrace{E[\mu^2]}_{E[c] = c} \\
= E[X^2]-2\mu^2+\mu^2 \\
= E[X^2]-\mu^2
\end{split}
$$

We can re-write the last line as:

$$
Var(X) = E[X^2]-E[X]^2
$$

