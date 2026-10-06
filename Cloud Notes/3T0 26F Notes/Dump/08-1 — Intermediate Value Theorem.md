---
updated_at: 2026-10-06T16:16:14.886-04:00
edited_seconds: 370
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 10
Lecture Date: 2026-10-01
Week: 4
---
Hub: [[ESC194 Hub]]
Previous: [[08 — Continuity]]
Next: [[09 — Derivatives and Rates of Change]]
> [!caution] Note
> This note was primarily written using in-lecture notes. 

> [!quote] Recommended Reading 
> Supplement Section 4.1
> Stewart Ch. 1.8

--- 
# Lecture Notes
## Intermediate Value Theorem (IVT) 
> [!theorem] Intermediate Value Theorem
> If $f(x)$ is continuous on the closed interval $[a,b]$, and $k$ is any number strictly between $f(a)$ and $f(b)$, then **there is at least one** number $c$ on $[a,b]$ such that$f(c) =k$
> 
> What this implies that given a continuous function $f(x)$, it will take on all of it's values between $[a,b]$, where $f(a) < k <f(b), \exists c \text{ }s.t. f(c)=k$.  Or: 
> $$\begin{align}f(x), x\in [a,b] &\implies & \text{And f(x) is continuous on } [a,b]\\&\implies f(a) < k  < f(b)  \\&\implies \exists c \text{ s.t. } f(c) = k \\\\& \text{ Or, concisely:} \\f(x), x\in[a,b] &\implies f(a) < k < f(b) \implies \exists c \text{ s.t.} f(c) = k \tag{IVT}\end{align}$$
### Applied Example
Example: Show that there is *at least* one root of the equation $$f(x) = 4x^3 + 3x^2 -2x - 1$$
On the interval $[0,1]$. Using IVT, we can show this. Take our function from $[0,1]$, then for IVT, we need
$$
\begin{align}
f(a) < k &< f(b)  & \text{Root implies some value k=0 exists.}\\
f(0) < 0 &< f(1)  \\
-1 < 0 &< 4 & \text{note that f(a) < 0, f(b) > 0} \implies k=0\in[f(a),f(b)]
\end{align}
$$
Note that since $f(x)$ is a polynomial, it is continuous on any interval. Thus by $IVT$, these exists at least one location $x=c\in[0,1]\to f(c)=k=0$. 



