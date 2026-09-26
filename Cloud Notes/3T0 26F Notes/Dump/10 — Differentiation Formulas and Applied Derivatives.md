---
updated_at: 2026-09-26T17:28:46.905-04:00
edited_seconds: 240
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Lecture Date: 2026-10-01
Week: 4
Created: September 26th 2026, 5:14:39 pm
---
Hub: [[ESC194 Hub]]
Previous: [[09 — Derivatives and Rates of Change]]
Next: N/A 
> [!quote] Recommended Reading 
> Sections 2.3, 2.7 of the Stewart Textbook. 
> Also, [[07 — Limit Laws]] will also be a useful reference for some of the things that we do. 
--- 
# Lecture Notes
# Pre-Lecture Notes
## Differentiation Formulas 
Retaking the limit-based definition of the limit: 
$$
f'(x) = \frac{df(x)}{dx}= \lim_{ h \to 0 }  \frac{f(x+h) - f(x)}{h}
$$
As we saw from the previous section, taking the derivative solely from this limit definition *is* possible, however it takes a significant amount of effort and time to do. We can create some quick definitions to solve for the derivatives of some simple functions without having to invoke this definition directly. 

> Constant Rules
> 1. Let $f(x) = c$, then $f'(x) = 0$
> *Proof:* $$\begin{align}f'(x) &= \lim_{ h \to 0 }  \frac{f(x+h) - f(x)}{h} \\&=\lim_{ h \to 0 } \frac{c-c}{h} \\&=\lim_{ h \to 0 } \frac{0}{h} = 0 \\&\therefore, f(x) = c \implies f'(x) = 0\end{align}$$
> 2. Let $g(x) = cf(x)$, $g'(x) = cf'(x)$. 
> *Proof:*$$\begin{align}g'(x) &= \lim_{ h \to 0 } \frac{g(x+h) - g(x)}{h} \\&= \lim_{ h \to 0 } \frac{cf(x+h) - cf(x)}{h} \\&= c\left[\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} \right] \\&=cf'(x)\end{align}$$

> General Power Rule 
> Let $f(x) = x^n$, then $f'(x) = nx^{n-1}$. 
> *Proof:* Left as an exercise to the reader (Aries here, I am NOT writing out this proof in the back of a moving vehicle.) 

