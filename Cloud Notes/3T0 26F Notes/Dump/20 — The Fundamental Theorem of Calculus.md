---
updated_at: 2026-10-19T21:32:08.700-04:00
edited_seconds: 350
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Lecture Date: 2026-10-19
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[19 — The Definite Integral]]
Next: N/A 
> [!quote] Recommended Reading 
> Section 4.3 (Stewart) 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Fundamental Theorem of Calculus
The Fundamental Theorem of Calculus is, well, the fundamental theorem of Calculus. It lets us link together the concepts of differentiation and integration together in order. Note that the textbook goes in two parts in trying to solve and express the FToC, and we will follow the same logic here. 

### FToC: Special Case
The first segment of the Fundamental Theorem of Calculus deals with functions with the following form: 
$$
g(x)=\int_{a}^{x}f(x)~dx
$$
Where $f$ is a continuous function $[a,b]$, where $x$ varies between $a,b$. Note that $g(x)$ only depends on $x$, and is equivalent to the area under the function $f(x)$ from some point $a$ to $x$ (Note that if $f(x)>0 ~\forall x$ in it's domain, we can directly consider this to be the sum of the areas under the function. 

Consider now the following expression: 
$$
g(x+h) - g(x)
$$
This is equivalently telling us the difference in area between our function from $x,x+h$. Note that if $h$ is small, this approximates the small slice of area under our function $f(x)$, with a width of $h$, that is: 
$$
\begin{align}
g(x+h)-g(x)  & \approx hf(x) \\
\frac{g(x+h)-g(x)}{h} & \approx f(x)
\end{align}
$$
Thus, if we take the limit, this intuitively shows us that: 
$$
g'(x) = \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h} =f(x)
$$
Or in other words, the derivative of an integral function of the form above gives us back the original function inside. 

We can formally prove this with the Discrete Integral laws that we learned in the previous note: 
$$
\begin{align}
g(x+h)-g(x)  & =\int _{a}^{x+h} f(x)\, dx  - \int _{a}^{x} f(x)\, dx  \\
 & =\int _{a}^{x}f(x) \, dx +\int _{x}^{x+h} f(x)\, dx   - \int _{a}^xf(x) \, dx \\
&=\int _{x}^{x+h}f(x) \, dx 
\end{align}
$$
Note that for some $h\neq0$ then we can insert the following: 
$$
\frac{g(x+h)-g(x)}{h} = \frac{1}{h}\int_{x}^{x+h}f(x)~dx
$$
Note that since $f(x)$ is continuous on an interval $[a,b]$, we know that since the values we are testing are inside that interval, it must thus also be continuous within some closed interval $[x,x+h]$, thus following EVT, $\exists c_{1},c_{2}\in[x,x+h]$ where $f(c_{1})=m$ and $f(c_{2})=M$, that is, the absolute maxima and minima of the function. 

Note then that: 
$$
\begin{align}
m(x+h-x)  & \leq g(x+h)-g(x) \leq M(x+h-x) \\
mh & \leq g(x+h)-g(x) \leq Mh \\
f(c_{1})h  & \leq \int _{x}^{x+h}f(x) \, dx \leq f(c_{2})h  \\
f(c_{1}) & \leq \frac{1}{h}\int _{x}^{x+h}f(x) \, dx  \leq f(c_{2})  \\
f(c_{1}) & \leq \frac{g(x+h)-g(x)}{h} \leq f(c_{2})
\end{align}
$$
Note that with $\lim_{ h \to 0 }$, $c_{1} \to x$, $c_{2} \to x$ as $[x,x+h]$ with $h\to0\implies [x,x+h] \to[x,x]$; then: 
$$
f(x) \leq \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h}= g'(x) \leq f(x)
$$
Thus from the Squeeze Theorem, then:

$$
g'(x) = \lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h} = f(x)
$$
Thus we arrive at the formal definition for the first half of the Fundamental Theorem of Calculus: 

> [!theorem] Fundamental Theorem of Calculus (Part 1)
> If $f$ is continuous on $[a,b]$, then the function $g(x)$ defined by the following: 
> $$g(x) = \int _{a}^{x}f(t) \, dt, ~~~ a\leq x\leq b $$
> Here, $g(x)$ is continuous on $[a,b]$, and is differentiable on the corresponding open interval, where $g'(x)=f(x)$. 

### FToC: Calculation
