---
updated_at: 2026-10-04T22:46:42.181-04:00
edited_seconds: 400
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 12
Lecture Date: 2026-10-04
Week: 5
Created: October 4th 2026, 6:14:03 pm
---
Hub: [[ESC194 Hub]]
Previous: [[11 — Trigonometric, Chain and Implicit Differentiation]]
Next: [[13 — Mean Value Theorem, Linear Approximations and Differentials]]
> [!quote] Recommended Reading 
> Stewart Textbook Ch. 2.8, 3.1 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Related Rates
Related rates are an extension of the concept of the [[11 — Trigonometric, Chain and Implicit Differentiation#Chain Rule|Chain Rule]]. For instance, the volume of a sphere is defined as the following: 
$$
V(r) = \frac{4}{3}\pi r^3
$$
If, in some case, we are given some term $\frac{dr}{dt}$'s value; we can solve for a corresponding term of $\frac{dv}{dt}$; 
$$
\begin{align}
\frac{dV}{dt} &= \frac{d\left( \frac{4}{3}\pi r^3 \right)}{dr} \frac{dr}{dt} \\
\frac{dV}{dt}&=4\pi r^2 * \frac{dr}{dt}
\end{align}
$$
Note that terms should only be substituted *after* we have appropriately differentiated some of our terms; for instance if $\frac{dr}{dt}=C$, then this should only be substituted when $\frac{dV}{dr}$ has been differentiated. 
## Maximum and Minimum Values 
We follow the following definitions for the maximum and minimum values of a function. Let $c\in D$ , where $D$ is the domain of some function $f$, then $f(c)$ is the: 
* **absolute maximum** value for $f$ if $f(c)\geq f(x)$ for all $x\in D$
* **absolute minimum** value for $f$ if $f(c) \leq f(x)$ for all $x\in D$
* **local maximum** value for $f$ if $f(c) \geq f(x)$ for all $x$ near $c$
* **local minimum** value for $f$ if $f(c)\leq f(x)$ for $x$ near $c$
Note that the definition for $x$ near $c$ is that it is true for some open interval $S\in D$ where $c\in S$. 

### Extreme Value Theorem 
The extreme value theorem is the following

> a
> > *Given:* $f$ is defined and continuous on $[a,b]$
> 
> Prove: $f$ assumes a maximum *and* minimum value on $[a,b]$. 

For us to prove this; we need to apply another theorem called the Boundness Theorem. 
#### Boundness Theorem 
The Boundness Theorem lets us show that, for any function defined and continuous on a closed interval $[a,b]$, it is bounded within that interval. 

> > *Given:* 
> > $f$ is a function defined and continuous on the interval $[a,b]$
> 
> Prove: $f$ is bounded on $[a,b]$.
> 
> Proof: 
> We can perform this proof by a contradiction. 
> > Assume that $f$ is not bounded on $[a,b]$. 
> 
> Let $c$ be the midpoint of $[a,b]$, if $f(x)$ is unbounded on $[a,b]$, then it is unbounded on either $[a,c]$ or $[c,b]$. Define now that $[a_{1},b_{1}]$ to be the half in which $f(x)$ is unbounded; if $f(x)$ is unbounded in both, take the left half. 
> 
> Progressively subdividing this gives us a set of $A$, defined by the left-most endpoints. From [[02 — The Real Number System#Completeness of the Reals Axiom (CORA)|Completeness of the Reals Axiom]] this set has some LUB $\gamma$; where $\gamma\in[a,b]$; then $f(\gamma)$ is continuous. 
> 
> Then: 
> * $\gamma=a$, then 
