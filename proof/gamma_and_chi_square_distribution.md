## Gamma and Chi-Squared Distribution
### Moment Generating Function of Gamma Distribution
Suppose $X \sim \text{Gamma}(\alpha, \beta)$ for $\alpha, \beta > 0 $:

$$
\begin{split}
M_X(t) 
&= E[e^{tX}] \\
&= \int_{0}^{\infty}e^{tx}\frac{\beta^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1}e^{-\beta x}dx \\
&= \int_{0}^{\infty}\frac{\beta^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1}e^{(t-\beta) x}dx \\
\end{split}
$$

If $t > \beta$:

$$
\lim_{x \to \infty} x^{\alpha-1}e^{(t-\beta)x} = \infty
$$

If $t = \beta$:

$$
\int_{0}^{\infty}x^{\alpha-1}dx = \frac{1}{\alpha}x^{\alpha}\bigg|_0^\infty = \infty
$$

For $t < \beta$, we want to isolate the PDF of the Gamma($\alpha, \beta-t$) distribution:

$$
\begin{split}
M_X(t) 
&= \int_{0}^{\infty}\frac{(\beta - t)^{\alpha}}{\Gamma(\alpha)}\cdot \frac{\beta^{\alpha}}{(\beta - t)^{\alpha}}x^{\alpha-1}e^{-(\beta-t)x}dx \\
&= \frac{\beta^{\alpha}}{(\beta - t)^{\alpha}} \underbrace{\int_{0}^{\infty}\frac{(\beta - t)^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1}e^{-(\beta-t)x}dx}_{=1}
\end{split}
$$

Thus, if $t \geq \beta$:

$$
M_X(t) = \infty
$$

if $t < \beta$:

$$
\begin{split}
M_X(t) = \frac{\beta^{\alpha}}{(\beta-t)^{\alpha}}
&= (\frac{\beta}{\beta-t})^{\alpha}
&= (\frac{\beta-t}{\beta})^{-\alpha}
&= (1-\frac{1}{\beta}t)^{-\alpha}
\end{split}
$$

### Gamma Distribution with 1 Degree of Freedom

The Chi-squared distribution with 1 degree of freedom is the Gamma($\frac{1}{2}, \frac{1}{2}$) distribution. First, let's suppose that $X_1, ... , X_n \stackrel{IID}{\sim} N(0, 1)$, and we want to derive the distribution of the statistic $X_1^2 + ... + X_n^2$. 

By independence of $X_1^2, ... , X_n^2$,

$$
M_{X_1^2 + ... + X_n^2}(t) = M_{X_1^2} \times ... \times M_{X_n^2}
$$

Since they are independent, we compute each $X_i$ its MGF:

$$
M_{X_i^2}(t) = \mathbb{E}[e^{tX_i^2}] = \int e^{tx^2} \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}dx = \int \frac{1}{\sqrt{2\pi}}e^{(t-\frac{1}{2})x^2}dx
$$

As with before, when $t \geq \frac{1}{2}$, then $M_{X_i^2}(t) = \infty$. When $t < \frac{1}{2}$:

$$
\begin{split}
M_{X_i^2}(t) = \int \frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}(1-2t)x^2}dx
\end{split}
$$  

Note that this looks similar to the normal distribution. Recall that the normal distribution has a PDF of:

$$
\begin{split}
\mathcal{N}(\mu, \sigma^2) = \frac{1}{\sigma \sqrt{2\pi}}e^{-\frac{1}{2} \frac{(x-\mu)^2}{\sigma^2}}
\end{split}
$$

So:

$$
\begin{split}
\mathcal{N}(0, \frac{1}{1-2t}) = \sqrt{\frac{1-2t}{2\pi}}e^{-\frac{1}{2} (1-2t)x^2}
\end{split}
$$

We can now try and "fit" $\mathcal{N}(0, \frac{1}{1-2t})$ into $M_{X_i^2}(t)$, resulting in:

$$
\begin{split}
M_{X_i^2}(t) = \frac{1}{\sqrt{1-2t}} \underbrace{\int \sqrt{\frac{1-2t}{2 \pi}}e^{-\frac{1}{2} (1-2t)x^2}dx}_{=1}
\end{split}
$$  

Thus, for $M_{X_i^2}(t)$ when $t \geq \frac{1}{2}, M_{X_i^2}(t) = \infty$, and when $t<\frac{1}{2}$, $M_{X_i^2}(t) = (1-2t)^{-1/2}$

Then for the sampling distribution:

$$
\begin{split}
M_{X_1^2 + ... + X_n^2}(t) = M_{X_1^2} \times ... \times M_{X_n^2} \\
&\text{for } t \geq \frac{1}{2} = \infty \\
&\text{for } t < \frac{1}{2} = (1-2t)^{-n/2}
\end{split}
$$


