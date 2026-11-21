---
updated_at: 2026-11-21T16:18:27.975-05:00
edited_seconds: 170
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Lecture Date: 2026-11-21
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[30 — Indeterminate Forms and l’Hospital’s Rule]]
Next:

> [!quote] Recommended Reading 
> Section 9.1 and 9.3 of the Stewart Textbook
> Also, refer to [[18— Numerical Solutions to Second Order Differential Equations]] and [[17 — Numerical Solutions to First Order Differential Equations]] from ESC103, as these also pertain to differentials. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Differential Equations
Differential Equations, in comparison to traditional equations, are equations which relate some function as well as it's derivative. An easy example of this would be a simple differential for the rate of which population growth scales, that is: 
$$
\begin{align}
\frac{dP}{dt} = kP
\end{align}
$$
Where $P(t)$ is some function of the population of a group at some time $t$. What this differential equation essentially states, is that a function's derivative, is proportional to the original function, as well as some factor of $k$. 

If we wanted to solve this analytically, what we want to find is essentially some function, whose derivative is some constant multiple of itself. A solution to this rapidly emerges: Our e