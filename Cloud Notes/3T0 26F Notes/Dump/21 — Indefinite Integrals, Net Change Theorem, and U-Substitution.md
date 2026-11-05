---
updated_at: 2026-11-05T14:51:17.474-05:00
edited_seconds: 1990
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
> [!caution] Note
> This was written partially on the same date as the previous lecture, though the timestamps have been kept to where they were (as this is a multi-day thing). Notes pertaining to the date will be written down in a separate section. 

## Indefinite Integrals (LEC) 
> Written: 11-02

Recall that we defined the definite integral in the previous note as the difference of the corresponding antiderivatives: 
$$
\int_{a}^{b}f(x)\,dx = [F(x)]^{b}_{a}
$$
Note that sometimes we don't know the bounds yet; or we want to find a general solution that we can use for *any* bounds of integration. This is where the concept of an Indefinite integral arises. Recall that: 
$$
G(x) = F(x) + C
$$
Where $C$ is any arbitrary formula. Note that this maintains the earlier definition that we had in our formula earlier: 
$$
[G(x)]^{b}_{a} = G(b)+C - G(a)-C = G(b)-G(a) = [G(x)]^{b}_{a}
$$
Or that is: 
$$
[G(x)]^{b}_{a} = [G(x) + C]^{b}_{a}
$$
If we don't know our integration bounds, then we state that :
$$
\boxed{\int f(x)\,dx = F(x)+C}
$$
This is what we note as the concept of an indefinite integral. > 
For instance: 
> $$\int x\,dx = \frac{1}{2}x^{2} + C$$
> Where $C$ is any arbitrary number; then this represents *not just one function*, but rather a *family of functions*, with the functions being vertically translated from each other. 

Note that to find the corresponding antiderivatives, we simply reverse the derivative identity table that we have introduced in multiple notes a few days back. For instance: 
$$
\begin{align}
 & = \int 2 + \tan ^{2}\theta \,d\theta \\
 & = \int 1 + 1+ \tan ^{2}\theta \,d\theta = \int 1 + \sec ^{2}\theta \,d\theta \\
 & =\theta + \tan\theta + C
\end{align}
$$
### Example
Take the following expression. Given $f'(x)=3x^{2} + 2x$, and $f(0)=5$, solve for $f(x)$.
We know from the earlier expression that $f(x)$ by integrating that derivative, thus: 
$$
f(x) = x^{3} + x^{2} + C
$$
To solve for $c$, we simply evaluate at $f(0)$, thus we see that $C=5$, thus $f(x) = x^{3} + x^{2} + 5$. 

