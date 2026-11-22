---
updated_at: 2026-11-22T12:50:22.482-05:00
edited_seconds: 680
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 33
Lecture Date: 2026-11-30
Week:
Created: November 22nd 2026, 11:55:55 am
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

This is an example of a First Order Linear Differential Equation. Note that if we multiply both sides by $x$, we can note that from product rule: 

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
## Generalizing
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
\begin{align}
I(x)(y' + P(x)y) & = (I(x)y)' \\
I(x)y' + I(x)P(x)y & = I(x)y' + I'(x)y \\
I(x)P(x)y & =I'(x)y \\
I(x)P(x) & = \frac{dI}{dx} \\
\end{align}
$$

Noting that this is a separable differential equation, then: 

$$
\begin{align}
P(x)\,dx & = \frac{1}{I(x)}\,dI \\
\int P(x)\,dx & = \int \frac{1}{I(x)}\,dI \\
\int P(x)\,dx & = \ln \left| I(x)\right|+C \\
e^{\int P(x)\,dx} & = I(x) e^{C} & A=\pm e^{C} \\
I (x) & =Ae^{\int P(x)\,dx}  & A=1 \text{ to simplify} \\
I(x) & =e^{\int P(x)\,dx}

\end{align}
$$

Thus, with our expression in this form, we note now that to simply solve a linear differential equation of the first order, we simply multiply by this function on both sides then integrate. 
> [!theorem] Solving First Order Linear Differential Equations 
> Given a linear differential of the first order: 
>
> $$y' + P(x)y = Q(x)$$
>
> This can be solved by multiplying both sides by the integration factor of $I(x) = e^{\int P(x)\,dx}$, then integrating the expression from there.
>
> $$e^{\int P(x)\,dx}(y' + P(x)y)=  e^{\int P(x)\,dx}Q(x)$$
>
> As: 
>
> $$\begin{align}e^{\int P(x)\,dx}y' + e^{\int P(x)\,dx}P(x)y  & = e^{\int P(x)\,dx}Q(x) \\\frac{d}{dx}\left( e^{\int P(x) \, dx}y \right)  & = e^{\int P(x)\,dx}Q(x)\end{align}$$
>
> And then from here, you can solve for $y$ by solving for the integral as per usual. 

### Example(s)
Consider the following differential: 
$$
\frac{dy}{dx} + 3x^{2}y = 6x^{2}
$$
Noting that $P(x)=3x^{2}$, then we can find our integration factor: 
$$
\begin{align}
I(x) & =e^{\int 3x^{2}\,dx}= e^{x^{3}}
\end{align}
$$
> (Note that we don't have a $e^{C}$ term present **for the integration factor**, as from our earlier algebra, this expression is actually $I(x)=\frac{e^{\int P(x)\,dx}}{e^{C}}$, taking the corresponding antiderivative and adding the $+C$ term at the end cancels out.) 

Plugging this into our expression, then: 
$$
\begin{align}
e^{x^{3}}\left( y'+3x^{2}y \right)  & = e^{x^{3}}6x^{2} \\
e^{x^{3}}y' + e^{x^{3}}3x^{2}y & = e^{x^{3}}6x^{2} \\
\frac{d}{dx}(e^{x^{3}}y)  & =e^{x^{3}}6x^{2} \\
\int \frac{d}{dx}( e^{x^{3}}y)\,dx & =\int e^{x^{3}}6x^{2}\,dx \\
e^{x^{3}}y & =2e^{x^{3}} + C \\
y  & = 2 + \frac{C}{e^{x^{3}}}
\end{align}
$$

Consider now the following IVP: 
$$
x^{2}y' + xy = 1, x>0, y(1)=2
$$
Noting that we want to get to some $y' +P(x)y = Q(x)$, we divide by $x^{2}$ on both sides: 
$$
\begin{align}
\frac{1}{x^{2}}(x^{2}y' + xy) & = \frac{1}{x^{2}} \\
y' + \frac{1}{x}y & = \frac{1}{x^{2}}
\end{align}
$$
Finding our integration factor: 
$$
I(x) = e^{\int 1/x\,dx} = e^{\ln(x)} = x
$$
Multiplying on both sides, then: 
$$
\begin{align}
xy' + y  & = \frac{1}{x} \\
(xy)'  & = \frac{1}{x} \\
\int(xy)'\,dx & = \int \frac{1}{x}\,dx \\
xy & = \ln|x|+C \\
y  & = \frac{\ln|x|+C}{x}
\end{align}
$$
Noting that from our initial value, that $y(1)=2$, thus: 
$$
\begin{align}
y(1)=2=\frac{\ln|1|+C}{1} \implies C=2
\end{align}

$$
Thus our solution becomes: 
$$
y = \frac{\ln|x|+2}{x}
$$
