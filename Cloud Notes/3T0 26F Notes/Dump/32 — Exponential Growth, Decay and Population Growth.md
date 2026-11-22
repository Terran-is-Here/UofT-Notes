---
updated_at: 2026-11-21T22:02:57.703-05:00
edited_seconds: 520
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
> Let $t=0$ when it was the year 1950. At this point in time, the world had a population of 2560 million, and by 1960, the world had a global population of 3040. What is the relative growth rate? Can we extrapolate this value to the year 2025? 

In this case, we have the following sets of equations: 
$$
\begin{align}
P(0)  & = 2560 \\
P(10)  & = 2560*e^{k(10)} = 3040
\end{align}
$$
Solving that last equation, we have: 
$$
\begin{align}
\ln e^{10k}  & =\ln\left(  \frac{3040}{2560} \right) \\
k  & = \ln\left( \frac{3040}{2560} \right) \frac{1}{10} \approx{0}.01718
\end{align}
$$
Thus we find that: 
$$
\begin{align}
P(t) = 2560e^{0.01718t} \\
P(75) = 2560e^{0.01718*75} \approx{9289}
\end{align}
$$

### Radioactive Decay
Radioactive Decay instead finds that, for a given amount of mass undergoing radioactive decay, we have the following differential
$$
-\frac{\frac{dm}{dt}}{m} = k
$$
Or in other words: 
$$
\frac{dm}{dt} = km
$$
Where $k<0$ (as it is negative, thus indicating radioactive decay). Using the same ideas we have had earlier, we note that: 
$$
m = m_{0}e^{kt}
$$
We can apply this like the following. Consider where, after some $T_h$, our substance loses half of it's mass (something that we term as a half life. half life three?): 
$$
\begin{align}
m(T_{h}) = m_{0}e^{kT_{h}}  & = \frac{1}{2}m_{0} \\
e^{kT_{h}} & = \frac{1}{2} \\
kT_{h}  & = \ln\left( \frac{1}{2} \right) = -\ln(2) \\
k  & = -\frac{\ln(2)}{T_{h}}
\end{align}
$$
Plugging this into our expression, then: 
$$
m_{0}e^{-\ln(2)t/T_{h}} = m_{0} 2^{-t/T_{h}} = \frac{m_{0}}{2^{t/T_{h}}}
$$
Note that this indicates that for every $t_{h}$, our mass effectively halves. The expression that we derived here is applicable for a wide range of radioactive decay questions, and these should still be familiar to you. As such, the exercises are left as an exercise to the reader. 

### Temperature and Interest
The textbook introduces two more expressions here, which have been left as more examples of Exponential Decay: 

> Newton's Law of Cooling
> The rate of cooling of an object is proportional to the temperature difference between the object and it's surroundings, if the temperature difference is not too large. In terms of a differential, we find that: 
> $$\frac{dT}{dt} = k(T-T_{s})$$
> Where $T_{s}$ represents the temperature of the environment, and $T$ represents the temperature at some time $t$, that is $T(t)$. 
> $$\frac{dT}{dt} = k(T(t)-T_{s})$$
> We can let $y(t) = T(t) - T_{s}$, and thus: 
> $$\frac{dy}{dt} = ky$$
> We note that this is similar to our earlier expressions, so we know $y(t)$ is some exponential. We note that at $y(0) = T(0)-T_{s}$, thus we find that: 
> $$y(t) = (T(0)-T_{s})e^{kt}$$
> > Using a textbook example, 
> > Given that $T_{s} = 44$, $T(0)=72$, and $T(30)=61$, we find that: 

$$
\begin{align}
y(t)  & = (72-44)e^{kt} = 28e^{kt} \\
y(30) & = T(30) - 44 = 61-44 = 17 = 28e^{30t}

\end{align}
$$
