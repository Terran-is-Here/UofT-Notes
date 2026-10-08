---
updated_at: 2026-10-08T10:17:19.502-04:00
edited_seconds: 750
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
Next: [[15 — Summary of Curve Sketching ]]
> [!quote] Recommended Reading 
> Chapter 3.3, 3.4 of the Stewart Textbook. 
> [[12 — Related Rates, Min and Max Values#Fermat's Theorem]]
> [[06 — Precise Limit Definition#Epsilon-Delta Definition]]
> [[13 — Mean Value Theorem, Linear Approximations and Differentials#Mean Value Theorem]]

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
\begin{align}\lim_{ x \to \infty } f(x) &= L\\\forall\epsilon&>0, \exists N \text{ s.t. } \\x>N &\implies |f(x)-L| < \epsilon\end{align}
$$
Once again, using our knowledge on $\epsilon-\delta$, that we want to write $N$ as some term of $\epsilon$ (or more accurately, choose some $N=?\epsilon$ such that we can back-substitute back to $|f(x)-L|<\epsilon$). Graphically, what this means is that for some arbitrarily large value of $x$ larger than $N$, we can progressively bound it to a smaller and smaller $\epsilon$. This is also defined in terms to negative infinity: 
$$
\begin{align}
\lim_{ x \to -\infty } f(x) & =L  \\
\exists\epsilon&>0,\exists N\text{ s.t.} \\
x<N &\implies |f(x)-L| < \epsilon
\end{align}
$$

> [!ila] Application
> Note that this concept is not limited in application to determining the end behaviors of a function; this can also be applied in the following limit: 
> $$\lim_{ x \to \infty } \frac{1}{x}=0$$
> A proof is attached below: 
> > [!theorem]- Proof
> > $$\begin{align}\lim_{ x \to \infty } \frac{1}{x} = 0  \\\forall \epsilon>0, \exists N \text{ s.t. } \\x> N &\implies |f(x) -0| < \epsilon\end{align}$$
> > First, let's determine a good choice of $N$: $$\begin{align}\left|\frac{1}{x}\right|  < \epsilon && x > N \implies x > N > 0 \implies \left| \frac{1}{x}\right|=\frac{1}{x}\\-\epsilon < \frac{1}{x} < \epsilon && \forall x>0, -\epsilon< \frac{1}{x} \text{ is always true}\\x > \frac{1}{\epsilon} && \implies \text{Choose } N=\frac{1}{\epsilon}\end{align}$$
> > With our choice of $N$, we now seek to prove the forwards direction. $$\begin{align}x > N   = \frac{1}{\epsilon} \\x> \frac{1}{\epsilon} \\\frac{1}{x} <  \epsilon &&x > N > 0 \implies \frac{1}{x} = \left| \frac{1}{x}\right|\\\left| \frac{1}{x}\right| < \epsilon\end{align}$$
## Precise Infinite Limit
Combining our definitions above; then we can show that a limit diverges to infinity by the following precise definition: 
$$
\begin{align}
\lim_{ x \to \infty } f(x) = \infty \\
\forall M, \exists N \text{ s.t.} \\
x>N \implies f(x) > M
\end{align}
$$
The negative definition also exists for this; follow the same logic to write $N$ as some term of $M$. 