> Continued: 11-05
## Net Change (LEC) 
Consider the following expression: 
$$
\int_{a}^{b}f(x)\,dx = \int_{a}^{b}F'(x) \,dx
$$
We can express this as: 
$$
=\int_{a}^{b} \frac{df}{dx}dx \to \sum df
$$
(Note we don't fully cancel out the differentials, but this represents us with a central idea: The integral is equivalent to the net change of the function over such an interval). For instance: 

$$
v(t) = t^{2} -2t - 3
$$
Consider an object as a function of time, and this represents velocity; then we note $v(t) = s'(t)$, or that is $v(t) = \frac{ds}{dt}$, then: 
$$
\int_{2}^{4}v(t)\,dt = \Delta s
$$
Substituing in, then: 
$$
\int_{2}^{4}[t^{2}-2t-3]\,dt = \left[ \frac{t^{3}}{3}-t^{2}-3t \right]^{4}_{2} = \frac{2}{3} =\Delta s
$$

Consider now the following function. Consider a charged particle undergoing acceleration in a field: 
$$
a(t) = 3-t
$$
Note that $a=v'(t)=s''(t)$, then. $s(0)=0$, and $s(3)=-1$. Integrating $a(t_{0})$ twice gives us x(t), which is: 
$$
x(t) = -\frac{t^{3}}{6} + \frac{3}{2}t^{2} + C_{1}t + C_{2}
$$
Note that with $s(0)=0 \implies C_{2}=0$, and $s(3) \implies C_{1}=-4$, thus the expression is: 
$$
x(t) = -\frac{1}{6}t^{3} + \frac{3}{2}t^{2} -4t 
$$
Consider now, how far has our particle travelled in total? Consider now the pure distance; then: 
$$
\Delta x = \int_{0}^{6}|v(t)|\,dt
$$
As $v(t) = -\frac{1}{2}t^{2}+3t - 4=\frac{dx}{dt}$ then: 
$$
\begin{align}
=\int_{0}^{6}|-\frac{1}{2}(t-2)(t-4)|\,dx
\end{align}
$$
(Function was simply factored). Due to the absolute function present inside, we have to take this in terms of the intervals $t=2,t=4$, as well as the corresponding intervals to find the resultant signs we integrate with respects to: 
* $t=2,v=0 \implies x=-\frac{4}{3}$
* $t=4, v=0 \implies x=-\frac{2}{3}$
* $t\in(0,2), v<0$
* $t\in(2,4), v>0$
* $t\in(4,6), v<0$
Thus, breaking up the interval into three based on our intervals, then: 
$$
\Delta x = [-x(t)]^{2}_{0} + [x(t)]^{4}_{2} + [-x(t)]^{6}_{4} = \frac{22}{3}
$$

## Substitution Rule (LEC) 
The Substitution Rule is equivalent to reversing the means that we do the chain rule, that is, recall that: 
$$
\frac{d}{dx}f(g(x)) = f'(g(x))g'(x)
$$
Then, in reverse: 
$$
\int f'(g(x))g'(x) \,dx = f(g(x))
$$
We let $g(x)=u$, then $du = g'(x)dx$, then: 
$$
\int f(u)\,du = F(u)+C \to F(g(x))+C
$$
As taking the chain rule of $F(u) \to F'(u)du = F'(g(x))g'(x)$, as expected. 
### Examples 
$$
\int(x^{3} +2)^{2}x^{2}\,dx
$$
Note that $x^{3}+2 =u$, then we see that $du = 3x^{2}dx$, then $\frac{du}{3}=x^{2}dx$, then: 
$$
\begin{align}
\int u^{2} \frac{1}{3}du = \frac{1}{3}\int u^{2}\,du = \frac{1}{3}\left[ \frac{1}{3}u^{3} \right]+C = \frac{(x^{3}+2)^{3}}{9} + C
\end{align}
$$

Or: take the following: 
$$
\int \cos ^{3}x\sin x\,dx
$$
Note that $u=\cos x,du=-\sin x\,dx$, then: 
$$
\int-u^{3}\,du = -\frac{u^{4}}{4}+C = - \frac{\cos^4(x)}{4} + C
$$

take the following: 
$$
\int \frac{x}{\sqrt{ x^{2}+4 }} \,dx
$$
Note that $u=x^{2}+4 \to du=2xdx$, then: 
$$
\int \frac{1}{2}u^{-1/2}\,du = \frac{1}{2}\int u^{-1/2} = u^{1/2}+C = \sqrt{ x^{2}+4 }+C
$$

Take the following: 
$$
\int x \csc x^{2}\cot x^{2}
$$
Letting $u=x^{2}\to du \to 2xdx$, then: 
$$
\frac{1}{2}\int \csc u\cot u \,du = -\frac{1}{2}\csc u + C = -\frac{1}{2}\csc x^{2}+C
$$
> [!ila] Idea
> Note that U-Sub often requires some form of pattern recognition; that is noting when a case where you *can* use u-sub exists. 

### Definite Integrals 
Consider the following expression: 
$$
\int_{0}^{1}x\sqrt{ x^{2}+1 }\,dx
$$
Consider taking U-sub, we see that $u=x^{2}+1 \to du =2xdx$, then: 
$$
\int \frac{1}{2}u^{1/2} = \frac{1}{2}\int u^{1/2}\,du = \frac{1}{3}u^{3/2} + C = \frac{(x^{2}+1)^{3/2}}{3}+C
$$
Then from here, we simply evaluate this from $0,1$. Note that with the change in variable, we can consider it with a change in the bounds in terms of that variable: 
$$
\int_{a}^{b}f(g(x))g'(x) = \int_{g(a)}^{g(b)}f(u)\,du
$$
This is known as the *change of variables* formula. This can be proved trivially: 
Let $F'(x)=f(x)$, then note the following: 
$$
\int_{a}^{b}f(g(x))g'(x) \,dx = \int_{a}^{b}F'(g(x))g'(x)\,dx = [F(g(x))]^{b}_{a} \tag{from u-sub}
$$
Then: 
$$
= F(g(b))-F(g(a)) = [F(u)]^{g(b)}_{g(a)} = \int_{g(a)}^{g(b)}f(u)\,du
$$
### Examples
Consider the following: 
$$
\int_{0}^{1}x\sqrt{ x^{2}+1 }\,dx
$$
Note that $u=x^{2 }+1$, then $u(0)=1,u(1)=2$, then: 
$$
\frac{1}{2}\int_{0}^{2}u^{-1/2}\,du = \frac{2\sqrt{ 2 }}{3} - \frac{1}{3}
$$
Note that **it is very important that you change the corresponding bounds**. 
$$
\int x^{2}(2x+1)^{4}\,dx
$$
Note the substitution of $u=2x+1$, then $du=2dx$ then $x=\frac{1}{2}(u-1)$, thus: 
$$
\frac{1}{4}\int(u-1)^{2}u^{4} \frac{1}{2}du = \frac{1}{8}\int(u-1)^{2}u^{4} \,du = \frac{1}{8}\int(u^{6}-2u^{5}+u^{4})\,du
$$
then: 
$$
=\frac{1}{8}\left[ \frac{u^{7}}{7} - \frac{2u^{6}}{6} + \frac{u^{5}}{5} \right] + C\\
=\frac{1}{8}\left[ \frac{(2x+1)^{7}}{7} - \frac{(2x+1)^{6}}{3} + \frac{(2x+1)^{5}}{5} \right] +C
$$

Consider now the following expression: 
$$
\int_{1}^{3}2x\sqrt{ x-1 }\,dx
$$
Let $u(x) = x-1$, then $x=u+1$, then $du=dx$, then: 
$$
\int_{0}^{2}2(u+1)u^{1/2}\,du
$$
Then: 
$$
=2\int_{0}^{2}u^{3/2}+u^{1/2}\,du\dots
$$
You can solve this integral from here. 

## Symmetry
Definite integrals have the following properties relating to symmetry: 
* If $f$ is odd on a symmetric interval, then $\int_{-a}^{a}f(x)\,dx = 0$
* If $f$ is even on a symmetric interval, then $\int_{-a}^{a}f(x)\,dx = 2\int_{0}^{a}f(x)\,dx$ 
### Examples
For instance, take the following: 
$$
\int_{-\pi}^{\pi}\sin(x)\,dx = 0
$$
(As $\sin(x)$ is odd)
Additionally: 
$$
\int_{\frac{\pi}{2}}^{\pi/2}\cos(x)\,dx = \int_{0}^{\pi/2}\cos(x)\,dx = 2
$$
As $\cos(x)$ is even. 

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
Where $F(x)$ is any antiderivative of $f(x)$, that is $F'(x)=f(x)$. Note that we can actually *back substitute this* back into our original expression, giving us the resulting Net Change theorem: 
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
  & =\frac{1}{4}\sin(x^4+2) + C
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
Note that this may not be easy to solve at first glance. Let's try setting $u=1+x^2$, then the following become the result
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
 & =\frac{(1+x^{2})^{7/2}}{7} + \frac{2(1+x^{2})^{5/2}}{5} + \frac{(1+x^{2})^{3/2}}{3} +C
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

> [!theorem] Substitution Rule (Definite Integrals)
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
* Note 1: Similar logic to the above applies. 
![[21 — Indefinite Integrals, Net Change Theorem, and U-Substitution-1793052361062.webp|296]]
Or, in a graphical representation: 