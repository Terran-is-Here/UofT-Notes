---
updated_at: 2026-10-19T21:13:44.736-04:00
edited_seconds: 260
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
