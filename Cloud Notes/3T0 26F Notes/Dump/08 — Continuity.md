---
updated_at: 2026-09-25T13:32:21.419-04:00
edited_seconds: 410
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
## Substitution Limits
There are limits in which you can directly substitute a value into a function to evaluate the limit. These normally arise during *rational inequalities* in which a denominator causes a division by 0 when the limit is taken. For instance: 
$$
\begin{align}
\lim_{ x \to 3 } \left(\frac{x^2-x-6}{x-3}\right) &=?&\text{Note that we can't distribute, limit would cause div by 0:}\\
\lim_{ x \to 3 } \left(\frac{x^2-x-6}{x-3}\right) &= \lim_{ n \to 3 } \left(\frac{(x-3)(x+2)}{x-3}\right) & \text{So we factor it: }\\
&=\lim_{ x \to 3 } (x+2)  \\
&= 5\end{align}$$

Another example: 
$$
\lim_{ x \to 5 } \frac{\sqrt{ x+4 }-3}{(x-5)}
$$
At this point, we can't use any of our rules. Let's try rationalizing the numerator by multiplying it by it's conjugate: 
$$
\begin{align}
\lim_{ x \to 5 } \frac{\sqrt{ x+4 }-3}{(x-5)} *\frac{\sqrt{ x+4 }+3}{\sqrt{ x+4 }+3} \\
=\lim_{ x \to 5 } \frac{x+4-9}{(x-5)(\sqrt{ x+4 }+3)} \\
=\lim_{ x \to 5 } \frac{x-5}{(x-5)(\sqrt{ x+4 }+3)} && \text{Cancel out our terms, then} \\
=\lim_{ x \to 5 } \frac{1}{\sqrt{ x+4 }+3} \\
= \frac{1}{6}
\end{align}
$$

Final Example: 
$$
\begin{align}
f(x) = \begin{cases}
\sqrt{ x
\end{cases}\\
\text{find }\lim_{ x \to 2 } f(x) 
\end{align}

$$

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



