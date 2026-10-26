---
updated_at: 2026-10-26T16:54:42.971-04:00
edited_seconds: 430
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 21
Lecture Date: 2026-11-02
Week: 8
---
Hub: [[ESC194 Hub]]
Previous: [[20 — The Fundamental Theorem of Calculus]]
Next: [[22 — Areas Between Curves]]
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
\int \sin(x) \, dx  & =-\cos(x) +C & \int \cos(x) \,dx & =\sin(x)+C \\
\int \sec^2(x) \, dx  & =\tan x + C & 
\end{align}
$$
Note that this works for (arguably) trivial polynomials / expressions where no kinds of substitution are required. Some algebra may be required to manipulate a function to a form in which we can utilize these integration / antiderivatives within our expression. 
## Net Change Theorem
Recall the second Theorem in the Fundamental Theorem of Calculus: 
$$
g(x) = \int _{a}^{b}f(x) \, dx = F(b)-F(a)
$$
Where $F(x)$ is any antiderivative of $f(x)$, that is $F'(x)=f(x)$. Note that we can actually *backsubstitute this* back into our original expression, giving us the resulting Net Change theorem: 
$$
g(x) = \int_{a}^{b}F'(x) \,dx = F(b)-F(a)
$$
Or, in words: 
> The area under the rate of change, is equal to the net change. 
> That is, the integral of a rate of change is equal to the net change. 

This has numerous applications, such as pertaining to real world scenarios: 
$$
g(x) = \int _{t_{1}}^{t_{2}}dV\,dt = V(t_{2})-V(t_{1}) = \Delta V_{t} \text{ (change in volume)}
$$
$$
g(x) = \int_{t_{1}}^{t_{2}}dS\,dx = S(t_{2})-S(t_{1}) = \Delta S \text{ (change in position)}
$$
This is similar to how we define work-energy relations in physics, though not exactly. Integrating the rate of change of something to get the net change is a very powerful concept overall. 
## U-Substitution / The Substitution Rule
Recall that our Indefinite Integral formulas above solely solve for how we can find the antiderivatives of some trivial functions. Consider the case in which we have a function composing another function such as: 
$$
\int 2x\sqrt{ 2+x^2 } \, dx 
$$
There's nothing explicitly set out within our earlier expressions in terms as to how we can solve this. 