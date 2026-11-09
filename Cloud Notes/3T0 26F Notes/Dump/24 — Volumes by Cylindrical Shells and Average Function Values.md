---
updated_at: 2026-11-09T11:50:02.227-05:00
edited_seconds: 1460
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 24
Lecture Date: 2026-11-09
Week: -18
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

Recall that a Volume of Rotation is equivalent to taking the following integral: 
$$
\int_{a}^{b}\pi(f(x))^{2}\,dx
$$
> Note that $f(x) \mapsto y$, where $y$ represents our corresponding axis of rotation. If we are revolving around some term $x$ instead; we instead consider rewriting this in terms of $y$. 

Where $f(x)$ effectively represents the radius of some infinitesimally small circle that we want to take, that is it represents some tiny disk $dA=\pi(f(x))^{2}$; then the integral is simply taking up the sum of all of these volumes from the axis. In other words, this represents us taking the volume through a method of **disks**. 

> [!theorem] Disk Method of Volumes of Rotation
> $$\boxed{\int_{a}^{b}\pi(f(x))^{2}\,dx}$$
> Where $f(x)$ represents the distance of the function from the rotational axis $x$. 

Consider now that if we wanted to rotate a function as a region between two curves. Recall that we bounded these two between functions based on the corresponding comparisons between the functions (i.e. $f(x)>g(x)$, $f(x)<g(x)$, etc.) We can picture taking the volume of this corresponding rotated shape across an axis; as taking the **area of a disk with a hole in the middle**. 

In this case, the area associated with a disk is equivalent to taking the area of the outer disk minus the area of the inner disk. Assuming that $g(x)>f(x)$, then: 
$$
A = \pi f(x)^{2} - \pi g(x)^{2}
$$
We can consider taking the volume of such a shape as the following Reimann sum: 
$$
V \approx \sum_{i=1}^{n}\pi(f(x)^{2}-g(x)^{2})\Delta x
$$
Or, when taking the limit as $||P|| \to  0$, then: 
$$
V=\int_{a}^{b}\pi[f(x)^{2}-g(x)^{2}]dx
$$
Where this represents the **washer method** across the $x$ axis. 

> Washer Method of Volumes of Rotation
> $$\boxed{\int_{a}^{b}\pi\left[f(x)^{2}-g(x)^{2}\right]\,dx}$$
> Where $f(x)>g(x) \forall x\in[a,b]$. This corresponds to the washer method of a Volume of Rotation using the $x$ axis as the axis of rotation. 

### Example
Consider the two following functions: 
* $y=x^{2}$
* $y=x$
Points of intersection are at $0,1$, then we note that $x>x^{2}$ for this bound; then drawing a rectangle, we see that the height is equivalent to $x-x^{2}$, then taaking the integral: 
$$V_{x}=\int_{0}^{1}\pi[x^{2}-x^{4}]\,dx = \pi\left[ \frac{x^{3}}{3}-\frac{x^{5}}{5} \right]^{1}_{0} = \frac{2\pi}{15}$$
Consider now revolving this across the $y$ axis, then using the same bound, then we see that $\sqrt{ y }=x, y=x$, then: 
$$
V_{y}=\int_{0}^{1}\pi[\sqrt{ y }^{2}-y^{2}]\,dy = \pi\left[ \frac{y^{2}}{2}-\frac{y^{3}}{3} \right]^1_{0} = \frac{\pi}{6}
$$

### Rotation Across Other Axis's
Consider now the case in which we rotate across another axis of rotation besides the x or y axis. For instance, let's rotate the function $f$ along some axis $y=k$. In this case, the formula still holds true; our term for radius simply increases proportionally: 

$$
V=\int_{a}^{b}\pi(f(x)-k)^{2} \,dx
$$
Note that $f(x)-k$ simply corresponds to the distance from $f(x)$ to $k$. 

> Consider now this case when we are taking a volume of rotation by some region. 

Consider that $g(x)>g(x)$ in the interval of $x\in[a,b]$, and that we are rotating this along some axis $y=k$. We define the Volume of Revolution as the following in this case then: 
$$
V = \int_{a}^{b}\pi |(f(x)-k)^{2}-(g(x)-k)^{2}|\,dx
$$
With the absolute values simply solving this in terms of a proper volume. Note that this description requires that $k<f,g$ or $k>f,g$ (that is to say, the axis can never be in the region itself). 


#### Example
Consider now the same example from above, but we rotate it along some axis $y=k=-2$: 
* $y=x^{2}$
* $y=x$

