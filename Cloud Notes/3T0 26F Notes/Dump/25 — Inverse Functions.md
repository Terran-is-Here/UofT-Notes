---
updated_at: 2026-11-10T09:07:14.144-05:00
edited_seconds: 230
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 25
Lecture Date: 2026-11-01
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[24 — Volumes by Cylindrical Shells and Average Function Values]]
Next: N/A
> [!quote] Recommended Reading 
> Stewart Textbook Section 6.1 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Inverse Functions
Consider now the case of *inverse* functions, that is, functions which reverse the mapping given by some function from $x \mapsto y$, an inverse function would $y\mapsto x$ (going the opposite direction). 

Note that for this requirement to be acceptable, consider that $f(x) \mapsto y$ **must** be a bijective (one-to-one) function. Consider the case in which for multiple $x_{1},x_{2}$ would equal some $y$, then: 
$$
f(x_{1}) = f(x_{2}) =y \implies f^{-1}(y) = x_{1} \lor x_{2}
$$
Which does *not* make sense, as our inverse function would have no means for determining between the two values present. Geometrically, this can be represented by the *horizontal line test*, which tests if a function is bijective. Formally, an inverse function is defined as the following expression: 

> Inverse Function
> Let $f$ be a bijective function that maps values from it's domain, $A$, to it's range, $B$. The *inverse* function is notated by $f^{-1}$, and maps it's domain $B$ back onto it's range, EA. For instance: 
> $$f^{-1}(y) = x \iff f(x)=y$$
> For any $y$ in $B$. 

In other words, the domain and range between inverses correspondingly reverse, as is expected. We thus obtain the following identities pertaining to evaluating Inverse Functions. 
$$
\begin{align}
 & \text{let } f^{-1}(x) = y \iff f(y)=x & y\text{ is independent variable...} \\
 & \implies f^{-1}(f(y)) = y \implies f^{-1}(f(x)) =x & \forall x\in A\\
 & \implies f(f^{-1}(x))= x & \forall x\in B
\end{align}
$$
Note that our definitions for the sets arise from how these functions relate to each other: $f(y)\mapsto B, f^{-1}(x) \mapsto A$. Both of these functions essentially return our original value; however the corresponding interior domains and ranges have a different set of values that we can correspondingly plug in. 

> Finding Inverse Functions
> Finding inverse functions is trivial