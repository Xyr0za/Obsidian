---
tags:
  - Maths
  - Calculus
---
---

#  What is a McLaurin Series?

A McLaurin series is an infinite series, as a simplified version of a [[Taylor Series]], that relies on a function being continuous at $0$. Its principles state that any function can be reconstructed into an infinite series, provided that enough local information exists for this to occur.


**MOST DISCRETE MATH FUNCTIONS ARE AN EXCEPTION TO THE RULE; CONTINUITY IS AN EXCEPTION NOT A STANDARD**


#  Definition
A McLaurin Series is defined as being being *the infinite sum of the nth [[Differentiable Calculus|derivative]] of f(x) evaluated at 0, multiplied by $x^n$*.  Or in mathematical notation as, 

$$
M(x) = \sum\limits^{\infty}_{n=0} \frac{{f^{(n)}(0)}}{n!}\cdot x^n
$$

where $f(x)$ is continuously differentiable at 0. 

# Examples

Some popular series include: 

$$\sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots = \sum_{n=0}^{\infty} (-1)^n \frac{x^{(2n+1)}}{(2n+1)!}$$
$$
\cos(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}
$$

$$
e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots = \sum_{n=0}^{\infty} \frac{x^n}{n!}
$$

# Some Important Uses

When substituting $ix$ into the McLaurin expansion of  $e^x$ ; we are left with both the expansion for $\cos x$ and $i\sin x$; which is a useful proof for [[Euler's Formula]] and the concepts of [[Polar Form]].