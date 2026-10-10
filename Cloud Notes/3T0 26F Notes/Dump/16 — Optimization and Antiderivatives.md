---
updated_at: 2026-10-10T14:15:27.382-04:00
edited_seconds: 260
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 16
Lecture Date: 2026-10-16
Week: 6
---
Hub: [[ESC194 Hub]]
Previous: [[15 — Summary of Curve Sketching]]
Next: N/A 
> [!quote] Recommended Reading 
> Stewart Section 3.7, 3.9
> [[10 — Differentiation Formulas and Applied Derivatives]], [[11 — Trigonometric, Chain and Implicit Differentiation]]
--- 

# Lecture Notes

---
# Pre-Lecture Notes
## Optimization
> [!quote] Recommended Reading 
> [[14 — Derivatives, Function Shape, Horizontal Asymptotes#First Derivative Test / 1DT]]
> [[12 — Related Rates, Min and Max Values]]

Optimization problems are problems where we want to find how to *maximize* or *minimize* something; or in other words: how do we find the absolute extremum of a function? We can primarily do this by adapting our First Derivative Theorem to expand over an entire interval:

> [!theorem] First Derivative Test (for absolute extremums): 
> If $f$ has a critical point at some value $c$; then: 
> * If $f'(x) <0$ for all values $x<c$, and $f'(c)>0$ for all values $c<x$, then $f(c)$ is the absolute minima of a function. 
> * If $f'(x) >0$ for all values $x<c$, and $f'(c)<0$ for all values $c<x$, then $f(c)$ is the absolute maxima of a function. 
>
> Note that these lines are essentially describing how the shape of a slope is like.

Note that for optimization problems, if possible, we still have to evaluate our endpoints if possible; though observations from the 1DT/2DT will also help to quickly show that evaluating endpoints is *not* necessary. 

Often however; we have cases where we have *two* equations to optimize; one equation being directly optimized and another offering a restraint to the problem. The general rule of thumb is to utilize the restraint equation to limit / restrain the corresponding function to be optimized. This is essentially similar to MCV4UR; just with some more proof/rigor behind it. 

## Antiderivatives 
Antiderivatives are effectively the inverse of differentiation, and are defined as the following expression below: 
> [!theorem] Antiderivatives
> If $F$ is an antiderivative of $f$, then: 
> $$F' = f$$
> That is, the derivative of an antiderivative of some function $f$ returns back that same function $f$. 

Note that the concept of taking an antiderivative also has an added component to it, a component that partially arises from the Mean Value Theorem. Recall that in [[13 — Mean Value Theorem, Linear Approximations and Differentials#^4698a8|Mean Value Theorem (13) > Corollary 1.1]] that $f'(x)=0$