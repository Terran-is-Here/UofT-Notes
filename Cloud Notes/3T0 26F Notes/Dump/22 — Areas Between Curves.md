---
updated_at: 2026-10-29T18:09:58.635-04:00
edited_seconds: 380
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

> Note that when the area is *enclosed* within two functions, in this context we're asking for the area within some two points of intersection of the functions involved. That is to say, the area being discussed is *entirely enclosed* between the two functions we have present. 
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
> Where $f(x),g(x)$ are in terms of $y$, and $a,b$ are in terms of $x$. 

Note that by our definition above, we need to solve for the areas in terms of the sums of the corresponding intervals; that is to say we need to find values where $f(x)=g(x)$ (or, more accurately, locations where the corresponding inequalities change), then take the integrals of those subintervals, then sum up the total resulting area. 

### Change of Variables
Occasionally, it may be more apt to redefine and resolve functions in terms of $y$ and $x$, that is we integrate with respects to $y$, and have our functions have outputs of $x$: 
$$
\int_{a}^{b}[f(y)-g(y)]\,dy
$$
Where $x=f(y),x=g(y)$, $y=a,y=b$; or in other words, we solve for $x$ within our expressions. For instance, take the two following functions: 
$$
\begin{align}
y & =x-1 \\
y^{2} & =2x+6
\end{align}
$$
Solving for $x$ we get the following expressions: 
$$
\begin{align}
x & =y+1 \\
x & =\frac{1}{2}y^{2} -3
\end{align}
$$
Solving for points of intersection, we get the following: 
$$
\begin{align}
y + 1  & = \frac{1}{2}y^{2}-3 \\
2y + 2  & =y^{2} - 6 \\
0 & =y^{2}-2y-8 = (y-4)(y+2)
\end{align}
$$
Solutions are therefore $(5,4)$ and $(-1,-2)$; then we note that the values we are integrating to with respects to $y$ are $y=-2,4$, then setting $g(y)=y+1$ and $f(y)=\frac{1}{2}y^{2}$
$$
\begin{align}
A & =\int ^{4}_{-2}[f(y)-g(y)]\,dy \\
 & =\int ^{4}_{-2}[]
\end{align}
$$
