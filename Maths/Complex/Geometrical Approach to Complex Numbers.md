---
tags:
  - Maths
  - ComplexNumbers
---
---

#  What is an Argand Diagram?

An Argand Diagram is a way of representing complex numbers; consisting of the normal cartesian plane. Albeit one key difference, instead of $x,y$, the diagram plots $\mathbb{R}$ against $\mathbb{I}$.

$z=x + iy$

We can use a set of axes where $x$ and $y$ give a coordinate of an imaginary set of axes.

$$
 \begin{pmatrix}
x \\ y
\end{pmatrix} \in \mathbb{R}
$$

Argand diagrams are useful for visualising the complex plane, and the cyclical nature of certain complex numbers, especially the roots of unity.

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[thin] (0,0) grid (6,6);

\draw[thin] (3,3) circle (1);

\draw[thin] (3,3) -- (3.717, 3.717);

\filldraw[color = red] (6,1) circle (0.1) node[anchor=west] {$z$};
\filldraw[color = green] (2,6) circle (0.1) node[anchor=south] {$w$};

\filldraw[color = red] (6,+5) circle (0.1) node[anchor=west] {$z*$};
\filldraw[color = green] (2,0) circle (0.1) node[anchor=north] {$w*$};

\node[anchor=west] at (6,3) {$+\mathbb{R}$};
\node[anchor=east] at (0,3) {$-\mathbb{R}$};
\node[anchor=south] at (3,6) {$+\mathbb{I}$};
\node[anchor=north] at (3,0) {$-\mathbb{I}$};

\node[anchor = north east] at (3,3) {$(0,0)$};

\end{tikzpicture}
\end{document}
```
Additionally, it may be beneficial to think of complex numbers as vectors; this provides a useful explanation as to how the addition of complex numbers works. Furthermore, it aids in the explanation of Realisation, with the [[Complex Conjugate]] and [[Polar Form]].

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

\filldraw[color = gray] (5,4) circle (0.1) node[anchor = south] {$z_1$}; 
\filldraw[color = gray] (2,2) circle (0.1) node[anchor = south] {$z_2$};
\filldraw[color = gray] (4,3) circle (0.1) node[anchor = south] {$z_{1} + z_{2}$};

\draw[->] (3,3) -- (5,4);
\draw[->] (3,3) -- (2,2);
\draw[->] (2,2) -- (4,3);

\end{tikzpicture}
\end{document}
```


For which non-negative integers $a$ and $b$ is the triangle in the Argand diagram with corners $z,w$ and $z+w$ isosceles?

```tikz
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

\filldraw[color = gray] (5,4) circle (0.1); 
\filldraw[color = gray] (1,2) circle (0.1);
\filldraw[color = gray] (3,3) circle (0.1);

\draw[->] (3,3) -- (5,4);
\draw[->] (3,3) -- (1,2);
\draw[->] (1,2) -- (5,4);

\end{tikzpicture}
\end{document}
```
