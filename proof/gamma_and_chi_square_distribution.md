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


