---
updated_at: 2026-11-01T12:50:51.919-05:00
edited_seconds: 750
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 23
Lecture Date: 2026-10-29
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[22 — Areas Between Curves]]
Next: [[24 — Volumes by Cylindrical Shells and Average Function Values]]
> [!quote] Recommended Reading 
> Section 5.2 of the Stewart Textbook. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Volumes
Recall that within [[18 — Areas and Distances]], we were forced to confront the idea of taking the area of some function under a curve. The question then arises, surely we can draw a parallel to this, and taking the volume of some $3d$ shape right? 

We now consider the simple concept of a **cylinder**, a 3d object which takes a constant area $A$ at some base plane $b_{1}$, and has some height $h$, on a plane perpendicular to $b_{2}$, then we can intuitively say that: 
$$
V = Ah
$$
where $A$ is the area in $b_{1}$, and $b_{2}$ is it's corresponding height.

Consider now if an object $S$ is not a cylinder, that is $A$ varies as a function of $h$. We can intuitively think that we can approximate the area by splitting up $S$ into sections, then approximating those sections by a cylinder, that is: 
$$
A_{S} = \sum_{i=1}^{N} A(h)\Delta h
$$
Letting $x$ be defined as the term for $h$, and defining that our shape goes from some interval $x\in[a,b]$, then we note that dividing $S$ into $n$ slabs of $\Delta x$, progressively slicing smaller and smaller and taking some sample points $x^{*}_{i}$ within sub partitions (slices) $x^{*}_{i}\in[x_{i-1},x_{i}]$. 

We note that this approximation gets more and more accurate as $\lim_{ n \to \infty }$, then we have: 
$$
A_{s} = \lim_{ n \to \infty } \sum_{i=1}^{n} A(x^{*}_{i})\Delta x_{i}
$$
Where we see that this is actually simply a Reimann Sum of our function of area, thus we can define this using our familiar definite integral notation as the following. 

> [!theorem] Areas & Definite Integrals
> Let $S$ be a solid that lies between $x=a,b$. If the cross-sectional area of $S$ in the plane $P_{x}$ ($P_{x}\perp x$) is defined by some function $A(x)$, where $A(x)$ is continuous in $[a,b]$, then the volume of $S$ is defined as the definite integral of $A(x)$ between $a,b$, or in other words: 
> $$V = \lim_{ N \to \infty } \sum_{i=1}^{N} A(x^{*}_{i})\Delta x_{i}=\int_{a}^{b}A(x)\,dx$$
> Which makes intuitive sense if you think about it; it's simply the sum of the areas of infinitesimal slices of a 3d object. 

### Application
For instance, we want to derive an expression for the volume of the sphere. Or in other words, show that the volume of a sphere of radius $r$ is defined by $\frac{4}{3}\pi r^{3}$. 

We know that the function of area for this will be defined as some $A(P)=\pi P^{2}$, as the cross-section is some circle with radius $P$. 

We also know that, with a sphere with a radius $r$, we can define $P$ from P Theorem by noting that $P$ will be perpendicular to the $x$ axis; then $P=\sqrt{ r^{2}-x^{2} }$; and thus $A(P)  = A(\sqrt{ r^{2}-x^{2} })$, then $A(x)=\pi(r^{2}-x^{2})$. Taking the integral of this from $-r,r$ gives us the following: 

$$
\begin{align}
V & =\int_{-r}^{r}A(x) \,dx \\
 & =\int_{-r}^{r}\pi(r^{2}-x^{2})\,dx \\
 & =\pi\int_{-r}^{r}(r^{2}-x^{2})\,dx  & \text{Integral of even function} \\
 & =2\pi\int_{0}^{r}(r^{2}-x^{2})\,dx \\
 & =2\pi\left[ r^{2}x-\frac{1}{3}x^{3} \right]_{0}^{r} \\
 & =2\pi\left[ r^{3}-\frac{1}{3}r^{3} \right] = \frac{4}{3}\pi r^{3}
\end{align}
$$

## Rotational Volumes 
Consider now the case in which we want to revolve a *region* around a line in order to obtain some concept of an *volume*; such as revolving the function $f(x)=\sqrt{ x }$ around the $x$ axis to get it's volume. 

Consider now that in this case; whenever we revolve some function around an axis, the corresponding cross-sectional function $A(x)$ will be based in terms of a circle (as we are revolving it), thus $A(x) = \pi r(?)$, where $r(?)$ is the function that corresponds to the radius (or in other words, the region) of our original function. 

