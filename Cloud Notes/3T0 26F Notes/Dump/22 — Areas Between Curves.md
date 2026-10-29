---
updated_at: 2026-10-29T17:45:41.117-04:00
edited_seconds: 240
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 22
Lecture Date: 2026-11-05
Week: 8
---
Hub: [[ESC194 Hub]]
Previous: [[21 — Indefinite Integrals, Net Change Theorem, and U-Substitution]]
Next: N/A
> [!quote] Recommended Reading 
> Section 5.1 of the Stewart Textbook
> [[19 — The Definite Integral]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Areas Between Curves
Recall the definition that we had for a Definite Integral with respects to the $x$ axis: 
$$\int _{a}^{b}f(x) \, dx = \lim_{ ||P|| \to 0 } \sum_{i=1}^{N} f(x^{*}_{i})\Delta x_{i}$$
That is, we take the area under the curve as the Reimann sum of a function $f(x)$, with sampling points and a width defined by us. 

Consider now the case in which we want to define the area between two functions, some $f(x)$ and $g(x)$, where $f(x) \geq g(x)$ then the height of the area between $f,g$ at some sample point $x$ can be defined as the difference between them: 
$$
f(x)-g(x)
$$
Since this represents the height at that point, we can extend this back into our Reimann sum definition by noticing that $f(x)-g(x)$ represents the height of the rectangle, and $\Delta x_{i}$ represents the width, then we can recognize this as: 
$$\lim_{ N \to \infty } \sum_{i=1}^{N} [f(x^{*}_{i})-g(x^{*}_{i})]\Delta x_{i}$$
Or, considering it with respects to the norm (in the case of a non-uniform width), then: 
$$
\lim_{ ||P|| \to 0 } \sum_{i=1}^{N} [f(x^{*}_{i})-g(x^{*}_{i})]\Delta x_{i} = \int_{a}^{b}[f(x)-g(x)]\,dx 
$$
> [!theorem] Areas Between Curves (base case)
> The expression of an area between a curve of two functions $f(x),g(x)$, where $f(x)\geq g(x)$ for all $x$ within the interval $[a,b]$, can be defined as the following discrete integral: 
> $$A=\int_{a}^{b}[f(x)-g(x)]\,dx$$
> Where $y=f(x),y=g(x),x=a,x=b, x\in[a,b]$. 

### Extension
Consider now that our definition above only applies for cases where, $\forall x\in[a,b],f(x)\geq g(x)$. But what about the cases in which this is not always true? What if $g(x)\geq f(x)$ in some cases? How do we grapple with this? 

For this context, we break up our function into *intervals* where $f(x)\geq g(x)$ and $g(x)\geq f(x)$ respectively, then taking the total area to be the sum *of* these areas. Note that we do this, as if we evaluate our integrals blindly; then we get negative values for area. 

Then, we are more accurately taking the integral of the following in the more general manner: 
$$
|f(x)-g(x)| = \begin{cases}
f(x)-g(x): f(x)\geq g(x) \\
g(x)-f(x):g(x)\geq f(x)
\end{cases}
$$
Then, generalizing this, we get: 

> Areas Between Curves (General Case)
> $$A=\int_{a}^{b}|f(x)-g(x)|\,dx$$
> 