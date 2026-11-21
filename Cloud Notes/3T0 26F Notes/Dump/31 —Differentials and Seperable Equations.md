---
updated_at: 2026-11-21T16:39:05.549-05:00
edited_seconds: 310
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

$$
\begin{align}
P(t)  & = Ce^{kt} \\
\frac{dp}{dt} & = kC^{kt} = kP
\end{align}
$$
As expected. Noting that if we set $P(0)$, we obtain that $C = P(0) = C_{0}$, or in other words, the original population, thus: 
$$
\frac{dP}{dt} = kP\\
P = C_{0}e^{kt}
$$
Where this is a valid solution to our differential. Explicit solutions to differential equations are not always possible, and sometimes these have to be solved numerically (as per in the ESC103 notes that we had earlier). 

### Equilibrium 
Consider that our earlier model for the population growth told us that population would grow exponentially with time; which is clearly untrue with the physical states of the world normally. 

This leads to us consider the more "accurate" population modelling equation known as the Logistic Population Growth function: 
$$
\frac{dP}{dt} = kP\left( 1 - \frac{P}{M} \right) 
$$
where $k=cM$, $M$ represents the logistic capacity, and $P$ represents the current population. 

We note how $P(t)=0,M$ are valid solutions, as this resolves to the right side evaluating to some term of 0: 
$$
\begin{align}
\frac{dP}{dt}  & = k(0)\left( 1-\frac{0}{M} \right) = 0 \\
\frac{dP}{dt} & = k(M)(1-1) = 0
\end{align}
$$
These cases imply that at these values, the rate of change is 0; or in other words, the original function does not change in value. Constant solutions to diff
