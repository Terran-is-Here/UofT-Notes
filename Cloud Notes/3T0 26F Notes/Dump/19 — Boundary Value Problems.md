---
updated_at: 2026-11-23T12:46:19.322-05:00
edited_seconds: 470
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
We can approximate this by **not** taking the limit of $h \to0$, or in other words, defining a secant line with two points, where we let $\Delta x$ be a reasonably small number, then: 
$$
\frac{dy}{dx} \approx \frac{f(x+\Delta x)-f(x)}{\Delta x}
$$
It is with this fundamental equation that we can find multiple methods to calculate a finite difference. 

> [!theorem] Forward Difference
> A forward difference is essentially this: 
> $$\Delta_{F}f(x) = \frac{f(x+\Delta x)-f(x)}{\Delta x}$$
> Where $\Delta x >0$, or in other words, we step forwards. 

> [!theorem] Backward Difference
> A backward difference is essentially us stepping backward by some term $\Delta x$: 
> $$\Delta_{B}f(x) = \frac{f(x) - f(x-\Delta x)}{\Delta x}$$
> Where we step backwards, from $f(x) \to f(x - \Delta x)$, where $\Delta x >0$

> [!theorem] Central Difference
> We can also take both, stepping forward and backward, then comparing the slopes between those two points: 
> $$\Delta_{C}f(x) = \frac{f(x+\Delta x)-f(x-\Delta x)}{2\Delta x}$$
> $\Delta x>0$, where we step over the larger interval of $[x-\Delta x,x+\Delta x]$

Note that if $\Delta x$ is reasonably small, $\Delta_{F}f(x) \approx \Delta_{B}f(x) \approx \Delta_{C}f(x)$. These methods generally approximate $\frac{dx}{dy}$. To approximate a second derivative, we can combine methods (using one method to find the first, then using another). For instance: 

$$
\begin{align}
f''(x)  & \approx \Delta_{B}[\Delta_{F}f(x)] \\
 & \approx \Delta_{B}\left( \frac{\Delta_{F}f(x) - \Delta _\text{F}f(x-\Delta x)}{\Delta x} \right) \\
 & \approx \frac{1}{\Delta x}\left( \frac{f(x+\Delta x)-f(x)}{\Delta x} - \frac{f(x)-f(x-\Delta x)}{\Delta x} \right) \\
f''(x)& = \frac{f(x+\Delta x)-2f(x)+f(x-\Delta x)}{(\Delta x)^{2}}
\end{align}
$$
### Example 
Take the following differential equation: 
$$
\frac{d^{2}y}{dt^{2}} + 2 \frac{dy}{dx} + 10y = 0
$$
Where our Boundary Conditions are given by: 
* $y(x=0)=0.75$
* $y(x=1.68)=0$
To solve this numerically using FDM: let $n=2,3,10$. 
> Note that the analytical solution for this expression is given by: 
> $$y(x) = e^{-x}\left[ \frac{3}{4}\cos(3x) + \frac{1}{4}\sin(3x) \right]$$

To start with, take $n=2$ ,then: 
![[Drawing 2026-11-23 12.40.27.excalidraw]]
Note then that : 
$$
\begin{align}
 & x_{0}   = 0 \\
 & x_{1} = \Delta x   = 0.84 \\
 & x_{2}   = 1.68 \\
 & y_{0} = 0.75 \\
 & y_{1} = ?? \\
 & y_{2} = 0
\end{align}
$$
Note that $y_{1}$ has to be a value which satisfies the differential equation, that is: 
$$
y'' + 2y' + 10y = 0
$$
Turning this into a linear equation, noting that we have three terms to turn into some algebraic equation: 

> For our $10y$ term:
$$
\begin{align}
x_{1} \implies y = y_{1}
\end{align}
$$

> For our $2y'$ term: 
$$
\begin{align}
x_{1} \implies y_{1}' = ?
\end{align}
$$
Noting that here, we can use our Finite Difference Method to solve. We note that taking the slope between our boundaries should approximate the slope of our function at that point, then: 

$$
y_{1}' \approx \frac{y_{2}-y_{0}}{2\Delta x} \tag{using central difference method}
$$


