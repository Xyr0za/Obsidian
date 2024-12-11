---
tags:
  - Maths
  - Calculus
---
---

# What is Definite Integration?

Definite integration is a form of integration characterised by the bounds present on the integral symbol, $\int^{b}_{a} \, dx$ . With $a$ being the lower bound of integration, and $b$ being the upper bound.

A common way of visualising definite integral is the idea of area present under a curve; see Figure 1 Below for an example.

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width=0.6mm] (0,0) grid (4,4);  
\draw[line width=0.6mm] (2,0) plot (\x, \x) node[anchor=south] {$f(x) = x$};

\filldraw[opacity=0.2, color=red] (0,0) -- (4,4) -- (4,0) -- cycle;

\end{tikzpicture}
\end{document}
```


*Figure 1: A Definite Integral over the graph of f(x)*

Notice how the red area below the line $f(x)$ can be valued at $8$ square units below the curve, but this can also be found from Definite Integration. 

Let $f(x) = x$,  $\int^{4}_{0} f(x) \, dx = \left [\frac{x^2}{2} \right ]^{x=4}_{x=0} = \frac{4^{2}}{2} - \frac{0^2}{2} = 8$.

As seen above, Indefinite Integration does *NOT* end with a $+c$ constant term, as that is a property unique to the [[Indefinite Integration|Anti-Derivative]]. 