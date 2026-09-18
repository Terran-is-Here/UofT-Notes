---
updated_at: 2026-09-18T16:35:03.931-04:00
edited_seconds: 690
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 5
Lecture Date: 2026-09-14
Week: 2
created:
Created: September 14th 2026, 5:22:05 pm
---
Hub: [[PHY180 Hub]]
Previous: [[4 — 1D Kinematics]]
Next: [[6 — Rotational Kinematics]]

> [!quote] Textbook Reading: 
> 4.1-4.3 
--- 

# Lecture Notes
# Pre-Lecture Notes

### 2D Extension
One of the core principles which allow us to analyze multi-dimension kinematics (not just $\mathbb{R}^2$, but $\mathbb{R}^n$) is the concept that dimensions within kinematics problems are linearly independent of each-other: that is $x$ and $y$ dimensions have their own movement / kinematics. 

> That is, $2d$ motion is composed of two independent $1d$ motions/kinematics.

This means that in general, we can break up any $n$-dimensional kinematics problem into an analysis of $n$ $1$-dimensional kinematics problems. Note that depending on the context, what we can learn in one axis may help us analyze another. 
#### Projectile Motion
Projectile Motion is generally defined as a 2d kinematics equation, where our $y$ axis is defined as a free-fall problem (i.e. $a_{y}=g$), and our $x$-axis (unless otherwise stated) has no acceleration. 

This means that kinematics equations for our $x$-dimension are simplified, since $v=v_{0}$. 

Our $y$-dimension does provide us with some interesting context: 
* When $\Delta y=0$, whatever object we have projectile motion on has hit the ground. 
* When $v_{y}=0$, our object is at it's "apex" (i.e. turn around window).
	* The time at this moment gives us time of max height, which can be used to solve for actual max height. 

Analysis of these one-dimensional fragments is trivial, as these can be done independently.

For instance, let us take: $\vec{v_{0}} \in \mathbb{R}^2$, then: 
$$
\vec{v_{0}} = \begin{bmatrix}
\cos\theta *|\vec{v}|  \\
\sin\theta * |\vec{v}|
\end{bmatrix}
$$
That is, $\vec{v_{0x}} = |\vec{v}|\cos\theta$ and $\vec{v_{0y}}=|\vec{v}|\sin\theta$; which we can then put into our respective $x$ and $y$ axis as their corresponding initial values. 
### Range 
Assume that we have a projectile launched on a flat surface, and we wish to determine the *distance* it travelled. We know we can find the horizontal distanced travelled by: 
$$x_{t} = v_{0x}t$$
We need to simply solve for a value of time to plug into this equation. We know at time of impact, $\Delta y=0$, then we can solve the following: 
$$0 = v_{0y}t -\frac{1}{2}gt^2 \implies 0=t\left( v_{0y} - \frac{1gt}{2} \right)$$
We know $\Delta y=0$ at $t=0$, so we try to solve for the other factor equal to 0 to solve for a value of $t$ to plug in: 
$$
v_{0y} - \frac{gt}{2} = 0 \implies t = \frac{2v_{0y}}{g} = \frac{2|\vec{v_{0}}|\sin\theta}{g}
$$
Plug it into our equation for $x_{t}$ above, then we get: 
$$
x_{t} = (|\vec{v_{0}}|\cos\theta)*\left( \frac{2|\vec{v_{0}}|\sin\theta}{g}\right)
$$
$$
x_{t} = \left( \frac{|\vec{v_{0}}|^2\sin(2\theta)}{g} \right)
$$

### Time of Flight
We already solved for a term of time of flight within our previous derivation of range: 
$$
t_{f} = \frac{2|\vec{v_{0}}|\sin\theta}{g}
$$
### Trajectory Equation
To solve for an equation to *graph* out the trajectory, we need to find some way we can present $t$ as some function of $x$. For the purposes of this, we will assume $(x_{0},y_{0}) \mapsto(0,0)$

$$
x = v_{0x}t \implies t = \frac{x}{v_{0x}} \implies t = \frac{x}{|\vec{v_{0}}|\cos\theta}
$$
Plug this into our general expression for $y$: 
$$
y = v_{0y}t +\frac{a}{2}t^2
$$
$$
y=(|\vec{v_{0}}|\sin\theta)\left(\frac{x}{|\vec{v_{0}}|\cos\theta}\right) + \frac{a}{2}\left(\frac{x}{|\vec{v_{0}}|\cos\theta}\right)^2
$$
Simplifying: 
$$
y = x\tan \theta + \frac{ax^2}{4|\vec{v_{0}}|^2\cos^2\theta} \implies y=\tan(\theta)x + \frac{a}{4|\vec{v_{0}}| \cos^2\theta}x^2
$$
From here, we can see that for these trajectories, our graph would take the form of *some* parabola, with the following values (e.g. if you were to use it in a quadratic) 
$$b = \tan\theta$$
$$a=\frac{a'}{4|\vec{v_{0}}|\cos^2\theta}$$
