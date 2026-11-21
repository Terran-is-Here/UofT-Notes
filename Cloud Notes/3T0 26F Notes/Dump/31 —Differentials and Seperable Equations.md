---
updated_at: 2026-11-21T17:08:22.926-05:00
edited_seconds: 580
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

We note how $P(t)=0,M$ are valid solutions, as this resolves to the right side evaluating to some term of 0 (as $\frac{dP}{dt}M = \frac{dP}{dt}0 = 0$). 
$$
\begin{align}
\frac{dP}{dt}  & = k(0)\left( 1-\frac{0}{M} \right) = 0 \\
\frac{dP}{dt} & = k(M)(1-1) = 0
\end{align}
$$
These cases imply that at these values, the rate of change is 0; or in other words, the original function does not change in value. Constant solutions to differential equations at some time $t$ are noted as equilibrium solutions (as the original equation's value does not inherently change). 
## General Differentials 
Differentials are generally equations which involve some function and some differentials of that function. We note that the *order* of a differential equation is equivalent to the highest degree derivative present within that expression. For instance: 
$$
y' = xy
$$
Where $y$ is some function of $(x)$, and that this holds true for all values of $x$. We can offer a trivial case here, consider the following expression: 
$$
y' = x^{3}
$$
By inspection (or integrating), we find that $y= \frac{x^{4}}{4}+C$ is a valid expression to this problem, however finding analytical solutions may not always be as apparent. 
### Example
Consider the following expression: 
$$
y = x + \frac{1}{x}
$$
Is it a differential to the following expressions:
* $xy' + y =2x$
* $xy''+ 2y' = 0$

Finding the first and second derivatives respectively: 
$$
\begin{align}
y'  & = 1 -\frac{1}{x^{2}} \\
y''  & = \frac{2}{x^{3}}
\end{align}
$$
Plugging these into our earlier expressions: 
$$
\begin{align} 
xy' + y  & = 2x\\
x\left( 1-\frac{1}{x^{2}} \right)+ x + \frac{1}{x} = x - \frac{1}{x} + x + \frac{1}{x} = 2x  & = 2x
\end{align}
$$
$$
\begin{align}
xy'' + 2y'  & = 0 \\
x\left( \frac{2}{x^{3}} \right) + 2\left( 1-\frac{1}{x^{2}} \right) =  \frac{2}{x^{2}} + 2 -\frac{2}{x^{2}} = 2  & \neq 0
\end{align}
$$
## Initial Value Problems
Note that we could theoretically solve for any arbitrary number of functions within the family of functions that could satisfy our differential equation. We often however want to solve this with a set of constraints, such as the initial value of the problem; leading to the term, an initial value problem. 

For the purpose of this section, we will use the same question as was used within the textbook: 
$$
y' = \frac{1}{2}(y^{2}-1)
$$
Where we want to show that the following is a solution: 
$$
y = \frac{1+ce^{t}}{1-ce^{t}}
$$
Noting that differentiating this gives us: 
$$
y' = \frac{ce^{t}(1-ce^{t}) -(1+ce^{t})(-ce^{t}) }{(1-ce^{t})^{2}} = \frac{ce^{t} - ce^{2t} +ce^{t} +ce^{2t}}{(1-ce^{t})^{2}} = \frac{2ce^{t}}{(1-cet)^{2}}
$$
And plugging it into our expression above: 
$$
\frac{1}{2}\left( \left( \frac{1+ce^{t}}{1-ce^{t}} \right)^{2} - 1 \right) = \frac{1}{2}\left( \frac{(1+ce^{t})^{2 }-(1-ce^{t})^{2}}{(1-ce^{t})^{2}} \right) = \frac{1}{2}\left( \frac{4ce^{t}}{(1-ce^{t})^{2}} \right)
$$
From here, we note that the right and left sides would become equal. In other words, this is a valid solution to the differential. Consider now if we wanted to provide some initial restraint for the initial value, such as where $y(0)=2$. Plugging this into our earlier expression, we find that: 

$$
\begin{align}
y(0) = \frac{1+ce^{t}}{1-ce^{t}} = \frac{1+c}{1-c}  & = 2 \\
1+c & = 2-2c \\
c  & =\frac{1}{3}
\end{align}
$$
Thus: 
$$
y = \frac{1 + \frac{1}{3}e^{t}}{1-\frac{1}{3}e^{t}}, y' = \frac{\frac{2}{3}e^{t}}{\left( 1-\frac{1}{3}e^{t} \right)^{2}}
$$
## Separable Equations 
Consider that we have considered functions from a
