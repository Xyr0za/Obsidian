---
tags:
  - tag
---
---

# Examples of an Argand Diagram?

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[thin, color=gray, ->] (-6,0) -- (6,0) node {$\Re$};
\draw[thin, color=gray, ->] (0, -6) -- (0,6) node {$\Im$};

\filldraw (2,2) circle (0.07) node[anchor=south] {A};
\filldraw (3,2) circle (0.07) node[anchor=south] {E};
\filldraw (0,2) circle (0.07) node[anchor=south] {C};
\filldraw (1,-3) circle (0.07) node[anchor=south] {G};
\filldraw (-3,-2) circle (0.07) node[anchor=south] {D};
\filldraw (-3,0) circle (0.07) node[anchor=south] {H};
\filldraw (-5,2) circle (0.07) node[anchor=south] {B};
\filldraw (3,-2) circle (0.07) node[anchor=south] {F};



\end{tikzpicture}
\end{document}
```
