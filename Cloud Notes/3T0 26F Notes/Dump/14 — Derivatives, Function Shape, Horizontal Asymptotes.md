---
updated_at: 2026-10-07T23:16:31.055-04:00
edited_seconds: 520
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 14
Lecture Date: 2026-10-09
Week: 5
Created: October 5th 2026, 1:58:37 pm
---
Hub: [[ESC194 Hub]]
Previous: [[13 — Mean Value Theorem, Linear Approximations and Differentials]]
Next: N/A
> [!quote] Recommended Reading 
> Chapter 3.3, 3.4 of the Stewart Textbook. 

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Intervals of Increase and Decrease 
> [!quote] Recommended Reading 
> [[12 — Related Rates, Min and Max Values#Fermat's Theorem]]

Recall the definition that we had for Fermat's Theorem being one of the tests that we have for solving critical points: 
> [!theorem] Fermat's Theorem
> If a function $f$ has a local maximum *or* minimum at $c$, if $f'(c)$ exists, then $f'(c)=0$.

From here, we can define the concepts of Intervals of Increase and Intervals of Decrease: 
> [!theorem] Intervals of Increase and Decrease
> An interval $(a,b)$ is an: 
> * Interval of Increase if $f'(x) >0$
> * Interval of Decrease if $f'(x) <0$

Proofs of this are attached below: 
> Proof of IoI, IoD: 
> Let $x_{1},x_{2}$ be any two numbers in an interval with $x_{1}<x_{2}$. From how we defined an *increasing* function, then we need to prove that $f(x_{1})<f(x_{2})$. Given if $f'(x) >0$, then from [[13 — Mean Value Theorem, Linear Approximations and Differentials#^646c42|Mean Value Theorem]]: $$\begin{align}f'(c) &= \frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}} &  x_{1}<x_{2} \to 0 < x_{2}-x_{1}  \\(x_{2}-x_{1})f'(c) &= f(x_{2})-f(x_{1}) & (x_{2}-x_{1}) > 0 \land f'(c) >0 & \implies f(x_2)-f(x_{1}) > 0 \\f(x_{2})>f(x_{1}) \implies f(x_{1}) & \leq f(x_{2})\end{align}$$
> Similarly, now let $f'(x) <0$, then we need to show that our function must be decreasing, that is for $x_{1}<x_{2}$, $f(x_{2})<f(x_{1})$. $$\begin{align}f'(c) &= \frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}& x_{1}<x_{2} \implies 0 < x_{2}-x_{1} \\(x_{2}-x_{1})f'(c)&=f(x_{2})-f(x_{1}) & (x_{2}-x_{1})>0 \land f'(c) <0 \implies f(x_{2})-f(x_{1})<0 \\f(x_{2})-f(x_{1})<0 &\implies f(x_{2})<f(x_{1})\end{align}$$

### First Derivative Test 
The first derivative test arises from both Fermat's Theorem, *and* Intermediate Value Theorem: 

> Let $c$ be some critical number of $f$, then: 
> * If $f'$ changes from $+\to-$ at $f'(c)$, $f'(c)$ is a local maximum. 
> * If $f'$ changes from $- \to+$ at $f'(c)$, $f'(c)$ is a local minimum. 
> * If $f'$ changes from $- \to -$ or $+ \to +$ at $f'(c)$, $f'(c)$ is neither a local maximum or minimum. 
> 
## Second Derivative Test
The second derivative of some function $f$ tells us the rate of change *of* the rate of change, or in other words; the rate of change of our derivative. Graphically, this leads to the concept of *concavity*: 
> Concavity
> If a graph of $f$ lies above all *tangents* on an interval $I$, then $f$ is concave upwards on $I$. 
> Conversely, if $f$ lies below all tangents on $I$, then $f$ is concave downwards on $I$. 

Leading us to the Concavity Test: 

> Concavity Test
> $f''(x)>0$ on some $x\in I$, then $f$ is concave upwards in $I$. 
> $f''(x)<0$ on some $x\in I$, then $f$ is concave downwards in $I$. 

Where a point $P$ in $y=f(x)$ is called an inflection point **if** there's a change of concavity present; that is extending to some Second Derivative Test: 
> Second Derivative Test: Let $f''(x)$ be continuous near values of $x=c$
> $f'(c)=0 \lor f''(c)>0$ means that $f$ has a local minimum at $c$. 
> $f'(c)=0 \land f''(c)<0$ means that $f$ has a local maximum at $c$. 

## Infinite Limits 
We now introduce the concept of an *infinite limit*, or more accurately a limit to infinity as the notation below: 
$$
\lim_{ x \to \infty } f(x) = L
$$
In terms of our [[06 — Precise Limit Definition#Epsilon-Delta Definition|Epsilon-Delta Definition]] of a limit: 
$$
\begin{align}\forall\epsilon&>0, \exists N \text{ s.t. } \\x>N &\implies |f(x)-L| < \epsilon\end{align}
$$
Once again, using our 