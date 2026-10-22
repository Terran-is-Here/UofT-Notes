---
updated_at: 2026-10-22T13:30:44.234-04:00
edited_seconds: 790
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 18
Lecture Date: 2026-10-19
Week: 7
Created: October 18th 2026, 9:30:31 pm
---
Hub: [[ESC194 Hub]]
Previous: [[17— Optimization, Antiderivatives and Sigma Notation]]
Next: [[19 — The Definite Integral]]
> [!quote] Recommended Reading 
> Section 4.1 of the Stewart Textbook 
--- 
# Lecture Notes
## Sigma Notation (Continued) 
This is a continuation from the previous lecture's section on Sigma Notation; please refer to that section here: [[17— Optimization, Antiderivatives and Sigma Notation#Sigma Notation|Sigma Notation (Pre-LEC)]] or [[17— Optimization, Antiderivatives and Sigma Notation#Sigma Notation (LEC)|Sigma Notation (LEC)]]. 
Note the following summation results: 
$$
\begin{align}
\sum_{i=1}^{N} i  & = \frac{n(n+1)}{2} \\
\sum_{i=1}^{N} i^2  & = \frac{n(n+1)(2n+1)}{6} \\
\sum_{i=1}^{N} i^3 &  = \left[ \frac{n(n+1)}{2} \right]^{2}
\end{align}
$$
We will now prove the case for the second term by induction. We first take the base case, where $n=1$; then: 
$$
\sum_{i=1}^{1} i^2 = \frac{1(2)(3)}{6} = 1
$$
We now assume it works for some value $k$, then: 
$$
\sum_{i=1}^{K} i^2   = \frac{k(k+1)(2k+1)}{6}
$$
We now seek to show that this holds true for some value $n=k+1$; then: 
$$
\begin{align}
\sum_{i=1}^{k+1} i^2  & = \sum_{i=1}^{k} i^2 + (k+1)^2 = \frac{k(k+1)(2k+1)}{6} + (k+1)^2 \\
 & =\frac{k(k+1)(2k+1)}{6} + (k+1)^2 \\
 & =\frac{k(k+1)(2k+1)+6(k+1)^2}{6} = (k+1) \frac{k(2k+1) + 6(k+1)}{6} \\
\end{align}
$$
From here, the proof is trivial that you can get to the equation above, as we desired. We already proved this in the previous notes. 

## Limits Involving Sums
The proofs for these will be provided in the next term; but they have been put here as the following. 

If we have a sum to sum number of terms $n$, we can state that as some value of $f(n)$; that is: 
$$
\sum_{i=1}^{N} a_{i} = f(n)
$$
We can now define the term of a infinite set / sum as the following: 
$$
\lim_{ n \to \infty } \sum_{i=1}^{N} a_{i}
$$
Where this now describes an infinite sum, that is we took the limit of $f(n)$ to infinity. For instance, we can take this as: 
$$
\lim_{ n \to \infty } \left[ \frac{5}{n}\sum_{i=1}^{N} \left( \frac{1}{n} \right)^2 \right]
$$

Note that for the above, we can pull out a term of $n^2$, then: 
$$
\begin{align}
  & =\lim_{ n \to \infty } \left[ \frac{5}{n^3}\sum_{i=1}^{N} i^2 \right] \\
  & =\lim_{ n \to \infty } \left[ \frac{5}{n^3}* \frac{n(n+1)(2n+1)}{6} \right] \\
  & =\frac{5}{6}\lim_{ n \to \infty } \left[ \frac{(n+1)(2n+1)}{n^2}  = \frac{2n^2 + 3n + 1}{n^2} = 2 + \frac{3}{n} + \frac{1}{n^2}\right] \\
  & =\frac{5}{3}  & \text{by using }\lim_{ n \to \infty } \frac{1}{n^r} = 0
\end{align}
$$

## Integrals & The Area Problem
The Area Problem arises from the question: How do we evaluate the area under some graph of the function? We can define the area of something as some $bh$ of a rectangle; where the areas of other polygons can be described as some function proportional to a rectangle. 

