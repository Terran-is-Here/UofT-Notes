---
updated_at: 2026-11-09T11:09:12.301-05:00
edited_seconds: 930
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 24
Lecture Date: 2026-11-09
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[23 — Volumes]]
Next: [[25 — Inverse Functions]]
> [!quote] Recommended Reading 
> Stewart Textbook 5.3, 5.5
> We actually briefly mentioned the concept of the average value of a function in [[14 — Momentum and Impulse#^39f602|PHY180 (14) — Momentum and Impulse]]. 
> 
--- 
# Lecture Notes
## Volumes of Rotation (Continued)
> Continued from the previous lecture from a Volume of Rotation. 




---
# Pre-Lecture Notes
## Method of Cylindrical Shells
Recall in our previous note that the methods that we have used to determine the volume of a function of area over an interval, as well as the volume of a function rotated on a line. The methods we developed for these either: 
1. Requires us to inherently know the corresponding Area function being integrated (trivial)  
2. Requires us to know and or write out an equation in terms of the axis of rotation (e.g. $y=x^{3}+2x^{2}+1x+10$ in terms of some $x=?$) (non-trivial) 
3. Requires us to know the max-min behavior of a function in terms of it's smaller and larger radii (in the case of a washer) (slightly non-trivial)

This section will introduce a new method that will allow us to (potentially) compute the volume of a revolved function in a simpler manner. 

Consider taking the area of a hollow cylindrical tube; that is a tube with an inner radius $r_{1}$ and an outer radius $r_{2}$, and let's define this pipe having a height of $h$. We know that the volume of this shape is equivalent to us subtracting the interior cylinder volume by the volume of the exterior cylinder: 
$$
\begin{align}
V_{t} &  = V_{2} - V_{1} \\
 & =\pi r_{2}^{2}h - \pi r_{1}^{2} h  \\
 & =\pi(r^{2}_{2} - r_{1}^{2})h  \\
 & =\pi(r_{2}+r_{1})(r_{2}-r_{1})h  \\
 & =2\pi \left( \frac{r_{2}+r_{1}}{2} \right)(r_{2}-r_{1})h
\end{align}
$$
From here, we define the term $r$ as the average radius (that is, the midpoint of the actual, solid walls of the cylindrical shell), and $r_2-r_{1}$ as some term $\Delta r$, then: 
$$
V_{t} = 2\pi r*h*\Delta r
$$
That is, the *circumference* ($2\pi r$), the height ($h$), and the corresponding thickness $\Delta r$. 

Consider now applying this to a function, some $f(x)$. 

We can define a solid $S$ to be the function $f(x)$ revolved around some axis, define on an interval of $[a,b]$. Similarly to how we did discrete integrals previously, we can subdivide this 3d shape into $n$ subintervals $[x_{i-1},x_{i}]$, with an equal width $\Delta x$ between sample points; and letting the height of the function be defined by some $f(\bar{x}_{i})$, where $\bar{x}_{i}$ represents the midpoint of a partition, then: 
$$
\bar{x}_{i} = \frac{x_{i-1}+x_{i}}{2}
$$
And $\Delta x=\frac{b-a}{n}$; or assuming it is constant, then $\Delta x=(x_{i}-x_{i-1})$; then we see that this can be modelled as a set of hollow cylindrical shells, where the total volume of the function is given to us by the following: 
$$
V_{t} \approx \sum_{i=1}^{n} 2\pi \bar{x}_{i}f(\bar{x}_{i})\Delta x
$$
We know that this approximation improves as we take more and more subdivisions, then: 
$$
V = \lim_{ n \to \infty } \sum_{i=1}^{n} 2\pi \bar{x}_{i}f(\bar{x}_{i})\Delta x
$$
But we know this can be expressed as the following discrete integral: 
$$
V = \lim_{ n \to \infty } \sum_{i=1}^{n} 2\pi \bar{x}_{i}f(\bar{x}_{i})\Delta x = \int_{a}^{b}2\pi x \cdot f(x)\,dx
$$

Note that in this context, $2\pi x$ represents the circumference of an infinitesimal cylindrical shell, $f(x)$ represents the height and $dx$ represents the thickness, and $a,b$ represents the integration bounds of the function in terms of it's original axis.  

### Application

For instance, find the volume of the solid obtained by rotating around the y-axis the region bounded by $y=2x^{2}-x^{3}$, and $y=0$. 

From our functions above, we know that the region bounded by our function is between $x\in[0,2]$, as $y=2x^{2}-x^{3} \to x^{2}(2-x)$. We can also identify that the leading term of *height* of the function will be $2x^{2}-x^{3}$, then: 

$$
\begin{align}
V  & = \int_{0}^{2}2\pi x(2x^{2}-x^{3})\,dx \\
 & =2\pi \int_{0}^{2}2x^{3}-x^{4}\,dx \\
 & =2\pi\left[ \frac{2}{4}x^{4} - \frac{x^{5}}{5} \right]^{2}_{0} \\
 & =2\pi\left[ \frac{x^{4}}{2} - \frac{x^{5}}{5} \right]^{2}_{0} \\
 & =2\pi\left[ 8 - \frac{32}{5} \right] = \frac{16\pi}{5}
\end{align}
$$

Note that the term of height of a function is the main thing we are trying to determine. 

For instance find the volume of the solid obtained by rotating around the y axis the region between $y=x$ and $y=x^{2}$. 
We know that the bounds of this function are $[0,1]$ from inspection, then we note that the circumference is some term $x$, height as some term $f(x) = (x-x^{2})$, then the volume is therefore given by the following: 
$$
\begin{align}
V & = \int_{0}^{1}2\pi x(x-x^{2)})\,dx \\
 & = 2\pi \int_{0}^{1}x(x-x^{2})\,dx \\
 & =2\pi\left[ \frac{x^{3}}{3}-\frac{x^{4}}{4} \right]^{1}_{0} \\
 & =2\pi\left[ \frac{1}{3}-\frac{1}{4} \right] = \frac{\pi}{6}
\end{align}
$$
### Comparison
> [!caution] Note for Future Lagrange
> Look at this section please! 


When considering the Method of Cylindrical Shells and Solids of Revolution, what arises is the question of which variable is more trivial to work with in terms of determining the volume of a rotated region / function? 

The Method of Cylindrical Shells lets us define the volume through some $y=f(x)$, where the difficulty is comparing the corresponding functions that bound that region and determining which is always greater within an interval (that is, comparing by the y axis). 
* In other words, MCS does its comparison by preserving the original region the function was defined in.
* In this context, we step with respects to $x$ (in a 2d context, moving left to right and summing the areas of the cylindrical shells)

Solids of Revolution lets us define the volume through some $x=f(y)$, where the difficulty is comparing the corresponding functions which bound the region and determining which is always greater within the interval to determine a term of radius (that is, by comparing directly inline with the axis of rotation). 
* In other words, SoR does its comparison by directly comparing the functions in a plane normal to the axis of rotation. 
* In this context, we step with respects to $y$ (in a 2d context, moving from bottom to top, summing the areas of the cross-sections along that axis)
## Average Function Value
Consider the common case in which we need to take the average value of a function, we know that we can take the finite average of a set of values as the following: 
$$
\bar{x} = \frac{x_{1}+x_{2}+\dots+x_{i}}{i}
$$
Where $x_{1},x_{2},\dots x_{i}$ are values of the function. How about taking the average *value* of a function, some $f(x)$. An average implies we need to take some sample points, and we already have a developed framework for that.

Consider a function $f(x)$ within the interval $[a,b]$. As we have done for multiple times within this unit, we know that we can divide this up into $n$ even segments by $\Delta x=\frac{b-a}{n}$; where $\Delta x$ is our even spacing. We can rearrange this equation to see that $n=\frac{b-a}{\Delta x}$. Considering that this splits up the function into $n$ partitions of $[x_{i-1},x_{i}]$, and $x^{*}_{i}\in[x_{i-1},x_{i}]$, then we can see our sample points as these $x^{*}_{i}$, thus: 
$$
\begin{align}
\bar{f(x)}  & = \frac{\left( \sum_{i=1}^{n} f(x_{i}^{*}) \right)}{n} & n=\frac{b-a}{\Delta x} \\
 & =\frac{\left( \Delta x\sum_{i=1}^{n} f(x^{*}_{i}) \right)}{b-a} \\
 & =\frac{1}{b-a}\sum_{i=1}^{n} f(x^{*}_{i})\Delta x
\end{align}
$$
We know that this approximation improves as we take the limit as $n\to \infty$, and we know that that is equivalent to the discrete integral $\int_{a}^{b}f(x)\,dx$, thus: 
$$
\bar{f(x)} = \frac{1}{b-a}\int_{a}^{b}f(x)\,dx
$$
> [!theorem] Average Function Value
> $$\bar{f(x)}=\frac{1}{b-a}\int_{a}^{b}f(x)\,dx$$

Note that this is actually a small part of the MVT for Integrals: 

> [!theorem] Mean Value Theorem (Integrals) 
> If $f(x)$ is continuous in $x\in[a,b]$, $\exists c\in[a,b]$ such that: 
> $$f(c)=\bar{f}=\frac{1}{b-a}\int_{a}^{b}f(x)\,dx$$
> That is,
> $$f(c)(b-a)=\int_{a}^{b}f(x)\,dx$$
### Proof
Recall the Mean Value Theorem: 
> [!theorem] MVT 
> If $f$ is differentiable on the open interval $(a,b)$ **AND** continuous on the *closed* interval $[a,b]$, then there is *at least* one number $c\in(a,b)$, where: 
> $$f'(c) = \frac{f(b)-f(a)}{b-a}$$

Consider now we let $F(x)=\int_{a}^{x}f(x)\,dx$. We know from [[20 — The Fundamental Theorem of Calculus#Fundamental Theorem of Calculus|FToC]] that $F'(x)=f(x)$, then $F'(c)=f(c)$, thus: 
$$
\begin{align}
F'(c)  & = \frac{1}{b-a}\left( \int _{a}^{b}f(x)\,dx -\int_{a}^{a}f(x)\,dx\right) & \int_{a}^{a}f(x)=0 \\
f(c)  & =\frac{1}{b-a}\int_{a}^{b}f(x)\,dx \\
f(c)(b-a) & =\int_{a}^{b}f(x)\,dx
\end{align}
$$
Which is what we intended to prove. 