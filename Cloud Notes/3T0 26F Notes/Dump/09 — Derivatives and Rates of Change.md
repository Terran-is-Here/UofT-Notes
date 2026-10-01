---
updated_at: 2026-10-01T13:33:33.074-04:00
edited_seconds: 380
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

> The derivative of a function $f(x)$ at $x=a$ is denoted by the notation of $f'(a)$ is defined as: $$f'(a) = \lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h} \underbrace{\implies}_{a=x} f'(x) = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}$$

### Computing from Definition
Given the following function: $f(x) = x^2 + 3x + 2$. Take the derivative of this function using the limit definition of a derivative. This can be expressed as: 
$$
\begin{align}
f'(x) &= \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} \\
&= \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
\end{align}

$$

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