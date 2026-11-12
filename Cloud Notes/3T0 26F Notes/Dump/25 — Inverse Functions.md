---
updated_at: 2026-11-12T14:55:10.989-05:00
edited_seconds: 960
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 25
Lecture Date: 2026-11-12
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[24 — Volumes by Cylindrical Shells and Average Function Values]]
Next: [[26 — The Natural Logarithmic Function]]
> [!quote] Recommended Reading 
> Stewart Textbook Section 6.1 
--- 
# Lecture Notes
## Inverse Functions (LEC) 
Before we define an Inverse Function, we need to show that a function is bijective ("one-to-one")
> A function $f(x)$ is said to be bijective if $f(x_{1})=f(x_{2}) \implies x_{1}=x_{2}$. Or in other words, $f(x_{1})\neq f(x_{2}) \implies x_{1}\neq x_{2}$

This can be done graphically by the application of a horizontal line test; that is simply slicing some line $y=a$ , and showing that for some $f(x)=y$, there exists solely one value of $x$ that satisfies this possibility. 

From this, we can define the concept of an *inverse function* as the following. 
> Let $f$ be a one-to-one / bijective function with a domain $A$ and a range $B$; thus $A\mapsto B$ for $f$. 
> Then it's *inverse function* $f^{-1}$ has a domain of $B$ with a range of $A$, that is $B\mapsto A$, and is defined as $f^{-1}(y) = x \iff f(x) =y$. 

Thus, we find that: 
$$
\begin{align}
f^{-1}(f(x)) = x \\
f(f^{-1}(x)) = x
\end{align}
$$
Note that for notation wise, we will notate this as attaching this directly onto the term (which should be obvious). 

To find an inverse, first swap the $y=f^{-1}(x)$; such that is $f(y)=x$. In other words, swap $y=x$ then return values at the end. 
* $f(x)=x^{3} \implies f^{-1}(x) = x^{1/3}$
* $f(x)=\sqrt{ x } \implies \forall x\in[0,\infty), f^{-1}(x) = x^{2}$

Graphically, since $f(a)=b \implies (a,b) \lor(a,f(a)$. Note that $f'(b)=a$ by definition, thus representing the ordered pair $(b,a)$. In other words, we change the values of our points across the line $y=x$. 
### Example
Consider the following function: 
$g(x) = \sqrt{ 2x+1 }$, where $x\geq -\frac{1}{2}$. 

Consider showing bijectivity, then: 
$$
\begin{align}
g(x_{1}) &  = g(x_{2}) \\
\sqrt{ 2x_{1} +1}  & = \sqrt{ 2x_{2} }+1 \\
\implies x_{1} & =x_{2}
\end{align}
$$
Thus an inverse exists, thus: 
$$
y=g^{-1}(x)
$$
 Thus: 
$$
 \begin{align}
 g(y)=\sqrt{ 2y+1 } = x \\
 y=\frac{x^{2}-1}{2}=g^{-1}(x)
 \end{align}
$$
Note that this applies $\forall x\geq0$. 
### Increasing and Decreasing Functions
Bijectivity actually follows partially from the following theorem: 
> If a function $f$ is an *increasing* or *decreasing* function, then $f$ is bijective, and thus has an inverse. 

This is proven by the following. 

> Let $f(x)$ be an increasing function, then $x_{1}<x_{2} \implies f(x_{1})<f(x_{2})$. 
> From Trichotomy [[02 — The Real Number System]], then this implies that $x_{1}\neq x_{2} \implies f(x_{1})\neq f(x_{2})$, which is 

Note that to prove this, we simply take the derivative and show that a function's first derivative is always positive (or negative) across an interval. 

Take the following example: 
$$
f(x) = x^{3} \implies \frac{df}{dx} = 3x^{2} \implies \frac{d^{2}f}{dx^{2} } = 6x
$$
Note that this function has *a* location where $f'=0$. Recall that increasing or decreasing means the implication that the order of the points corresponds to the order of the function *evaluated* at those points. 

Take the following example: 
$$
f(x) = 5x^{7}+3x^{3} - 7 \implies \frac{df}{dx} = 35x^{6} + 9x^{2}
$$
Thus, $\forall x\in(-\infty,\infty), \frac{df}{dx}\geq0$, thus an inverse exists, simply setting $y=f^{-1}(x)$, $f(y)=x$ and solve as per usual. Note that solving for the inverse functions may be difficult. 

## Inverse Function Derivatives (LEC) 

> [!theorem] 
> Let $f$ be a bijective function defined on an interval $I$. If $f$ is continuous on $I$, then $f^{-1}$ is also continuous. 
> > Proof available in Page A47 of the Stewart Textbook

For the purposes of this section, let $g(x)= f^{-1}(x)$, thus $f(g(x)) = x$. Consider differentiating both sides, thus: 

$$
\begin{align}
\frac{d}{dx}(f(g(x))) & =\frac{d}{dx}x \\
f'(g(x))g'(x)  & =1 & f'(g(x)) \neq 0 \\
g'(x)  & =\frac{1}{f'(g(x))} 
\end{align}
$$
Or, in alternative notations: 
$$
\begin{align}
\frac{dy}{dx} = \frac{1}{\frac{dx}{dy}} \\
f'^{-1}(x) = \frac{1}{f'(f^{-1}(x))}
\end{align}
$$

Consider that graphically, taking the derivative is equivalent to us taking some $\frac{\Delta y}{\Delta x}$. If our functions are equivalently flipped across some mirror $y=x$, then it follows that $f'(x)=\frac{\Delta x}{\Delta y}$ as per the slope, or in other words, the inverse of the slope. 


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
f^{'-1}(x) = \lim_{ c \to x } \frac{f^{-1}(c)-f^{-1}(x)}{c-x}
$$
Consider now that if $f(b)\to c$, then $f^{-1}(c)=b$. Conversely, consider that if $f(\gamma) \to x$, then $f^{-1}(x) \to \gamma$. Consider now as well that as $c \to x$, $f^{-1}(c) \to f^{-1}(x)$, which means that $b \to \gamma$, thus: 
$$
\begin{align}
f'^{-1}(x)  & = \lim_{ \gamma \to b } \frac{b - \gamma}{f(b) - f(\gamma)} \\
 & =\lim_{ \gamma \to b } \frac{1}{\frac{f(b)-f(\gamma)}{b-\gamma}} & 
\end{align}
$$
Note that the term in the denominator is equivalent to $f'(b)$, which means that: 
$$
\begin{align}
f'^{-1}(x) = \frac{1}{f'(b) }
\end{align}
$$
Recall that if $b = f^{-1}(c) = b$, and if $c \to x$, then this becomes:
$$
f'^{-1}(x) = \frac{1}{f'(f^{-1}(x))}
$$

> Note that this could also be derived from the chain rule. If we know that some function $f(y) = x$ is differentiable, and that $f^{-1}(x)=y$ exists, then we note that: 
> $$\begin{align}f'(y) \frac{dy}{dx}  & = 1 & \text{from } f(y) = x \\f'(y) & =\frac{1}{\frac{dx}{dy}} & \frac{dx}{dy}= f'(f^{-1}(x)) \\& =\frac{1}{f'(f^{-1}(x))}\end{align}$$
> Note that we resubstituted back in our term above, as we note that $\frac{dx}{dy}=f'(y)$, and $y$ can be rewritten as some function of $x$ from our inverse function expression from above.

