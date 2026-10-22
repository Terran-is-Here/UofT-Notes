---
updated_at: 2026-10-22T13:10:14.731-04:00
edited_seconds: 540
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


