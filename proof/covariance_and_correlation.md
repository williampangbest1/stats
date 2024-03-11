## Covariance and Correlation
The definition of covariance is defined as:

$$
Cov(X,Y) = E[(X-\mu_x)(Y-\mu_y)]
$$

In other words, the covariance tells us the average value of the product of the deviation of X from its mean and Y from its mean.

We can also partition the covariance into expected values:

$$
\begin{split}
Cov(X,Y) 
&= E(XY-X\mu_Y-Y\mu_X+\mu_X\mu_Y) \\
&= E(XY) - \underbrace{E(X)\mu_Y - E(Y)\mu_X}_{E(X) = \mu_X \text{ and } E(Y) = \mu_Y} + \mu_X\mu_Y \\
&= E(XY) - \mu_X\mu_Y \\
&= E(XY) - E(X)E(Y)
\end{split}
$$

The correlation coefficient can also be defined in terms of covariance:

$$
\rho = \frac{Cov(X,Y)}{\sigma_X \sigma_Y}
= \frac{Cov(X,Y)}{\sqrt{Var(X)Var(Y)}}
$$

Also note that the correlation is invariant to rescaling, i.e.:

$$
corr(aX,bY) = corr(X,Y) 
$$

**References**
- The Book of Statistical Proofs: [Partition of covariance into expected values](https://statproofbook.github.io/P/cov-mean)
