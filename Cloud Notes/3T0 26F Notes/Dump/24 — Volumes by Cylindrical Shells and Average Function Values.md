---
updated_at: 2026-11-01T14:29:20.662-05:00
edited_seconds: 380
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 24
Lecture Date: 2026-11-01
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[23 — Volumes]]
Next: N/A
> [!quote] Recommended Reading 
> Stewart Textbook 5.3, 5.5
> We actually briefly mentioned the concept of the average value of a function in [[14 — Momentum and Impulse#^39f602|PHY180 (14) — Momentum and Impulse]]. 
> 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Method of Cylindrical Shells
Recall in our previous note that the methods that we have used to determine the volume of a function of area over an interval, as well as the volume of a function rotated on a line. The methods we developed for these either: 
1. Requires us to inherently know the corresponding Area function being integrated (trivial)  
2. Requires us to know and or write out an equation in terms of the axis of rotation (e.g. $y=x^{3}+2x^{2}+1x+10$ in terms of some $x=?$) (non-trivial) 
3. Requires us to know the max-min behavior of a function in terms of it's smaller and larger radii (in the case of a washer) (non-trivial)

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
And $\Delta x=\frac{b-a}{n}$; or assuming it is constant, then $\Delta x=(x_{i}-x_{i-1})$; then 

We then note that we can model these subdivisions by some hollow cylindrical shell; with 