Thus, taking the integral, then noting that $x^{2}<x$, then: 
$$
\begin{align}
V  & = \int_{0}^{1}\pi|(x+2)^{2} - (x^{2}-2)^{2}|\,dx \\
 & =\pi\int_{0}^{1}|x^{2}+4x + 4 - x^{4} -4x^{2}  -4|   \,dx \\
 & =\pi \int_{0}^{1}|-x^{4} -3x^{2} + 4x|\,dx = \pi\left[ -\frac{x^{5}}{5} - x^{3}+2x^{2} \right]^{1}_{0} \\
 & =\frac{4}{5}\pi
\end{align}
$$
Note that this volume is larger than our previous case, as the effective radius of our washer correspondingly increases. 

## Volumes by Cylindrical Shells (LEC)
Consider that there may exist cases where solving for the volume via an axis of rotation may be annoying. For instance, taking the rotation of some region of some $f(x)$ around the $y$ axis. Note that this requires us to explicitly solve our function to be in terms of $y$, which may be non-trivial / difficult to perform. 

That is, using the washer method horizontally using the rectangles from the axis of rotation may be difficult. The Method of Cylindrical Shells lets us define our rectangles with respect to the original axis of the function, then simply revolving it around the axis as per usual. 

Recall that we can define the area of a rectangle under some function as some $f(x^{*}_{i})\Delta x$. Revolving this rectangle around gives us some value in terms of a shell. Then the volume of this corresponding shell is given to us by the following: 

$$
V_{i}=f(x^{*}_{i})\Delta x \times 2\pi x^{*}_{i}
$$

Note that in this equation, the term on the left simply gives us the area, while the term of the right performs a revolve extrude around this area to take the volume; then noting that we can sum up the areas as a Reimann sum, then: 
$$
V_{i}\approx \sum_{i=1}^{n}2\pi x^{*}_{i}f(x^{*}_{i})\Delta x_{i} = \int_{a}^{b}2\pi xf(x)\,dx
$$
### Regions
Consider the following two functions that enclose some region, where $f(x)>g(x)$ within $x\in[a,b]$. 
* $f(x) = \dots$
* $g(x) = \dots$

When we draw our rectangles, then the corresponding area of the rectangle is given as a function of the height, and the width, thus: 
$$
A_{i} = (f(x^{*}_{i})-g(x^{*}_{i}))\Delta x
$$
Thus the integral is given as the following: 
> [!theorem] Shell Method Of a Region about the $y$ axis
> $$V = \int_{a}^{b}2\pi x(f(x)-g(x))\,dx$$
> Note that the corresponding term is taken if we take it about the $x$ axis: 
> > $$V = \int_{a}^{b}2\pi y(f(y)-g(y))\,dy$$


Note that this allows us to integrate with respects to $x$, when we are revolving with respects to $y$. In this case, if we want to rotate across the $x$ axis, we integrate with respects to $y$ instead. A good way to differentiate between Volumes of Rotation and Volumes of Cylindrical Shells, as comparing it between a method of *cross-sections* (VoR), and a method of cylinder sections going outwards from our axis of rotation (VoCS). 

### Example
Consider now the following: 
* $F(y)=x^{2}$
* $G(y)=\sqrt{ x }$ 
Revolve this around $y$, then we note that $x^{2}<\sqrt{ y }$, and that they intersects at $0,1$, thus: 
$$
\begin{align}
V & =\int_{0}^{1}2\pi x(\sqrt{ x }-x^{2})\,dx \\
 & =2\pi \int_{0}^{1}x^{3/2}-x^{3}\,dx \\
 & =2\pi \left[  \frac{2x^{5/2}}{5} - \frac{x^{4}}{4} \right]^{1}_{0} = \frac{3\pi}{10}
\end{align}
$$

Performing this through the Washer Method: $\sqrt{ y }=x$, and $y^{2}=x$, then noting that within the interval, $y^{2}<\sqrt{ y }$, then: 
$$
\begin{align}
V & =\int_{0}^{1}\pi(\sqrt{ y }^{2}-y^{4})\,dy \\
 & =\pi \int_{0}^{1}(y-y^{4})\,dy \\
 & =\pi\left[ \frac{y^{2}}{2}-\frac{y^{5}}{5} \right]^{1}_{0}=\frac{3\pi}{10}
\end{align}
$$


Consider now the following example: 
* $y^{2}-x^{2}=1$ --> $y=\sqrt{ 1+x^{2} }$ or $x = \pm \sqrt{ y^{2}-1 }$
* $y=2$
Revolve this region around the $x$ axis. For this case, we can do it by the washer method. But for the sake of exercise, we will do it by the shell method. 

Noting that the points of intersections are at $\sqrt{ 3 },-\sqrt{ 3 }$, then we also note that since we are integrating with respects to the $y$ axis, then our bounds are $11,2$
$$
\begin{align}
V & =\int_{1}^{2}
\end{align}
$$



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