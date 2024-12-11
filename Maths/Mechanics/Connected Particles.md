---
tags:
  - Mechanics
  - Maths
  - Calculus
---
---

# What are connected particles?

# Example Questions

## Question 1

Most of these questions rely on [[Newtons Laws]] and [[SUVAT]] to be able to solve, with slight bits of reference to [[Calculus]] for variable acceleration questions. 

A car of mass 1400 kg pulls on a trailer of mass 600 kg attached with a towbar. The resistance force acting on the car is 190N while the force that acting on the trailer is 150N. Given that the driving force of the car is 600N, calculate the tension in the tow bar.

``` tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:8]

\draw[line width=0.6mm] (0,0) -- (0,1) -- (1,1) -- (1,0) -- cycle;
\draw[line width=0.6mm] (3,0) -- (3,1) -- (4,1) -- (4,0) -- cycle;

\draw[line width=0.7mm, ->] (0,0.5) -- (-1.5,0.5) node[anchor=south] {$150N$};
\draw[line width=0.7mm, ->] (4,0.5) -- (6,0.5) node[anchor=south] {$600N$};

\draw[line width=0.6mm,<->] (3,0.5) -- (1,0.5);
\node[anchor=south] at (2,0.5) {$T$};
 
\end{tikzpicture}
\end{document}
```

## Question 2 

A box of mass 4kg sits at rest on a smooth horizontal surface. A force of $P \, N$  is applied to the box at an angle of $30 \deg$ to the horizontal causing the particle to move 1m5 in the first 5 seconds. 

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width = 0.7mm] (-2,0) -- (2,0);
\draw[line width = 0.7mm] (-1.5,0) -- (-1.5, 1.5) --(1.5, 1.5) -- (1.5,0);

\node at (0, 0.75) {$M$};

\draw[line width=1mm, dotted] (1.5, 0.75) -- (3.5, 0.75);
\draw[line width=0.7mm] (1.5, 0.75) -- (3.5, 2.75);

\node at (-2, 2.75) {$4ms^{-2} \rightarrow \rightarrow$};

\node[anchor = south west] at (3.5, 2.75) {$30 N, 40 \, \theta$};

\end{tikzpicture}
\end{document}
```

##  Question 3

Two particles A and B have mass $2kg$ and $m \, kg$ respectively, where $m <2$. The particles are connected by a light inextensible string which passes over a smooth, fixed pulley. Initially A is $3m$ above horizontal ground. The string is released from the rest with the string taut and the hanging parts of the string vertical.

After A has been descending for $2.5s$ it strikes the ground. Particle A reaches the ground before B reaches the pulley. 

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width=0.7mm] (0,0) circle (1);
\draw[line width=0.7mm] (1,0) -- (1, -4);
\draw[line width=0.7mm] (-1,0) -- (-1, -3);

\filldraw (-1, -3.5) circle (0.5);
\filldraw (1, -4.3) circle (0.7);

\node[anchor = north] at (-1, -4) {$A (2 \, kg)$};
\node[anchor = north] at (1, -5) {$B (m \, kg)$};

\end{tikzpicture}
\end{document}
```