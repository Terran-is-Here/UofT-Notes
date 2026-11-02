---
updated_at: 2026-11-02T11:48:09.577-05:00
edited_seconds: 1340
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 20
Lecture Date: 2026-11-02
Week: 7
---
Hub: [[ESC194 Hub]]
Previous: [[19 — The Definite Integral]]
Next: [[21 — Indefinite Integrals, Net Change Theorem, and U-Substitution]]
> [!quote] Recommended Reading 
> Section 4.3 (Stewart) 
--- 
# Lecture Notes
## FTC (LEC) 
Recall from Definite Integrals that we can define the concept *of* a definite integral as the limit of the Reimann sum in terms of the norm (see: [[19 — The Definite Integral#^13b41d|the formal definition]]); from here, we can work towards the crucial theorem of the Fundamental Theorem of Calculus. 

To begin with; let's define a familiar function from the pre-lecture notes: 
$$
f(x) = \int_{a}^{x}f(t)\,dt
$$
Where $f(x)$ represents the area of $f(t)$ from $[a,x]$; For instance, take the example of $\int_{0}^{x}t\,dt$. 

Finding the area of this function from $[0,x]$, we realize that this represents the area of a triangle, with a base of $x$, and a height of x; thus $A=\frac{1}{2}x^{2}$; or in other words: 
$$
\int_{0}^{x}t\,dt = \frac{x^{2}}{2} =F(x)
$$
Consider that $F'(x)=x$; or in other words, this represents our integrand; or in other words, the outcome of an integral in this context is equivalent to the antiderivative of the integrand. We now seek to prove this in a general case. 

### FTC 1
> [!theorem] FTC 1 (LEC) 
> Let $f$ be continuous on $[a,b]$, the function $F$ defined on $[a,b]$ by the following expression: 
> $$F(t) = \int_{a}^{x}f(t)\,dt $$
> This expression is continuous on $[a,b]$, differentiable on $(a,b)$, and has the derivative where $F'(x)=f(x)$, $\forall x\in(a,b)$

Now, consider the following function: 
$$
F(x) = \int_{a}^{x}f(t)\,dt
$$
Consider, that for $h>0$, the following expression: 
$$
F(x+h)-F(x) = \int_{a}^{x+h}f(t)\,dt - \int_{a}^{x}f(t)\,dt
$$
Consider that this is equivalent to us taking the difference area of a function $f(x)$ between $x+h$ and $x$; where this approximates $hf(x)$, or in other words: 
$$
\frac{F(x+h)-F(x)}{h} \approx f(x)
$$
We can prove this by using the Squeeze Theorem in combination with the integral expression that we defined earlier above. 

> *Proof*

$\forall x,x+h \in(a,b)$, we have the following: 
$$
\begin{align}
F(x+h)-F(x)  & = \int_{a}^{x+h}f(t)\,dt - \int_{a}^{x}f(t)\,dt \\
 & =\int_{a}^{x}f(t)\,dt + \int_{x}^{x+h}f(t)\,dt - \int_{a}^{x}f(t)\,dt \\
 & =\int_{x}^{x+h}f(t)\,dt
\end{align}
$$
As long as $h\neq 0$; then we see that, considering $h>0$
$$
\begin{align}
\frac{F(x+h)-F(x)}{h} = \frac{1}{h}\int_{x}^{x+h}f(t)\,dt
\end{align}
$$
Considering now the EVT, that our function takes a value of $M,m$ (Maximum and Minimum in $(a,b)$). Define $f(u)=m$ and $f(V)=M$, where $u,V\in[x,x+h]$. 

From one of our integral properties, we see that: 
$$
\begin{align}
m(h)  & \leq \int_{x}^{x+h}f(t)\,dt \leq M(h) \\
f(u)h  & \leq \int_{x}^{x+h}f(t)\,dt \leq f(V)h \\
f(u) & \leq \frac{1}{h}\int_{x}^{x+h}f(t)\,dt \leq f(V)
\end{align}
$$
Note that $h\to 0, u,v \to x$, as these are defined in terms of the interval of $[x,x+h]$; then we see that: 
$$
f(x) \leq \lim_{ h \to 0 } \frac{1}{h}\int_{x}^{x+h}f(t)\,dt \leq f(x)
$$
Resubstituting back in that $\int_{x}^{x+h}f(t)\,dt = F(x+h)-F(x)$, then we see that: 
$$
f(x) \leq \lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h} = F'(x) \leq f(x)
$$
From Squeeze Theorem, then we see that $F'(x)=f(x)$; or in other words, the derivative of the integral gives the integrand; thus we arise at the more formal definition of the Fundamental Theorem of Calculus: 

> Let $f$ be continuous in $[a,b]$, if $G$ is any antiderivative of $f$ on $[a,b]$, then: 
> $$\int_{a}^{b}f(t)\,dt = G(b)-G(a)$$
> This is the second half of the FTC. Note that this does *not* indicate how we can find the corresponding antiderivatives of our function. 

### FTC 2
To prove the statement we made above, consider the following expression: 
$$
F(x) = \int_{a}^{x}f(t)\,dt
$$
Where $F$ is an antiderivative of $f()$ on $[a,b]$. Note that if $G$ is also an antiderivative of $f$, then $F'=G'=f$. Note that in this case, then we know that these can only differ from some constant: $F(x)=G(x)+C$

Recall that $F(a)=0$ from our integral properties, thus: $F(a)=G(a)+C=0$, then $C=-G(a)$, then we see that: 
$$
F(x) = G(x)-G(a)
$$
Then we can note that we can substitute this for any bounds; thus: 
$$
\int_{a}^{x}f(t)\,dt = G(x)-G(a)
$$
Where $x$ is any corresponding number. To apply this, for instance take the following: 
$$
\int_{1}^{4}x^{2}\,dx = \left[ \frac{1}{3}x^{3} \right]^{4}_{1} = \left( \frac{4^{3}}{3 } -\frac{1}{3} \right) = \frac{63}{3}=21
$$

## Examples of FTC2 
Take the following integral: 
$$
\int_{0}^{\pi/2}\cos(x)\,dx
$$
Recall that $G(x)=\sin(x)$, then we see that: 
$$
\int_{0}^{\pi/2}\cos(x)\,dx = \sin \frac{\pi}{2}-\sin 0 = 1
$$

Alternatively, now take the following integral: 
$$
\int_{0}^{\pi/4}\sec ^{2}(t)\,dt = \tan(\frac{\pi}{4})-\tan(0) = 1
$$



---
# Pre-Lecture Notes
## Fundamental Theorem of Calculus
The Fundamental Theorem of Calculus is, well, the fundamental theorem of Calculus. It lets us link together the concepts of differentiation and integration together in order. Note that the textbook goes in two parts in trying to solve and express the FToC, and we will follow the same logic here. 

For the purposes of readability; the two tenets of FToC have been placed here: 
> [!theorem] Fundamental Theorem of Calculus 
> 1. If $g(x) = \int _a^x~f(x)~dx,~g'(x)=f(x)$. Or in other words, $\frac{d}{dx}\int_{a}^xf(x)~dx = f(x)$
> 2. $\int_{a}^b f(x)~dx = F(b)-F(a)$, where $F'(x)=f(x)$. 
### FToC: Special Case
The first segment of the Fundamental Theorem of Calculus deals with functions with the following form: 
$$
g(x)=\int_{a}^{x}f(x)~dx
$$
Where $f$ is a continuous function $[a,b]$, where $x$ varies between $a,b$. Note that $g(x)$ only depends on $x$, and is equivalent to the area under the function $f(x)$ from some point $a$ to $x$ (Note that if $f(x)>0 ~\forall x$ in it's domain, we can directly consider this to be the sum of the areas under the function. 

Consider now the following expression: 
$$
g(x+h) - g(x)
$$
This is equivalently telling us the difference in area between our function from $x,x+h$. Note that if $h$ is small, this approximates the small slice of area under our function $f(x)$, with a width of $h$, that is: 
$$
\begin{align}
g(x+h)-g(x)  & \approx hf(x) \\
\frac{g(x+h)-g(x)}{h} & \approx f(x)
\end{align}
$$
Thus, if we take the limit, this intuitively shows us that: 
$$
g'(x) = \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h} =f(x)
$$
Or in other words, the derivative of an integral function of the form above gives us back the original function inside. 

We can formally prove this with the Discrete Integral laws that we learned in the previous note: 
$$
\begin{align}
g(x+h)-g(x)  & =\int _{a}^{x+h} f(x)\, dx  - \int _{a}^{x} f(x)\, dx  \\
 & =\int _{a}^{x}f(x) \, dx +\int _{x}^{x+h} f(x)\, dx   - \int _{a}^xf(x) \, dx \\
&=\int _{x}^{x+h}f(x) \, dx 
\end{align}
$$
Note that for some $h\neq0$ then we can insert the following: 
$$
\frac{g(x+h)-g(x)}{h} = \frac{1}{h}\int_{x}^{x+h}f(x)~dx
$$
Note that since $f(x)$ is continuous on an interval $[a,b]$, we know that since the values we are testing are inside that interval, it must thus also be continuous within some closed interval $[x,x+h]$, thus following EVT, $\exists c_{1},c_{2}\in[x,x+h]$ where $f(c_{1})=m$ and $f(c_{2})=M$, that is, the absolute maxima and minima of the function. 

Note then that: 
$$
\begin{align}
m(x+h-x)  & \leq g(x+h)-g(x) \leq M(x+h-x) \\
mh & \leq g(x+h)-g(x) \leq Mh \\
f(c_{1})h  & \leq \int _{x}^{x+h}f(x) \, dx \leq f(c_{2})h  \\
f(c_{1}) & \leq \frac{1}{h}\int _{x}^{x+h}f(x) \, dx  \leq f(c_{2})  \\
f(c_{1}) & \leq \frac{g(x+h)-g(x)}{h} \leq f(c_{2})
\end{align}
$$
Note that with $\lim_{ h \to 0 }$, $c_{1} \to x$, $c_{2} \to x$ as $[x,x+h]$ with $h\to0\implies [x,x+h] \to[x,x]$; then: 
$$
f(x) \leq \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h}= g'(x) \leq f(x)
$$
Thus from the Squeeze Theorem, then:

$$
g'(x) = \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h} = f(x)
$$
Thus we arrive at the formal definition for the first half of the Fundamental Theorem of Calculus: 

> [!theorem] Fundamental Theorem of Calculus (Part 1)
> If $f$ is continuous on $[a,b]$, then the function $g(x)$ defined by the following: 
> $$g(x) = \int _{a}^{x}f(t) \, dt, ~~~ a\leq x\leq b $$
> Here, $g(x)$ is continuous on $[a,b]$, and is differentiable on the corresponding open interval, where $g'(x)=f(x)$. 

### FToC: Calculation
The second segment of the Fundamental Theorem of Calculus is defined as the following: 

$$
\int _{a}^{b}f(x)~dx = F(b)-F(a)
$$
Where $F'(x)=f(x)$, that is $F$ is *any* antiderivative of $f(x)$. We will now attempt to prove the following: 

Let $g(x)$ be the following: 
$$
g(x) = \int_{a}^x f(x)~dx
$$
Recall from part $1$ that $g'(x) = f(x)$, or in other words; $g(x)$ is the antiderivative of $f(x)$; then: 
$$
F(x) = g(x) +C
$$
Note that taking the one-sided limits, we can see that $g(a),g(b)$ exist, where $g(a)=0$, as $\int_{a}^a~f(x)~dx = 0$; then we can define the difference as the following: 

$$
\begin{align}
F(b)-F(a)  & =(g(b) + C ) - (g(a)+C) \\
 & =g(b) = \int_{a}^b ~f(x)~dx
\end{align}
$$
Then; we can see that a discrete integral can be calculated by taking the difference between an antiderivative taken at two points. 

> [!theorem] Fundamental Theorem of Calculus (Part 2): 
> If $f$ is continuous on $[a,b]$, then: 
> $$\int_{a}^b~f(x)~dx = F(b)-F(a)$$
> Where $F$ is any antiderivative of $f$, that is $F'(x)=f(x)$

## Implications of FToC
### FToC 1 
Retaking the theorem: 
> [!theorem] Fundamental Theorem of Calculus (Part 1)
> If $f$ is continuous on $[a,b]$, then the function $g(x)$ defined by the following: 
> $$g(x) = \int _{a}^{x}f(t) \, dt, ~~~ a\leq x\leq b $$
> Here, $g(x)$ is continuous on $[a,b]$, and is differentiable on the corresponding open interval, where $g'(x)=f(x)$. 

Note that in our integrand, if the following is true: 
$$
g(x) = \int _{a}^{u(x)}f(t) \, dt 
$$
Then: 
$$
g'(x) = f(u(x))u'(x)
$$
That is, following from chain rule; as $f(u(x))$ is the equivalent term on the right; then $g(x) = \int f(u(x))dx \to g'(x)=f(u(x))u'(x)$; as the integrand is a function of $u(x)$, thus chain rule kicks in. 


Additionally, if such the case as this exists (exercise 62 from 4.3)
$$
g(x) = \int _{\tan(x)}^{x^2} \frac{1}{\sqrt{ 2+t^4 }} \, dx 
$$
We can break this up into: 
$$
g(x) = \int_{\tan x}^{0} \frac{1}{\sqrt{ 2+t^4 }}\, dt + \int_{0}^{x^2} \frac{1}{\sqrt{ 2 +t^4 }}\,dt
$$
Following the discrete integral properties discussed in the previous note. Note that the bound for $0$ is arbitrary, as long as it is the same value in both; though $0$ often simplifies calculations. 

For the above; then taking our FToC 1: 
$$
\begin{align}
g(x)  & = \int_{\tan x}^{0} \frac{1}{\sqrt{ 2+t^4 }}\, dt + \int_{0}^{x^2} \frac{1}{\sqrt{ 2 +t^4 }}\,dt \\
 & =-\int_{0}^{\tan x} \frac{1}{\sqrt{ 2+t^4 }}\, dt + \int_{0}^{x^2} \frac{1}{\sqrt{ 2 +t^4 }}\,dt \\[1em]
 & \text{let }\alpha(x) =\tan x, u(x)=x^2 \implies d\alpha=\sec^2x, du=2x \\  & \text{then sub in:}\\[1em]
 & =-\int_{0}^{\alpha(x)}\frac{1}{\sqrt{ 2+t^4 }}\,dt + \int ^{u(x)}_{0}\frac{1}{\sqrt{ 2+t^4 }}\, dt \\
g'(x) & =\frac{d}{d\alpha}\left[ -\int_{0}^{\alpha(x)}\frac{1}{\sqrt{ 2+t^4 }} \,dt \right] \frac{d\alpha}{dx} + \frac{d}{du}\left[ \int_{0}^{u(x)}\frac{1}{\sqrt{ 2+t^4 }}\,dt \right] \frac{du}{dx} \\
 & =-\frac{1}{\sqrt{ 2+\alpha(x)^4 }} \frac{d\alpha}{dt} + \frac{1}{\sqrt{ 2+u(x)^4 }}\ \frac{du}{dx} \\
 g'(x)& =-\frac{\sec^2x}{\sqrt{ 2 + \tan^4(x) }} + \frac{2x}{\sqrt{ 2+x^8 }}
\end{align}
$$

### FToC 2: 
Retaking the Theorem: 
> [!theorem] Fundamental Theorem of Calculus (Part 2): 
> If $f$ is continuous on $[a,b]$, then: 
> $$\int_{a}^b~f(x)~dx = F(b)-F(a)$$
> Where $F$ is any antiderivative of $f$, that is $F'(x)=f(x)$

Note that if $f(x)$ is some piecewise function, such as the following: 
$$
f(x) = \begin{cases}
g(x): a_{1}\leq x<a_{2} \\
j(x):a_{2}\leq x\leq a_{3}
\end{cases}
$$
Then: 
$$
g(x) = \int_{a}^{b} f(x) \, dx  = \int_{a_{1}}^{a_{2}}g(x)\,dx + \int_{a_{2}}^{a_{3}}j(x)\,dx
$$
That is, you take the integral under each corresponding segment of the piecewise function. That is, the sum of the areas of a piecewise function is equivalent to the sum of the corresponding sections of each function conglomerated within the overall piecewise function expression. 

Additionally, if we define $g(x)$ now as something similar to our function earlier that we used in FToC 1: 
$$
g(x) = \int_{a}^{x}f(t)\,dt
$$
Then $g(x)$ may also develop into it's corresponding piecewise function; with terms expanding from the concepts from above. 
### Application
For instance, take the following problem. Solve for this holding true $\forall x>0$, solve for $f(t)$ and $a$. S
$$
6 + \int_{a}^{x} \frac{f(t)}{t^2}\,dt = 2\sqrt{ x }
$$
Recall that from the FToC1 that $\frac{d}{dx}\int_{a}^{x}f(x)dx=f(x)$, then: 
$$
\begin{align}
\frac{d}{dx}\left[ 6 + \int_{a}^{x} \frac{f(t)}{t^2}\,dt \right]  & = \frac{d}{dx}[2\sqrt{ x }] \\
\frac{f(x)}{x^2}  & =\frac{1}{\sqrt{ x }} \\
f(x)  & =x^{3/2}
\end{align}
$$
Then, our expression from earlier becomes: 
$$
\begin{align}
6 + \int_{a}^{x} \frac{1}{\sqrt{ t}}\,dt  & = 2\sqrt{ x }  & F(x) = 2\sqrt{ x } \\
6 + F(x)-F(a) & =2\sqrt{ x } \\
6 + 2\sqrt{ x } - 2\sqrt{ a } & =2\sqrt{ x } \\
6  & =2\sqrt{ a } \\
a & =9
\end{align}
$$
Then, our expression from earlier becomes: 
$$
6 + \int_{9}^{x} \frac{1}{\sqrt{ t }}\,dt = 2\sqrt{ x }
$$
