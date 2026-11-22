---
updated_at: 2026-11-22T12:22:51.643-05:00
edited_seconds: 340
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 33
Lecture Date: 2026-11-30
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[32 — Exponential Growth, Decay and Population Growth]]
Next: [[34 — Complex Numbers]]
> [!quote] Recommended Reading 
> Stewart Section 9.5 and [[31 —Differentials and Separable Equations]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Linear Equations
Recall that in our notes about [[31 —Differentials and Separable Equations|Separable Equations]], we noted that we are currently only able to solve a differential equation of the following form: 
$$
\frac{dy}{dx} = \frac{f(x)}{g(y)}
$$
However, following this section, we should be able to solve the field of *first order linear differential equations*: 
$$
\frac{dy}{dx} + P(x)y = Q(x)\tag{1}
$$
Where $P,Q$ are continuous functions on some interval $I$. For instance: 
$$
y' + \frac{1}{x}y = 2
$$
This is an example of a First Order Linear Differential Equation. Note that if we multiply both sides by $x$, we can note that from chain rule: 
$$
xy' + y = 2x \implies (xy)' = 2x
$$
Then integrating, we find that: 
$$
\begin{align}
\int(xy)' \,dx  & = \int2x\,dx \\
xy & = x^{2}+C \\
y & = x + \frac{C}{x} \\
\implies y' & =1 -\frac{C}{x^{2}}
\end{align}
$$
Noting that this is a valid solution to our expression: 
$$
\begin{align}
1 - \frac{C}{x^{2}} + \frac{1}{x}\left( x+\frac{C}{x} \right)  = 1 - \frac{C}{x^{2}} + 1 + \frac{C}{x^{2}} = 2 
\end{align}
$$
as desired. 
### Generalizing
Note that how in our previous example, we multiplied both sides by some function $I(x)$ which allows us to integrate it, a function that we note as an "integration factor". Recalling $(1)$ from earlier: 
$$
\frac{dy}{dx} + P(x)y = Q(x)\tag{1}
$$
We want to multiply some function $I(x)$ such that the left side of our equation above, becomes the derivative of the product $I(x)y$, that is: 
$$
I(x)\left( \frac{dy}{dx} + P(x)y \right) =(I(x)y)' \tag{2}
$$
If such a function exists, then: 
$$
(I(x)y)' = I(x)Q(x) 
$$
Considering this, taking expression $(2)$(and substituting $\frac{dy}{dx}=y'$ notation-wise), we find that: 

$$

$$