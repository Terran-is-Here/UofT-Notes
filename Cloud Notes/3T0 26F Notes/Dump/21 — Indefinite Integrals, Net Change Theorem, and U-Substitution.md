---
updated_at: 2026-10-26T18:05:24.771-04:00
edited_seconds: 1190
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
There's nothing explicitly set out within our earlier expressions in terms as to how we can solve this. We will now introduce the Substitution Rule. 

> Recall that from our definition of an Indefinite integral that: $\int f(x) \, dx = F(x) + C$
> Recall from the Net Change theorem as well that $f(x) = F'(x)$; then: $\int F'(x)\,dx = F(x) + C$

Now, take the following Integral, where $F'(x)=f(x)$
$$
\int F'(g(x))g'(x) \,dx = F(g(x)) + C
$$
Recall that from the chain rule; that:
$$
\begin{align}
\frac{d}{dx}[F(g(x))+C] = F'(g(x))g'(x) 
\end{align}
$$
Which satisfies our definition for an Indefinite Integral above, then setting $u=g(x)$, this can be written as: 
$$
F'(g(x))g'(x) = F'(u)du \implies \int F'(g(x))g'(x) \;dx = \int F'(u)\,du
$$
Since $F'(u)=f(u)$, then this can be finally expressed as: 
$$
\boxed{\int f'(g(x))g'(x)\,dx = \int f(u)\,du}
$$
Where $u=g(x),du=g'(x)$. This is The Substitution Rule. 

> [!theorem] The Substitution Rule 
> If $u=g(x)$ and is differentiable; where it's range is $I$, and if $f$ is continuous on an interval $I$, then: 
> $$\int f'(g(x))g'(x) = \int f(u)\;du$$
> Or in other words, The Substitution Rule implies to us that we can treat $dx,du,\dots$ as differentials if they take place after an integration symbol.
> > The Substitution Role is the analogous "inverse operation" to function composition, however some function composition operations may be more applicable to be simplified in a different manner. 

Often what happens is that we find for a corresponding pair / term of a function & it's corresponding $dx,du,\dots$ as some term of the differential that we are substituting with respects to. 
### Application
We can apply this in a trivial case to demonstrate it's application: 
$$
\begin{align}
 & = \int x^{3}\cos(x^{4}+2) \, dx \\ \\
 u& =x^4 + 2  \implies du = 4x^3 \,dx \to x^3 \,dx = \frac{1}{4}du \\
  & =\int \frac{1}{4}\cos(u) \, du \\
  & =\frac{1}{4}\int \cos(u) \,du = \frac{1}{4}\sin(u) + C \\
  & =\frac{1}{4}\cos(x^4+2) + C
\end{align}
$$

In a slightly more challenging case: 
$$
\begin{align}
 & =\int \sqrt{ 2x+1 }\,dx \\
 u & =2x+1 \to du = 2dx \to dx=\frac{1}{2}du \\
  & =\int \frac{1}{2}\sqrt{ u } \, du \\
  & =\frac{2}{6}u^{3/2}+C \\
  & =\frac{2}{6}(2x+1)^{3/2} +C = \frac{1}{3}(2x+1)^{3/2}+C
\end{align}
$$
The hardest part for $u$ substitution is trying to figure out what is the best term to substitute in as a term of $u$. For instance: 
$$
\begin{align}
u =(2x+1)^{1/2}=  \sqrt{ 2x+1 } \implies u^2=2x+1 \\
\frac{d}{dx}u^2 = \frac{d}{dx}2x + 1 \implies 2u\,du  = 2\,dx \implies u \,du = dx
\end{align}
$$
Then, resubstituting in: 
$$
\int \sqrt{ 2x+1 }\,dx = \int u ^2 \,du = \frac{u^3}{3}+ C = \frac{1}{3}(2x+1)^{3/2}
$$
There exist many ways to plug in, some are simpler than others. 

Take now this more challenging example: 
$$
\int \sqrt{ 1+x^2 }* x^5\,dx
$$
Note that this may not be easy to solve at first glance. Let's try setting $u=1+x^2$, then the following: 
$$
\begin{align}
u  & = 1+x^2 \\
 & \implies u-1 = x^2 \implies (u-1)^2 = x^4 \\
 & \implies du = 2x \,dx \implies x \, dx = \frac{1}{2}du 
