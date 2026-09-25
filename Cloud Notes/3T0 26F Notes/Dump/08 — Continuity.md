---
updated_at: 2026-09-25T12:46:39.464-04:00
edited_seconds: 270
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 8
Lecture Date: 2026-09-23
Week:
Created: September 23rd 2026, 4:21:26 pm
---
Hub: [[ESC194 Hub]]
Previous: [[07 — Limit Laws]]
Next: N/A
> [!quote] Recommended Reading 
> 1.8 in the Stewart Textbook, 3.3 of the Supplemental. 
--- 
# Lecture Notes
# Pre-Lecture Notes
## Continuity 
The concept of continuity can be generally defined as the idea of "not lifting your hand from the page". Mathematically however, this is defined as the following: 

> [!theorem] Continuity
> A function $f(x)$ is continuous at $x=c$ if and only if: $$\lim_{ x \to c } f(x) = f(c)$$

That is, a function is both defined at it's limit, and that it's limit converges onto this point. In terms of Epsilon Delta: 
$$\forall\delta, \exists\epsilon >0 \text{ s.t. } |x-c| < \delta \implies |f(x) - f(c)| < \epsilon$$
This has some interesting properties. Given two continuous functions $f$ and $g$: 
* $f+g$ will result in some continuous function. 
* $fg$ will result in some continuous function. 
* $\frac{f(x)}{g(x)}$ will be continuous in all of it's domain with the exception of $g(x) = 0$. 

### Polynomials
Note that Polynomials are continuous in all of it's domain, that is $x\in \mathbb{R}$ for any polynomial. This arises from our [[07 — Limit Laws|Limit Laws]]: 
Given the following polynomial: 
$$
f(x) = c_{1}x^n + c_{2}x^{n-1} + \dots + c_{n}x^0
$$
Taking the limit of this for some arbitrary value $a \in x$, then: 
$$
\lim_{ x \to a } f(x) = \lim_{ x \to a } c_{1}x^n + c_{2}x^{n-1} + \dots + c_{n}x^0
$$
Recall that: 
$$
\lim_{ x \to a } c_{1} = c_{1}
$$
And 
$$
\lim_{  x \to a } x^n = a^n \iff n\in \mathbb{N}
$$
Since both of these are continuous, and that a polynomial is the sum of these polynomial functions, then it arises that any polynomial is continuous along it's entire domain. 

> [!theorem] Rational Functions
> From this, it also extends to the concept that rational functions are continuous everywhere in it's domain *with the exception of places in which the denominator resolves to a value of 0.*



