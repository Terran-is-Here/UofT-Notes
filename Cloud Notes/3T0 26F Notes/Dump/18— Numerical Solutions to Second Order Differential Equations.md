---
updated_at: 2026-11-17T17:43:17.391-05:00
edited_seconds: 360
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 18
Lecture Date: 2026-11-17
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[17 — Numerical Solutions to First Order Differential Equations]]
Next:

--- 
# Lecture Notes

## Two Dependent Variables
Consider now the Initial Value Problem with 2 independent variables: 
$$
\begin{align}
x'(t)  & = ax(t) + by(t) \\
y'(t) & =cx(t) + dy(t)
\end{align}
$$
Note that since these are linear systems, we can express these as the following: 
$$
\begin{bmatrix}
x' \\y'
\end{bmatrix} = \begin{bmatrix}
a & b\\c & d
\end{bmatrix}\begin{bmatrix}
x\\y
\end{bmatrix}
$$
Where our initial conditions are set at: 
$$
x(t=0) = x(0)\\
y(t=0) = y(0)
$$
Or as the following vector: 
$$
\vec{Z}_{0}=
\begin{bmatrix}
x(0) \\
y(0)
\end{bmatrix}
$$
Note that we can let our functions and our corresponding term of our matrix as the following: 
$$
\vec{Z} = \begin{bmatrix}
x\\y
\end{bmatrix}, \vec{Z'} = \begin{bmatrix}
x'\\y'
\end{bmatrix}
$$
Using this, we can use Euler's Method to step to solve: 
### Euler's Method
Recall that Euler's Method uses the concept of stepping through time to solve an IVT: 
$$
t_{n+1} = t_{n} + \Delta t
$$
Where: 
$$
\begin{align}
x_{n+1}  & = x_{n} + \Delta_{t}x'_{n} \to x_{n+1} = x_{n} + \Delta t(ax_{n} +by_{n}) \\
y_{n+1} & = y_{n} + \Delta_{t}y'_{n} \to y_{n+1} = y_{n} + \Delta t (cx_{n}+dy_{n})
\end{align}
$$
Or, in terms of a vector matrix, we find that: 
$$
Z_{n+1}=\vec{Z_{n}} + \Delta t \vec{Z_{n}'} =  \vec{Z_{n}} + \Delta tA \vec{Z_{n}}
$$

That is: 
$$
\boxed{\vec{Z_{n+1}} = \vec{Z_{n}} + \Delta tA \vec{Z_{n}}}
$$
### IEM 
Using IEM, we get the following: 
$$
\vec{Z_{n+1}^{EM}} = \vec{Z_{n}} + \Delta tA \vec{Z_{n}}
$$
Using this estimation, we get the following estimate using IEM: 
$$
\vec{Z_{n+1}^{IEM}} =\vec{Z_{n}} + \frac{\Delta t}{2}[A \vec{Z_{n}} + A \vec{Z_{N+1}^{EM}}]
$$
## Initial Value Problems to the Second Degree
Consider now if we are dealing with something with a second derivative, then: 
$$
\frac{d^{2}y}{dt^{2}}=  y''(t) = f(t,y,y')
$$
Where our requirements are now: 
* $y(t=0)=y(0)$ (Initial value of our function)
* $y'(t=0) = y'(0)$ (Initial slope of our function) 

Note that, if you consider that $x(t) = y'(t)$, then we simply get a similar case to what we had to tackle earlier. 

Note the following: 
$$
x=y' \implies x' = y'' = f(t,y,x)
$$
Thus, finding our initial conditions: 
> $y(t=0) = y(0)$
> $x(t=0) = x(0) = y'(0)$

### Example 
Consider the problem of Spring Damping. That is we have some fixed surface with a weight with a mass $M$ attached through a spring and a *damper* attached, we define that: 
$$y = 0$$
At the rest position of the spring, where positive $y$ is away from the wall. 

Finding the balance of the springs involved, we note that from Hooke's Law, we get the following restoring force if $y\to +$'ve. 
$$
F_E = -ky
$$
The damper attached will also provide friction: 
$$
F_{damper} = -by'
$$
Where this is proportional to being opposite to the velocity. That is the Damper is some function of the velocity of our object. Taking the net force, we find that: 
$$
-ky - by' = ma
$$
Or, setting this in our coordinate system, we find that: 
$$
\begin{align}
m \frac{d^{2}y}{dt^{2}}=-ky - b \frac{dy}{dt} 

\end{align}
$$
We note that our initial conditions are the following: 
* $y(t=0) = y(0)$ (Initial displacement)
* $y'(t=0) = 0$ (Starts at rest) 

Let $x=y'$, where we set it as another dependent variable, thus we find that: 
$$
y'' = x'  = -\frac{k}{m}y - \frac{b}{m}x
$$
And $y'=x$ by definition, thus rewriting this in terms of a vector equation: 

$$
\begin{bmatrix}
x'\\y'
\end{bmatrix} = \begin{bmatrix}
-\frac{k}{m} & -\frac{b}{m} \\
1 & 0 & 
\end{bmatrix}\begin{bmatrix}
x\\y
\end{bmatrix}
$$
Noting that the first matrix is $\vec{Z'}$, the second matrix is $A$, and the third matrix is $\vec{Z}$, then we also note that: 
$$
\vec{Z_{0}} = \begin{bmatrix}
x(0)\\y(0)
\end{bmatrix} = \begin{bmatrix}
0\\y(0)
\end{bmatrix}
$$

Thus, performing a single step of Euler's Method, we find that: 
$$
\begin{bmatrix}
x_{n+1}^{EM}\\y_{n+1}^{EM}
\end{bmatrix}= \begin{bmatrix}
x_{n}\\y_{n}
\end{bmatrix} + \Delta t \begin{bmatrix}
-\frac{k}{m} & -\frac{b}{m}\\1 & 0
\end{bmatrix} \begin{bmatrix}
x_{n}\\y_{n}
\end{bmatrix}
$$
Similarly, now performing Improved Euler's Method after: 
$$
\begin{bmatrix}
x^{IEM}_{n+1}\\y^{IEM}_{n+1}
\end{bmatrix} = \begin{bmatrix}
x_{n}\\y_{n} 
\end{bmatrix} + \frac{\Delta t}{2}\left( \begin{bmatrix}
-\frac{k}{m} & -\frac{b}{m}\\1 & 0
\end{bmatrix}\begin{bmatrix}
x_{n}\\y_{n}
\end{bmatrix} + \begin{bmatrix}
-\frac{k}{m} & -\frac{b}{m}\\1 & 0
\end{bmatrix}\begin{bmatrix}
x_{n+1}^{IEM}\\y_{n+1}^{IEM}
\end{bmatrix}\right)
$$
