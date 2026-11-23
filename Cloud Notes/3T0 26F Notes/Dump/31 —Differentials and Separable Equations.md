---
updated_at: 2026-11-23T11:41:07.798-05:00
edited_seconds: 940
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 31
Lecture Date: 2026-11-26
Week: 11
Created: November 21st 2026, 4:08:52 pm
---
Hub: [[ESC194 Hub]]
Previous: [[30 — Indeterminate Forms and l’Hospital’s Rule]]
Next: [[32 — Exponential Growth, Decay and Population Growth]]

> [!quote] Recommended Reading 
> Section 9.1 and 9.3 of the Stewart Textbook
> Also, refer to [[18— Numerical Solutions to Second Order Differential Equations]] and [[17 — Numerical Solutions to First Order Differential Equations]] from ESC103, as these also pertain to differentials. 
--- 
# Lecture Notes
## Introduction
Recall that velocity is equivalent to the first derivative of position, and acceleration being the second derivative of position, that is: 
$$
\begin{align}
v  & = \frac{dx}{dt}  \\
a  & =\frac{dv}{dt} = \frac{d^{2}x}{dt^{2}}
\end{align}
$$

In many field of engineering, what normally happens is that a function is often defined in terms of how other characteristics present within the equation change. For instance, consider the temperature within a Fusion Reactor: 

$$
\frac{dT}{dt} \propto P_{in}-P_{out}
$$
Where the more power is input, the rate of the change of temperature increases; if less power is input, then the rate of change of the temperature decreases. Consider, that intuitively, this would also depend on the inherent temperature of our plasma, where: 
$$
\frac{dT}{dt} \propto AT^{-3/2} - BT^{1/2} - C \frac{dT}{dx} + P^{fus}(T)
$$
Where:
* $AT^{-3/2}$ corresponds to resistive heating
* $Bt^{1/2}$ corresponds to bremsstrahlung. 
* $C \frac{dT}{dx}$ corresponds to fusion heating, 
* $P^{fus}(T)$ corresponds to the power from fusion
Note how all of these are correlated to real terms and properties, however the solution to this is complicated. This is an example of a Differential Equation. 
## Differential Equations (LEC)
Differential equations are defined as the following: 
> [!theorem] Differential Equations (LEC) 
> A Differential Equation (DE) is an equation which contains an unknown function and one or more of it's derivatives. 

A trivial case could be: 
$$
\frac{dy}{dx} = ky
$$
Where this corresponds to exponential growth (the solution is $y$. We also have Newton's Second Law: 
$$
F = ma = m \frac{d^{2}x}{dt^{2}}
$$
However, things could also get more complicated in terms of other differentials, such as Faraday's Law: 
$$
\nabla \times \vec{E} = -\frac{\vec{B}}{dt}
$$
Where this is a 3D equation system of differentials. We also have Gauss's Law: 
$$
pC_{p} \frac{dT}{dt}
$$
= u dp


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

Is it a differential to the following expressions?:
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
Consider that we have considered functions from a general standpoint. In terms of attempting to solve them, we introduce the first family of differential functions that we can solve. 

Consider the following expression: 

$$
\frac{dy}{dx} = f(x)g(y)
$$

Where we note this is a Separable Differential equation, where $\frac{dy}{dx}$ can be expressed / factored into two functions of some $f(x)$ and $g(y)$. Consider that if $g(y)\neq 0$, then we can also express this in terms of some $h(y) = \frac{1}{g(y)}$, thus: 

$$
\frac{dy}{dx} = \frac{f(x)}{g(y)}
$$

If we want to solve this, we can rearrange in terms of their differentials, and integrate from there: 

$$
\begin{align}
g(y) \, dy  & = f(x)\,dx \\
\int g(y)\,dy & = \int f(x)\,dx
\end{align}
$$

Where this often provides us a solution. Note that this does not always result in an explicit expression, but a usable one nonetheless. We can actually work backwards from that definition above: 

$$
\begin{align}
\frac{d}{dx}\int g(y)\,dy & = \frac{d}{dx}\int f(x)\,dx \\
g(y) \frac{dy}{dx}& = f(x) \\
\frac{dy}{dx}  & = \frac{f(x)}{g(y)}
\end{align}
$$

### Examples
We introduce a trivial case: 

$$
\begin{align}
\frac{dy}{dx} & = \frac{x^{2}}{y^{2}} \\
y^{2}dy & = x^{2}dx \\
\int y^{2}\,dy & = \int x^{2}\,dx \\
\frac{y^{3}}{3}  & = \frac{x^{3}}{3}+C \\
y  & = \sqrt[3]{ x^{3}+3C } = (x^{3}+3C)^{1/3}
\end{align}
$$

Noting that this satisfies our earlier expression, as: 

$$
\frac{dy}{dx}= \frac{1}{3}(x^{3}+3C)^{-2/3}*3x^{2} = \frac{x^{2}}{(x^{3}+3C)^{2/3}}
$$

And this satisfies our expression as expected. Consider now the following Differential expression: 

$$
\begin{align}
\frac{dy}{dx}  & = \frac{6x^{2}}{2y + \cos y} \\
(2y + \cos y)dy & = 6x^{2}dx \\
\int 2y + \cos y \,dy  & = \int 6x^{2}dx \\
y^{2} + \sin y  & = 2x^{3} + C
\end{align}
$$

Note that we can't inherently solve this now explicitly with respects to $y$, but we can show this is a valid solution by performing implicit differentiation: 

$$
\begin{align}
\frac{d}{dx}(y^{2} + \sin y)  & = \frac{d}{dx}(2x^{3}+C) \\
2y* \frac{dy}{dx} + \cos y \frac{dy}{dx} & = 6x \\
(2y + \cos y)\frac{dy}{dx} & =6x \\
\frac{dy}{dx} & =\frac{6x}{2y + \cos y}
\end{align}
$$

Which is as expected. 
### Orthogonal Trajectories
Consider now the idea that we want to have some function where it will *always* be perpendicular to some other function at the point of intersection. That is to say, we want a family of curves where each curve intersects the family orthogonally. 

For example, we will consider finding the orthogonal trajectories of the family of curves of $x=ky^{2}$. Differentiating with respects to $x$, we find that: 
$$
\begin{align}
\frac{d}{dx}x & = \frac{d}{dx}ky^{2} \\
1  & =2ky \frac{dy}{dx} \\
\frac{dy}{dx} & = \frac{1}{2ky}
\end{align}
$$
To solve for any term of $k$, we note that $x=ky^{2}$, thus $k=\frac{x}{y^{2}}$, then: 
$$
\frac{dy}{dx} = \frac{1}{2 * \frac{x}{y^{2}}y} = \frac{y}{2x}
$$
Noting that we want to now solve for a *family of equations* orthogonal at the point of intersection, we simply take the negative reciprocal (as is the way we find orthogonality in $\mathbb{R}^{2}$, thus: 
$$
\frac{dy}{dx} = -\frac{2x}{y}
$$
Noting that this is a Separable equation, we can solve it using methods that we already know: 
$$
\begin{align}
y\,dy  & = -2x \,dx \\
\int y \,dy & = \int -2x\,dx \\
\frac{y^{2}}{2} & = -x^{2} +C \\
\frac{y^{2}}{2} + x^{2}  & = C
\end{align}
$$
Noting that this actually represents an *elipse* in our plane.