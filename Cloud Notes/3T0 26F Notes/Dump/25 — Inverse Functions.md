---
updated_at: 2026-11-11T08:51:36.448-05:00
edited_seconds: 400
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
> Finding inverse functions is trivial, noting that since an inverse function turns a mapping from $x\mapsto y$ to $y \mapsto x$. In other words, we reflect our function across the line $y=x$. In process, given some  function of $x$ mapping to $y$, we swap the terms $x$,$y$, solving for $y$, then resubstituting back (assuming that we keep our convention that way)


### Derivatives of Inverse Functions
To define the derivative of an inverse function; a key property is to note that, if $f(a)=b$, then $f^{-1}(b)=a$. Considering this, then using the limit definition of the derivative: 
$$
f^{-1}(x) = \lim_{ h \to 0 } \frac{f^{-1}(x+h)-f^{-1}(x)}{h}
$$
For our case for now, let's define $x+h=c$, then we note that if $h \to 0, c\to x$
$$
f^{'-1}(x) = \lim_{ x \to c } \frac{f^{-1}(c)-f^{-1}(x)}{c-x}
$$
Consider now that if $f(b)\to c$, then $f^{-1}(c)=b$. Conversely, consider that if $f(\gamma) \to x$, then $f^{-1}(x) \to \gamma$. Consider now as well that as $x \to c$, $f^{-1}(x) \to f^{-1}(c)$, which means that $\gamma \to b$, thus: 
$$
\begin{align}
f'^{-1}(x)  & `= \lim_{ \gamma \to b } \frac{b - \gamma}{f(b) - f(\gamma)} \\
 & =\lim_{ \gamma \to b } \frac{1}{\frac{f(b)-f(\gamma)}{b-\gamma}}
\end{align}
$$