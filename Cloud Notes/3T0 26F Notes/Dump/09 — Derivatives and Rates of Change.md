---
updated_at: 2026-10-01T13:56:46.207-04:00
edited_seconds: 810
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 10
Lecture Date: 2026-10-01
Week: 4
Created: September 26th 2026, 4:17:02 pm
---
Hub: [[ESC194 Hub]]
Previous: [[08 — Continuity]], [[08-1 — Intermediate Value Theorem]]
Next: [[10 — Differentiation Formulas and Applied Derivatives]]
> [!quote] Recommended Reading 
> Stewart 2.1, 2.2
> Since this section also pertains to limits, [[06 — Precise Limit Definition#Precise Limit Definition|the Precise Limit Definition (ESC194-L6)]] could also help. 
--- 
# Lecture Notes
## Derivatives
Recall, that we defined the concept of a derivative of a function as the *slope* of a tangent line. Or in other words, the instantaneous slope of our function at some point. We can concretely define this as the following: 

> Tangent Lines
> The tangent line to a curve $y=f(x)$ at some point $P(a,f(a))$ is the line through point $p_{1}$ with slope: $$m=\lim_{ x \to a } \frac{f(x)-f(a)}{x-a} \text{ Provided that the limit exists.}$$Alternatively, let $h=x-a$, then $$m=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h} $$Note that $a$ can be any value; then: $$m=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} $$

From this, we get the formal definition of a derivative. 

> [!theorem] Limit Definition of a Derivative
> The derivative of a function $f(x)$ at $x=a$ is denoted by the notation of $f'(a)$ is defined as: $$f'(a) = \lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h} \underbrace{\implies}_{a=x} f'(x) = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}$$
> This is alternatively notated as $\frac{dy}{dx}$, where $y=f(x)$, $\frac{dy}{dx}=f'(x)$
> $$\frac{dy}{dx} = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}$$

Higher order derivatives can be expressed as the following: 
$$
(f'(x))' = f''(x) = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{d^2y}{dx^2}
$$


### Computing from Definition
Given the following function: $f(x) = x^2 + 3x + 2$. Take the derivative of this function using the limit definition of a derivative. This can be expressed as: 
$$
\begin{align}
f'(x) &= \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} \\
&= \lim_{ h \to 0 } \frac{(x+h)^2 + 3(x+h) +2)-(x^2 + 3x + 2)}{h} \\
&=\lim_{ h \to 0 } \frac{x^2 + 2xh+h^2 + 3x+3h +2-x^2 - 3x - 2)}{h} \\
&=\lim_{ h \to 0 } \frac{2xh+h^2 +3h }{h} \\
&=\lim_{ h \to 0 } \frac{h(2x + h + 3)}{h} \\
&= \lim_{ h \to 0 } 2x+h+3 =2x + (0) + 3 \\
&=2x+3 
\end{align}
$$

Given the following function: $f(x) = \sqrt{ x }$ using the definition: 
$$
\begin{align}
f'(x) &= \lim_{ h \to 0 } \frac{\sqrt{ x+h }-\sqrt{ x }}{h} \\
&=\lim_{ h \to 0 } \frac{\sqrt{ x+h }-\sqrt{ x }}{h} *\frac{\sqrt{ x+h }+\sqrt{ x }}{\sqrt{ x+h }+\sqrt{ x }} \\
&=\lim_{ h \to 0 } \frac{x+h-x}{h(\sqrt{ x+h }+\sqrt{ x })} \\
&=\lim_{ h \to 0 } \frac{h}{h(\sqrt{ x+h }+\sqrt{ x })} \\
f'(x)&=\lim_{ h \to 0 } \frac{1}{(\sqrt{ x+h }+\sqrt{ x })} = \frac{1}{2\sqrt{ x }} \\
\end{align}
$$
Note that $f(x), x\in[0,\infty)$, but $f'(x), x\in(0,\infty)$ due to the denominator. The domain of a function and it's derivative may not be equal. 
### Function Differentiability 
A function $f(x)$ is differentiable at a point $a$ if $f'(a)$ exists. 

A function $f(x)$ is differentiable on an interval $(a,b)$ for any $a,b$ if it is differentiable on every point in $(a,b)$. 

> Example: Take the function $f(x) = |x|$. At what points is this differentiable. Note that absolute function is a piecewise function of $f(x)=|x|=\begin{cases}-x:x\leq 0\\x:x>0\end{cases}$. 
> Consider this in terms of cases, $x<0 \implies f(x) = -x$ therefore: 

$$f'(x) = \lim_{ h \to 0 } \frac{-(x+h) +x}{h} = \lim_{ h \to 0 } -\frac{h}{h} = -1$$
Consider this if $x >0 \implies f(x) = x$, therefore: 
$$f'(x) = \lim_{ h \to 0 } \frac{(x+h) -x}{h} = \lim_{ h \to 0 } \frac{h}{h} = 1$$
Consider however, what if $x=0 \implies f(x) =x$, then: 
$$
\begin{align}
f'(0) = \lim_{ h \to 0 } \frac{|0+h| - |0|}{h} &= \lim_{ h \to 0 } \frac{|h|}{h} & \text{Approach from both sides} \\
=\lim_{ h \to ^-0 } \frac{|h|}{h} =\lim_{ h \to ^-0 } -\frac{h}{h} &= -1 &  =\lim_{ h \to ^+0 } \frac{|h|}{h} =\lim_{ h \to ^+0 } +\frac{h}{h} &= -1 \\
\text{Since LHL} \neq \text{RHL} && \implies \lim_{ h \to 0 } =\frac{|h|}{h} =\text{DNE} \\
\therefore, f'(0) =\text{DNE.}
\end{align}
$$

### Continuity and Differentiability
> *Theorem.*
> If $f(x)$ is differentiable at $x=a$, then $f(x)$ is continuous at that point $a$. 
> This is non-bidirectional. Continuity does not imply differentiability, but differentiability implies continuity, that is: 
> $$\exists f'(x=a) \implies f(x) \text{ is continuous at } x=a$$Recall, continuous at $x=a$ means that $\lim_{ x \to a }f(x)=f(a)$. The proof is left as an exercise to the reader. 

#### Non-Differentiable Locations
> Cusps: 
> Locations that are continuous, or in other words, locations where our derivative from either side explode to $\pm \infty$. 

> Vertical Line Locations
> Locations where the derivative approaches infinity; or in other words the tangent line becomes vertical. 

----
# Pre-Lecture Notes
## Rate of Change
The concept of a rate of change is often defined by the slope equation below, which can be related into it's corresponding form as a function of $x$: 
$$
\begin{align}
m = \frac{\Delta y}{\Delta x} \to \frac{f(x_{1}) - f(x_{2})}{x_{1}-x_{2}} && \text{set this to } x_{1} = x_{2} + h \\
=\frac{f(x_{2} +h) - f(x_{2})}{h}
\end{align}
$$
This is essentially calculating the slope of the secant line between points $x_{1},x_{2}$, where these points have a distance $h$ between them. 
## Instantaneous Rate of Change
The concept of an instantaneous rate of change is defined by the equation below, where we take the limit of our functions as $h\to 0$. 
$$
m=f'(x)=\lim_{ h \to 0 } \frac{f(x+h) - f(x)}{h}
$$
This is notated as the limit-based definition of the limit. Note that the notation on the left ($f'(x)$) is the notation of the derivative, and this solves for the *slope* of our tangent line at $x$. 