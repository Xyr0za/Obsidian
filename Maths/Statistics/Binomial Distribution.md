---
tags:
  - tag
---
---

# What is the Binomial Distribution?

The Binomial Distribution is a field of statistics used in Probability, where it is used to calculate the results of binomial effects; "Win / Loss". The general formula for it can be seen below: 

$$
P(X_{n}) = \binom{i_{ters}}{r_{esult}} \cdot P(X)^{r_{esult}} \cdot (1-P(X))^{(I_{ters} - R_{esult})}
$$

Where $P(X_{n})$ is the chance that a result occurs $n$ amount of times over the total iterations; $i_{ters}$  is the total iterations that occur.  $r_{esult}$ is the amount of times the action is being checked for. 

# Derivation

The above formula may seem reminiscent of the [[Binomial Expansion]] as it uses said formula in its derivation; via the premises all independent exhaustive properties must sum to 1.

# Example 

Imagine a coin being flipped $n$ amount of times; it as has two possible states, $h,t$. Lets say we wish to predict the chance of the coin being in state $h$ after flipping $8$ times. 

While this can be trivially solved through $(2^{-1})^{8}= P(X)$, there is a more applied method that can be applicable to more complex questions; such as the probability of state $h$ arising thrice over $6$ iterations.

In this case we substitute into the formula: 



# More Questions

 The probability that Lee wins a game of darts is 0.3. Assuming that the outcome of each game is independent calculate the probability that Lee wins exactly 4 games out of 15.

Starting off we can define $i_{ters}$ as being 15 and $r_{esult}$ as being 4. Following these definitions we can see that $P(X) = 0.3 \implies P(X') = 0.7$. Where $P(X') = 1 - P(X)$. We may then substitute these numbers into the binomial distribution theorem. 

$$
\binom{15}{4} \cdot 0.3^{4}\cdot 0.7^{15} = P(X_{n}) = 0.219
$$

# Continuous Expansion of the formula
$$
f(x) = \frac{n!}{\left(n-x\right)!x!}\cdot p^{x}\cdot\left(1-p\right)^{\left(n-x\right)}
$$
