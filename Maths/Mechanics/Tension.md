---
tags:
  - tag
---
---

# What is Tension?

Tension is contact force that acts upon an object, typically stretching it. It is commonly found in pulley systems, and anything that goes against gravity. Some examples of commonly tensioned objects includes: pulleys, bridges, and car tows.

---


``` tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width=0.5mm] (-2.5,0) -- (2.5, 0);
\draw[line width=0.5mm] (-2,0) -- (-2,1) -- (-1,1) -- (-1,0) --cycle;
\draw[line width=0.5mm] (2,0) -- (2,1) -- (1,1) -- (1,0) --cycle;
\draw[line width=0.5mm, -stealth reversed] (-1, 0.5) -- (1, 0.5);
\draw[line width=0.5mm, -stealth reversed] (1, 0.5) -- (-1, 0.5);
\draw[->, line width=0.5mm] (0,2) -- (0,0.75);
\node[anchor = south] at (0,2) {$T_{ension}$};

\draw[->, line width=0.5mm] (-2,0.5) -- (-3,0.5);
\draw[->, line width=0.5mm] (2,0.5) -- (3,0.5);

\end{tikzpicture}
\end{document}
```

---
