---
updated_at: 2026-11-16T12:51:20.694-05:00
edited_seconds: 480
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-16
Week:
---
Hub: [[16 — Solving the Least Squares Problem]]
Previous: [[16 — Solving the Least Squares Problem]]
Next: N/A

> [!quote] Recommended Reading 
> Derive and apply Euler's Method (EM) and Improve Euler's Method (IEM) for solving a first order differential equation. 

--- 
# Lecture Notes

## Introduction
Consider the idea that we have a falling ball, we know from [[7 — 1st and 2nd Laws of Newton|Newton's Second Law]] that: 
$$
F = ma
$$
Since our ball is falling, assuming that the drag force is tiny; then: 
$$
F_{g} = ma
$$
Or: 
$$
-mg = ma \to -g = a
$$
Noting that $a = \frac{dv}{dt}$, then: 
$$
-mg = m \frac{dv}{dt} = mv'
$$
Or in other words, $v'=-g$, where the rate of change of $v$ is equal to the negative of the constant of $g$ (in other words, a line going downwards by a slope of $gt$). 

### Drag Force
Consider now the case in which we have a drag force! Note that drag force is proportional to $v$; or in other words, $f_{d} \propto v$. For now, we will state that it is proportional to velocity. 

Thus, our force summation becomes the following: 

$$
F_{g} - F_{d} = mv'
$$
Expanding this, we find that: 
$$
mg - kv = m \frac{dv}{dt}
$$
> [!ila] In Lecture Idea
> A Differential Equation relates a function (in this case, an unknown), to it's derivative
> $$y' = f(y,t); y=y(t) = ???$$

## Differentials
Consider the following differential: 
$$
y' = cy\\c<0
$$
This implies that the derivative is proportional to the original function; giving us a slope field (will insert diagram here in the future)
![[Drawing 2026-11-16 12.26.05.excalidraw]]
Where the red graph is the numerical solution to some $y(t)$. We term this as an Initial Value Problem: 

## Initial Value Problems 
Given the following expression: 
$$
\frac{dy}{dt} = y' = f(t,y) = cy
$$
Where $c$ is some scalar function, we also note that we need an initial condition: 
$$
y(t=0) = y(0)
$$
To solve this problem, we solve some $y(t)$ which: 
* Satisfies the Differential Equation present
* Satisfies the original condition present. 

Noting that if a function is proportional to it's derivative, we can see that our exponential equation will answer it. Thus, an analytical solution will be: 
$$
y(t) = y(0)e^{ct}
$$
Checking our Initial Condition: 
$$
y(0) = y(0)e^{0} = y(0)
$$
And checking our differential equation, then: 
$$
\begin{align}
\frac{d}{dx} y(0)e^{ct} = cy(0)e^{ct}
\end{align}
$$
Note then that $y(0)e^{ct}=y(t)$, then we find that $y' = cy$, which means that our analytical solution above satisfies our solution. 

> [!ila] In Lecture Addendum
> Our Analytical Solution is noted as a closed form solution; noting that this gives us a fully defined function as to how our value of $y$ is defined in terms of $t$. 

Note however, that while we were able to find a solution to this differential equation, not all differential equations have analytical solutions. Instead, we can apply numerical techniques to approximate a solution.

## Euler's Method 
Given that: 
$$
\begin{align}
y'(t)  & = y(t,y) \\
y(t=0) &  = y(0)
\end{align}
$$
That is, our initial value problem earlier. As such, we know that at some value of $t$, we know the value of that function at some point. 

To find the value of our function at some time $t_{1}$, we can take some time step $\Delta t$; then we note that for some small $\Delta t$, we can approximate the value of our function as our slope. 

Or in other words, $\frac{dy}{dt}=y'$. But in the case of our analysis, we define this as $\frac{\Delta y}{\Delta t}$ (That is, we don't inherently take the limit of $\Delta t \to dt$)

Note that if we find our corresponding increment of $\Delta y$, we can use the value at that step to correspondingly update our slope, then finding another value of $\Delta t$ away. We essentially define our function as a set of lines with points which approximate the overall function. 

Mathematically, we find that: 
$$
\text{slope} = y'(t=0) = f(0,y(0))
$$
Correspondingly, we find that: 
$$
\begin{align}
y_{1} = y(\Delta t)  & = y(0) + \Delta t f(0,y(0)) \\
 & =y(0) + \Delta tf'(\Delta t)
\end{align}
$$
Or in other words, we take our initial point, and step correspondingly with the slope at that point for some small $\Delta t$, for instance if we step this forward, then: 
$$
y_{2} = y_{1} + \Delta tf(t_{1},y_{1})
$$
Where $t_{1} = 0 + \Delta t$, or generally, $t_{n} = (t=0) + \Delta tn$

Generalizing: 
$$
y_{n+1} = y_{n} + \Delta tf(t_{n},y_{n})
$$
### Errors
Note that the formula we used to go from $(t_{n},y_{n}) \to (t_{n+1},y_{n+1})$ is not exact. Noting that using the slope at $t_{n}$ may not perfectly approximate the value at $t_{n+1}$. We experienced a similar issue in this case when we linearly approximated a function [[16 — Linear Approximation and Differentials]].

To reduce error: 
* Theoretically, we can simply use smaller and smaller time steps to reduce the potential error experienced. 
	* Or in other words, if $t \in [a,b]$, we take a greater value of time intervals $n$, since $\Delta t = \frac{b-a}{n}$, increasing n decreases the corresponding term of t. 
* 

