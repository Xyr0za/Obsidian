---
tags:
  - Maths
  - Calculus
---
---

# What is the Chain Rule? 

The Chain Rule is one of the fundamental rules of [[Differentiable Calculus|differentiation]], it allows for mathematicians to calculate the derivative of composite functions, take for example $\sin{(x^{2})}$. The rule states as follows: 
$$
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
$$

One such popular usage of the rule includes [[Implicit Differentiation]], where it is possible to differentiate $y$ with respect to $x$.

# How does it work? 
First let us define our example function, $f(x) = \sin{x^{2}}$. As can  be seen, $x^{2}$ is a composite part of the function, being situated inside the sin function. We define this inner function as being $u$. Following this definition, we then integrate $u$ with respect to x; in this case leaving us with $2x$. 
We may then differentiate $\sin u$ with respect to $u$, this gives us $-\cos u$. We then multiply these two numbers, and resubstitute $u$ with $x^{2}$. Finally we get, $f'(x) = -2x \cos{(x^{2})}$ as our derivative for the function. 