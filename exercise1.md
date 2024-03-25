# 1

$R(\alpha)$ is known as an alpha risk or as a type 1 error or as a false positive. This means an incorrect classification as poitive while the actual class was negative.

Risk is given by $R(\alpha) = \int \int L(y, x, \alpha) \cdot p(y, x) \, dy \, dx$ (Machine Learning: a Probabilistic Perspective, 7.36)
For our use case we can write the risk as following:
$$\begin{align*}
R(\alpha) = \int_{-3}^{3} \int_{2x-0.5}^{2x+0.5} (y - \alpha x)^2 \cdot p(y|x) \, dy \, dx \\
= \int_{-3}^{3} \int_{2x-0.5}^{2x+0.5} (y - \alpha x)^2 \cdot \frac{1}{1} \, dy \, dx \quad \text{(since \(p(y|x)\) is uniform)} \\
= \int_{-3}^{3} \left[ \frac{(y - \alpha x)^3}{3} \right]_{2x-0.5}^{2x+0.5} \, dx \\
= \int_{-3}^{3} \left[ \frac{(2x + 0.5 - \alpha x)^3 - (2x - 0.5 - \alpha x)^3}{3} \right] \, dx
\end{align*}$$