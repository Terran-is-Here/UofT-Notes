---
updated_at: 2026-11-16T12:30:05.088-05:00
edited_seconds: 260
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
Checking our Initia

