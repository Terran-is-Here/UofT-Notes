---
updated_at: 2026-10-04T18:28:25.577-04:00
edited_seconds: 220
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
Next: N/A 
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
