## Sampling the Normal Distribution
Consider a population which follows the normal distribution $X$ with mean $\mu$ and variance $\sigma^2$:

$$
X \sim N(\mu, \sigma^2)
$$

Now suppose you want to draw *n* random samples from the population (of mean $\mu$ and variance $\sigma^2$) and find the sampling distribution. 

### Using Expectations
$$
\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i
$$

Taking advantage of the linearity of expectations, we get:

$$
\begin{split}
\mathbb{E} (\bar{X}) = \mathbb{E} (\frac{X_1+X_2+... +X_n}{n})\\
= \frac{1}{n}\mathbb{E} (X_1 + X_2 + ... X_n) \\
= \frac{1}{n}[\mathbb{E} (X_1) + \mathbb{E} (X_2) + ... \mathbb{E} (X_n)]\\
= \frac{1}{n}(\mu_1 + \mu_2 + ... + \mu_n) \\
= \frac{n\mu}{n} = \mu
\end{split}
$$


Similarly, the variance can be found by:

$$
\begin{split}
Var(\bar{X}) = Var(\frac{X_1 + X_2 + ... X_n}{n}) \\
= \frac{1}{n^2}(Var(X_1 + X_2 + ... X_n)) \\
= \underbrace{\frac{1}{n^2}[Var(X_1) + Var(X_2) + ... Var(X_n)]}_{\text{Assuming i.i.d.}} \\
= \frac{1}{n}[\sigma_1^2 + \sigma_2^2 + ... \sigma_n^2]\\
= \frac{1}{n^2}[n\sigma^2] = \frac{\sigma^2}{n}
\end{split}
$$
