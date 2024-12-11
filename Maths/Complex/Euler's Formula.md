---
tags:
  - ComplexNumbers
  - Maths
---
---

# What is it? 

Euler's formula, $e^{i\pi} + 1 = 0$, commonly referred too as the *"Most Beautiful Equation In Maths"*, was discovered by Leonard Euler in the early 1700s. It has been adapted over the years into the more descriptive: 
$$e^{i\theta} = \cos \theta + i \sin \theta$$
Where $\theta$ is an angle in radians. 

# Derivation of the Formula

The formula has many ways to be derived, but the most common stems from the substitution of $ix$ into the [[McLaurin Series| McLaurin]] series of $e^x$.  Which coincidentally, results in $\cos \theta + i \sin \theta$. 

$$
e^x = \sum_{n=0}^{\infty} \frac{1}{n!}x^n
$$

# Uses

As a result of no real coefficient acting on the $e^{i\theta}$, the absolute distance between the complex point and the origin will **ALWAYS** be $1$. This begets the definition of the unit circle. 

When a coefficient is given to a number in polar form, that functions as the scalar that multiplies the magnitude of the displacement from the origin. For instance:

``` tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]
\draw[thin,color=gray] (0,0) grid (6,6);
\draw[<->, color=gray] (0,3) -- (6,3);
\draw[<->, color=gray] (3,0) -- (3,6);
\draw (3,3) circle (1);

\node[anchor=west] at (6,3) {$+\mathbb{R}$};
\node[anchor=east] at (0,3) {$-\mathbb{R}$};
\node[anchor=south] at (3,6) {$+\mathbb{I}$};
\node[anchor=north] at (3,0) {$-\mathbb{I}$};

\node[anchor=south west] at (3.717, 3.717) {$\frac{\sqrt{2}}{2}+\frac{\sqrt{2}}{2}i$};
\filldraw (3.717, 3.717) circle (0.1);

\draw (3.717, 3.717) -- (3,3);

\end{tikzpicture}
\end{document}
```
As seen above, the point lies on the Unit Circle, giving it a modulus of one; the argument of the number, or its phase; can be found form the equation $\theta = \arctan ( \frac{\Im}{\Re})$. 