\end{align}
$$
Noting that $x^5 = x^4x$, then rewriting our expression from earlier: 
$$
\begin{align}
 & =\int \sqrt{ 1 + x^2 } x^{5}\,dx \\
 & =\int \sqrt{ u }*(u-1)^2 * \frac{1}{2}\,du \\
 & =\frac{1}{2}\int u^{1/2} *(u-1)^{2}\,du = \frac{1}{2}\int u^{1/2}(u^{2} - 2u + 1)\,du \\
 & =\frac{1}{2}\int u^{5/2} -2u^{3/2} + u^{1/2} \, du \\
 & =\frac{1}{2}\left[ \frac{2u^{7/2}}{7} -\frac{4u^{5/2}}{5} + \frac{2u^{3/2}}{3} \right] +C\\
 & =\frac{u^{7/2}}{7} + \frac{2u^{5/2}}{5} + \frac{u^{3/2}}{3} +C\\
 & =\frac{(1+x^{2})^{7/2}}{7} + \frac{(1+x^{2})^{5/2}}{5} + \frac{(1+x^{2})^{3/2}}{3} +C
\end{align}
$$
## U-Substitution and Definite Integrals
Evaluating definite integrals through substitution steps above, then using the fundamental theorem as usual is possible. However, in some cases it may be more apt to perform substitution. 

Recall how we defined U-Substitution for Indefinite Integrals: We substituted our variable $x$ with some term $u$, where $u$ is a function of $x$. Retaking our earlier definition: 
$$
\int_{a}^{b} f'(g(x))g'(x) \, dx = \left.F(g(x))\right|^b_{a} = F(g(b))-F(g(a)) \tag{from FToC 2}
$$
Note that here, we had $g(b),g(a)$ are our evaluation terms, thus this implies that: 
$$
\int ^{g(b)}_{g(a)}f(u)\,du = F(u)|^{g(b)}_{g(a)} = F(g(b))-F(g(a))
$$
Thus, we find the corresponding substitution rule for Definite Integrals: 

> U-Sub Rule (Definite Integrals)
> If $g'(x)$ is continuous in $[a,b]$, and $f(x)$ is continuous on the range of $u=g(x)$, then: 
> $$\int_{a}^{b}f'(g(x))g'(x) \,dx = \int_{g(a)}^{g(b)}f(u)\,du$$

Note that we need to update the interval of integration when we perform this operation (or in other words, we find the range of values outputted by the composed function within, then plug those in as the range of values): 
$a,b \to g(a),g(b)$
### Symmetry in Definite Integrals
From the properties above, we can actually define two special identities pertaining to definite integrals where their bounds are symmetrical. Take the following: 
$$
\begin{align}
\int_{-a}^{a}f(x)\,dx  & = \int ^{0}_{-a}f(x)\,dx + \int ^{a}_{0}f(x)\,dx \\
 & =-\int ^{-a}_{0}f(x)\,dx + \int ^{a}_{0}f(x)\,dx
\end{align}
$$
If we substitute $u=-x$ in our first term, then $du=-dx$. Note as well that when $x=-a,u=a$, thus: 
$$
\begin{align}
 & =-\int_{0}^{-a}-f(-u)\,du + \int_{0}^{a}f(x) \, dx \\
 & =\int_{0}^{a}f(-u)\,du + \int ^{a}_{0}f(x)\,dx
\end{align}
$$
If $f$ is even, that is $f(-u)=f(u)$, then: 
$$
\begin{align}
 & =\int ^{a}_{0}f(-u)\,du + \int ^{a}_{0}f(x)\,dx =  \\
 & =\int ^{a}_{0}f(u)\,du + \int ^{a}_{0}f(x)\,dx  = 2\int_{0}^{a}f(x)\,dx\tag{note 1}
\end{align}
$$
* Note 1: Note that $f(u)\,du$ is in terms of what respects we are integrating our function with; irrespective of how we defined it earlier (i.e. this is our $x^{*}_{i}$ term and $\Delta x_{i}$ term) 
Similarly, if $f$ is odd, that is $f(-u)=-f(u)$, then: 
$$
\begin{align}
 & =\int ^{a}_{0}f(-u)\,du + \int ^{a}_{0}f(x)\,dx =  \\
 & =-\int ^{a}_{0}f(u)\,du + \int ^{a}_{0}f(x)\,dx  = 0\int_{0}^{a}f(x)\,dx\tag{note 1}=0
\end{align}
$$
![[21 — Indefinite Integrals, Net Change Theorem, and U-Substitution-1793052361062.webp|296]]
Or, in a graphical representation: 