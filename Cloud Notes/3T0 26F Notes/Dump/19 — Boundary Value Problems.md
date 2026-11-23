---
updated_at: 2026-11-23T12:24:42.191-05:00
edited_seconds: 250
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 19
Lecture Date: 2026-11-23
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[18— Numerical Solutions to Second Order Differential Equations]]
Next:
> [!quote] Recommended Reading 
> [[17— Optimization, Antiderivatives and Sigma Notation]], [[19 — The Definite Integral]]


--- 
# Lecture Notes
Recall that previously, we were able to step forward from the initial value of a set of differentials, then stepping forward by a time step to solve for a numerical solution of the value of a function. 

Instead of initial conditions, we could instead be given information about $y$ at **both ends** of the interval. In other words, we are given information pertaining to the boundaries of our expression. This is what we term as a **boundary value problem**. 

## BVPs (Boundary Value Problems) 
Note that now, we let $x$ be our independent variable, where $x$ is a spatial variable (instead of $t$ being our independent variable, some temporal derivative instead). 

> Note that in IVPs, we often had $t$ being our independent variable, with our function being defined with respects to some time. In this process, we step forwards with respect to the slopes at the points we evaluate (IEM / EM) 

For BVPs, We have the start and end points, and we want to interpolate **between these values**. How do we actually solve these though? We will use the Finite Difference Method! 

## Finite Difference Method 
We define the Finite Difference Method with respects to the following. Given two boundaries $a,b$, that is $x_{a}=a$, $x_{b}=b$ then: 
1. We divide the interval $[a,b]$ into $n$ equally spaced intervals, between $x=a$, $x=b$, that is: 
   $x_{i}^{*} = a+\frac{a-b}{n}i$, Where the width is defined by our familiar friend, $\Delta x = \frac{b-a}{n}$ where this represents our step size. 
2. For each interval present, that is between some $x_{i},x_{i+1}$, or $[x_{i-1},x_{i}]$, we are going to approximate the differential equation as a **finite difference** within the interval. 
   In other words, instead of solving the differential, we simply solve a linear equation.
	1. But how do we do this? ~~see the later parts of the note~~
3. We then repeat for every interval, then we build a system of $n-1$ linear equations, which can be solved using the methods that we have established previously within this course. 

The question now is, what do we define as a *finite difference*? Recall from calculus, we can take the instantaneous slope of a function as: 
$$
\frac{dy}{dx} =\lim_{ h \to 0 }   \frac{f(x+h)-f(x)}{h}
$$
We can approximate this by not taking the limit of $h \to0$, or in other words, defining a secant line with two points: 
$$
\frac{dy}{dx} \approx \frac{f(x+)}{}
$$
