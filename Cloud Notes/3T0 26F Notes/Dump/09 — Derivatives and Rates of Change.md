---
updated_at: 2026-10-01T13:08:15.575-04:00
edited_seconds: 190
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 9
Lecture Date: 2026-09-28
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