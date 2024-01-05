## Moment Generating Function of Normal Distribution
The moment generating function is defined as:

$$
M_z(t) = E[e^{tZ}]
$$

Suppose $Z \sim N(0,1):$

$$
\begin{split}
M_Z(t) = E[e^{tZ}] = \underbrace{\int e^{tz} \cdot \frac{1}{\sqrt{2 \pi}}e^{-\frac{z^2}{2}} dz}_{E(X) = \int x \cdot f_X(x)dx} \\
= \int \frac{1}{\sqrt{2 \pi}}e^{-\frac{z^2+2tz}{2}}dz
\end{split}
$$

To compute this integral, we have to complete the square:

$$
\begin{split}
M_Z(t) = \int \frac{1}{\sqrt{2 \pi}}e^{-\frac{z^2+2tz}{2}}dz = \int \frac{1}{\sqrt{2 \pi}} e^{\frac{z^2+2tz-t^2}{2} + \frac{t^2}{2}}dz \\
= e^{\frac{t^2}{2}} \underbrace{\int \frac{1}{\sqrt{2 \pi}} e^{-\frac{(z-t)^2}{2}}dz}_{z(t,1) \text{ integrates to 1}} = e^{\frac{t^2}{2}}
\end{split}
$$

Now further suppose that we want the non-standard normal distribution, i.e., $X \sim N(\mu, \sigma^2)$.

Knowing that $Z = \frac{x-\mu}{\sigma}$ then $X = \mu + \sigma Z$

$$
\begin{split}
M_X(t) = E[e^{tX}] = E[e^{t\mu} \cdot e^{t\mu Z}] \\
= e^{\mu t}E[e^{\mu t Z}] \\
= e^{\mu t} \cdot M_{Z}(\sigma t) \\
= e^{\mu t} e^{\frac{\sigma^2 t^2}{2}}
\end{split}
$$


**Reference**
- [Lecture 2](https://web.stanford.edu/class/archive/stats/stats200/stats200.1172/Lecture02.pdf), Statistics 200: Introduction to Statistical Inference (Zhou Fan, Stanford University, Autumn 2016)

