---
updated_at: 2026-10-23T11:34:09.712-04:00
edited_seconds: 290
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 21
Lecture Date: 2026-11-02
Week: 8
---
Hub: [[ESC194 Hub]]
Previous: [[20 — The Fundamental Theorem of Calculus]]
Next: N/A 
> [!quote] Recommended Reading 
> Sections 4.4, 4.5 of the Stewart Textbook
> [[17— Optimization, Antiderivatives and Sigma Notation]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Indefinite Integrals
Recall that the Fundamental Theorem of Calculus only pertains to *definite integrals*, that is, integrals where we're measuring the area within a certain, closed interval $[a,b]$; Retaking it here for reference: 

> The Fundamental Theorem of Calculus
> 1. $g(x) = \int_{a}^{b}f(x)dx,g'(x)=f(x)\implies \frac{d}{dx}\int_{a}^{b}f(x)dx=f(x)$ (Integration and Differentiation are inverse functions) 
> 2. $g(x)=\int_{a}^{b}f(x)=F(b)-F(a), F'(x)=f(x)$ (A discrete integral can be evaluated as the difference of the antiderivatives) 

Recall how we said that for a discrete integral, we can define it as the difference of the two antiderivatives calculated. From here, we can derive the definition of an indefinite integral: 

$$
\int f(x)~dx = F(x)
$$
Where this now describes a *family* of functions; that is some $F(x)+C$ (similar concepts applied from Antidifferentiation). This means that our second theorem can be expressed as: 
$$
\int _{a}^{b}f(x) \, dx  = \left[]\int f(x) \, dx\right]^{b}_{a} = F(b)-F(a)
$$
Note that this approach requires that we know how to take the antiderivatives of some common functions. Recall the antiderivatives that we know so far: 
> [!theorem]- Power Rule 
> From $f(x) = x^n, f'(x)=nx^{n-1}$ Then the antiderivative of $f(x)=x^n$ is:$$f(x) = x^n, \int f(x) dx = \frac{x^{n+1}}{n+1} + C$$
> Note this is only true if and only if $n\neq -1$. 
> > In this case, $f(x)=x^{-1}, F(x) = \ln|x| +C$. 

> [!theorem]- Differentiation Rules 
> The Sum Rule natively applies with antidifferentiation, as well as the constant rule. 
> > Constant Rule:
> > $$f(x)=c, F(x) = cx + C$$

> [!theorem]- Trigonometric Rules
> Essentially reverse the direction of your differentiation of the trig functions. 
> $$\begin{array}{cc|c}\text{ Function} && \text{Corresponding Antiderivative} \\\cos(x) &  & \sin(x) \\\sin(x) &  & -\cos(x) \\\sec^2(x) &  & \tan(x) \\\sec(x)\tan(x) &  & \sec(x)\end{array}$$

From this, we get the following series of equations: 
$$
\begin{align}
\int cf(x) \, dx  & = c\int f(x) \,dx & \int [f(x) + g(x)] \,dx  & =\int f(x) \,dx + \int g(x) \, dx  \\
\int k \, dx   & =kx + C & \int x^n \, dx   & =\frac{x^{n+1}}{n+1} + c \\

\end{align}
$$