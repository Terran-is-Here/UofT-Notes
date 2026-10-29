---
updated_at: 2026-10-29T18:50:05.096-04:00
edited_seconds: 270
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 23
Lecture Date: 2026-10-29
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[22 — Areas Between Curves]]
Next: N/A
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

> Areas & Definite Integrals
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
 & =2\pi\left[ \frac{1}{3}r^{3}-\frac{1}{3}x^{3} \right]_{0}^{r} \\
 & =2\pi
\end{align}
$$