Now the issue arises is that this works for flat, polygonal surfaces; it may be visibly apparent to how we apply this for smooth functions; or even smooth polygons (such as a circle).

For instance, take the function $x^2, x\in[0,1]$; and we want to know what area the function takes within this interval. 

We could define and take the area as the sum of the areas of some rectangles under the graph; where the base is some term $\Delta x$, and the height is some function of $f(x)$, where $x$ is dependent on $\Delta x$ (i.e. the width and the height). Taking $\Delta x=\frac{1}{4}$, we find that we can break up our function into four rectangles: 

$$
\begin{align}
f\left( \frac{1}{4} \right), f\left( \frac{1}{2} \right), f\left( \frac{3}{2} \right), f(1)
\end{align}
$$
Note that geometrically, this is a very vague / loose approximation of how things could be expressed. We could reduce $\Delta x$ into smaller and smaller values in order to more accurately model the area of a function under a graph. Specifically, we can define $\Delta x$ as some function relative to how many slices we want: 
$$
\Delta x = \frac{b-a}{n}
$$
Where $n$ is the number of "slices" or rectangles desired. 

For our earlier example, where $\Delta x=0.25=\frac{1}{4}$, $n=4$, thus the width is some term $\Delta x$, and the height is the values of our function tested at our sample points. For our general case, we can express the width as a term $\frac{1}{n}$, and the height as the function evaluated at these points. 

$$
\begin{align}
A_{f(x)}  & = \frac{1}{n}\sum_{i=1}^{N} \left( \frac{1}{n} \right)^2 \\
 & =\frac{1}{n^3}\sum_{i=1}^{N} i \\
 & =\frac{1}{n^3}*n()
\end{align}
$$



---
# Pre-Lecture Notes
## The Area Problem
We are now tackled with an interesting problem: *how do we find the area under a graph*? An approach that we can take is by using rectangles to approximate the area under a graph; with the height being some term $f(x)$ , and the width being some term $\Delta x$ across some interval. 

![[18 — Areas and Distances-1792374288706.webp]]The question now arises: how *do* we exactly define which side of that rectangle we use? 

We could use either the left side; or the right side of that interval defined by some $(x, x+\Delta x)$, and both would fall under our definition. 

However, note that if we take the limit as $\Delta x \to dx$; we note that the areas of these rectangles *should* converge; that is as we make $\Delta x$, the left endpoint case of our usage of rectangles converge onto the same value that the right endpoint case does. 

From here, we actually derive the concept of the discrete area under a graph. 

> [!theorem] Definition
> The area $A$ of the region $S$ that lies under some function $f$ is the *limit* of the sum of the areas of the approximating rectangles: $$A = \lim_{ n \to \infty } L_{n}=\lim_{ n \to \infty } [f(x_{0})\Delta x + f(x_{1})\Delta x+\dots+f(x_{n})\Delta x]$$
> Where $\Delta x$ is defined by dividing the interval by $n$ rectangles; or given an interval $(a,b)$; then
> $$\Delta x = \frac{b-a}{n}$$
> Note that this is more often defined as the following expression: 
> $$A=\lim_{ n \to \infty } L_{n} = \lim_{ n \to \infty } \sum_{n=1}^N~f(x_{x})\Delta x$$

Note that we can somewhat more precisely (albeit not fully) define the concept of the area under the curve by considering the intervals formed by $\Delta x$. We know from [[12 — Related Rates, Min and Max Values#Extreme Value Theorem (Proof)|EVT]] that a function will take some maximum and minimum within the intervals formed by $\Delta x$; we can denote the following: 
* The **Lower** sum is having the rectangles of the sum be defined **on** the minimum value of $f(x)$ within the intervals of $(x_{n}, x_{n}+\Delta x)$
* The **Upper** sum is having the rectangles of the sum be defined on the *maximum* value that $f(x)$ can obtain within the intervals of $(x_{n}, x_{n}+\Delta x)$

We then note that the area is the value that is **greater than** all possible lower sums, and **less than** all possible upper sums. You could also make the argument via Squeeze Theorem that if the Lower and Upper sum converge onto the same value; then the area in between will also be that value; but that's not rigorous enough to display within this note. 


