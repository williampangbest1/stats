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

To compute this integral, we have to complete the square

**Reference**
- [Lecture 2](https://web.stanford.edu/class/archive/stats/stats200/stats200.1172/Lecture02.pdf), Statistics 200: Introduction to Statistical Inference (Zhou Fan, Stanford University, Autumn 2016)

