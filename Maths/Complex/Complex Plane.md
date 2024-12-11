---
tags:
  - Maths
  - ComplexNumbers
---
---

# What is the complex plane?

The complex plane is a plan on which complex numbers can be plotted, the $y$ axis of the plane is referred too as the imaginary axis and appears as a rotation of the real number line by 90 degrees.

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

\node[anchor=south west] at (3.717, 3.717) {Unit Circle};

\filldraw[color=gray] (2,4) circle (0.1);
\node[anchor=south] at (2,4) {$-1 + i$};

\draw (2,4) -- (3,3);
\draw (2,2) -- (3,3);

\filldraw[color=gray] (2,2) circle (0.1);
\node[anchor=north] at (2,2) {$-1 - i$};

\end{tikzpicture}
\end{document}
```
*Fig 1: The Complex Plane*


# Explained

The circle centred around the origin is the unit circle, all points along it are equidistant from the origin; see [[Polar Form]] and [[Euler's Formula]].