For instance, given $f(x)=\sqrt{ x }$, let's say that we wanted to revolve it around the $x$ axis and solve for the corresponding volume in $[0,1]$; then we see that the corresponding term of radius will be some term of $\sqrt{ x }$, thus $A(x) = \pi(\sqrt{ x })^{2}= \pi x$, then $\int_{0}^{1}\pi x\,dx =\frac{\pi}{2}$. 

### Multiple Functions
Consider now the case in which we want to take the volume between two functions $f(x),g(x)$; that is the volume defined from the region enclosed between two functions. In these cases, (and generally, for multiple functions depending on which one is the upper bound / lower bound respectively), we can model this as a disk (or the subtraction of two corresponding circular cross-sections): 
$$
A(x) = \pi(\text{outer radius})^{2} - \pi(\text{inner radius})^{2}
$$
Where the outer radius and inner radius correspond to the functions $f(x),g(x)$ per region (as per the same ideas that we had in [[22 — Areas Between Curves#Areas Between Curves|Areas Between Curves]]). Note that if a volume is fully enclosed, **then the integration bounds are defined with respects to the points of intersection of the function** (as without it, it's not really an enclosed shape now is it?)

> [!axiom] Idea
> Another way to think of this, is that the corresponding functions which we are revolving around, define the "edges" of the 3d shape. 

For instance, let's say we wanted to find the volume of the region **enclosed** by $f(x)=x$ and $g(x)=x^{2}$, rotated around the $x$ axis. We know elementarily that the points of intersection will be $(0,0),(1,1)$; thus our integration bounds will be $[0,1]$. 

Consider now the region formed between $g(x)$ and $f(x)$. We note that $f(x)\geq g(x)$ within $[0,1]$, then we can define the inner radius as based of $f(x)$, and the corresponding outer radius as being defined from $g(x)$. We know the corresponding radii are directly linked to our functions, thus: 

$$
\begin{align}
A(x)  & = \pi(x)^{2} - \pi(x^{2})^{2} \\
 & =\pi(x^{2}-x^{4})
\end{align}
$$
Then, integrating this: 
$$
\begin{align}
 & =\int_{0}^{1}A(x)\,dx \\
 & =\pi \int_{0}^{1}(x^{2}-x^{4})\,dx \\
 & =\pi \left[ \frac{x^{3}}{3} - \frac{x^{5}}{5} \right]^{1}_{0} \\
 & =\pi\left[ \frac{1}{3}-\frac{1}{5} \right] = \frac{2\pi}{15}
\end{align}
$$

Note however, that the term that we define as our *radius* varies depending on the line of the axis of rotation that we choose, for instance; if we decide to take our axis of rotation around some other line, e.g. some line $y=2$, then the corresponding terms for radius change accordingly (i.e. $r=2-f^{*}(x)$). 

## Cross-Sectional Area
Note however that we have generally defined the concept of area within this note as the integral of a function of *area* with respects to a distance. Previously, we defined this in terms of a circle or a disk (in terms of rotation, for instance); but we can define this to be any arbitrary function within our context. 

For instance, consider finding the volume of a *pyramid* with a square base with a side length of $L$, and a height of $h$. 

We can consider trying to find the side area of some cross-sectional square within the triangle, some $s^{*}$. We see that as we traverse a distance of $x$ in the axis of $h$, $s\to L$, or in other words, $s^{*} = \frac{Lx}{h}$, where when $x=h,s^{*}=\frac{L}{2}$. (as we considered the purely vertical axis), Then the area of that cross-section is defined by $s^{2*}$, then: 
$$
A(x) = \frac{L^{2}x^{2}}{h^{2}}
$$
Note that we are now integrating from some origin point (for convenience, set it when $A(x)=0$), towards $h$, then: 
$$
\begin{align}
 & =\int_{0}^{h}A(x) \,dx \\
 & =\int_{0}^{h}\left[ \frac{L^{2}x^{2}}{h^{2}} \right]\,dx = \left[ \frac{L^{2}x^{3}}{3h^{2}} \right]^{h}_{0} \\
 & =\frac{L^{2}h^{3}}{3h^{2}} = \frac{L^{2}h}{3}
\end{align}
$$
In fact, we can arbitrarily use any $A(x)$ as long as it can properly model the cross-section of the shape that we are attempting to understand the volume of. 