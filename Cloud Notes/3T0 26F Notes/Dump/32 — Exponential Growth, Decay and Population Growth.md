---
updated_at: 2026-11-21T21:43:16.228-05:00
edited_seconds: 270
course:
tags:
  - esc
"Lecture #": 0
Lecture Date: 2026-11-21
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[31 —Differentials and Separable Equations]]
Next:
> [!quote] Recommended Reading 
> Sections 6.5 and 9.4 of the Stewart Textbook
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Exponential Growth & Decay
Recall that in the previous note, we stated that for differential equations of the following form: 
$$
\frac{dy}{dx} = ky
$$
The only solution to this expression is if $y=C_{0}e^{kt}$, Where $C_{0}=y(0)$, or in other words, the initial value of our expression: 
$$
\frac{dy}{dx} = ky \iff y (t) = y(0)e^{kt}
$$
Recall that in this context, the sign of $k$ dictates in which direction our expression is growing, a $k<0$ implies that our function is shrinking, whilst $k>0$ implies that our function's value is growing.
### Population Growth
Note how if we assume that population growth is fully exponential (that is, not logistic): 
$$
\frac{dP}{dt} = kP
$$
Then we note that: 
$$
\frac{\frac{dP}{dt}}{P} = k
$$
The value $k$ corresponds to the relative growth factor of such a given expression. That is; how much does it relatively scale on itself per value of $x$? Note that given two values of $P(t)$, we can solve for the value $k$ as per usual. 

> Textbook Example (Paraphrased)
> Let $t=0$ when it was the year 1950. At this point in time, the world had a population of 2560 million, and by 1960, the world had a global population of 3060. What is the relative growth rate? Can we extrapolate this value to the year 2025? 

In this case, we have the following sets of equations: 
$$
\begin{align}
P(0)  & = 2560 \\
P(10)  & = 2560*e^{k(10)} = 3060
\end{align}
$$
Solving that last equation, we have: 
$$
\begin{align}
\ln e^{10k}  & =\ln\left(  \frac{3060}{2560} \right) \\
k  & = \ln\left( \frac{3060}{2560} \right) \frac{1}{10} \approx{0}.01784
\end{align}
$$
Thus we find that: 
$$
\begin{align}
P(t) = 2560e^{0.01784t} \\
P(75) = 2560e^{0.01784*75} \approx{9757}
\end{align}
$$
