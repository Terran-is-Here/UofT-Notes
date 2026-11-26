---
updated_at: 2026-11-26T14:54:50.444-05:00
edited_seconds: 1270
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 32
Lecture Date: 2026-11-27
Week: 11
---
Hub: [[ESC194 Hub]]
Previous: [[31 —Differentials and Separable Equations]]
Next: [[33 — Linear Equations]]
> [!quote] Recommended Reading 
> Sections 6.5 and 9.4 of the Stewart Textbook
--- 
# Lecture Notes
## Exponential Growth
Consider the following: 
$$
\frac{df}{dt} = kf(t)
$$
Where the rate of change of a function, is equivalent to the value of the function multiplied by some factor of time: 
$$
\frac{1}{f} \frac{df}{dt} = k \implies k = \frac{d}{dt}\ln(f) \implies kt + C^{*} = \ln f
$$
Then: 

$$
f = e^{kt+C^{*}} = e^{C^{*}}e^{kt} = Ce^{kt}
$$
Where we let $C = e^{C^{*}}$. 

Note that: 
* $f(0) = C$, that is $C$ is equivalent to our initial value. 
* $k$ represents the growth constant of our expression.
For instance, take the following this example: 
### Examples
> Assume that in 1900, there were 1000 rabbits in Australia. Given a population growth rate of $1.3$, then: 

$$
\frac{dP}{dt} = 1.3P
$$
How many rabbits are there today? 
$$
P = 1000 * e^{1.3*126} = 1.37\times 10^{74} \text{ rabbits}
$$
### Doubling Time
Note that another way we can express a population growth function is in terms of the time to double: 
$$
\begin{align}
2P_{0}  & = P_{0}e^{kt_{2}} \\
2 & = e^{kt_{2}} \\
\ln(2) & = kt_{2} \\
\frac{\ln(2)}{k}= t_{2}
\end{align}
$$
For instance, consider that $k=0.011$ Thus: 
$$
\frac{\ln(2)}{0.011} = t_{2} = 63\text{ years to double population}
$$
### Radioactive Decay
Additionally, we also have: 

$$
\frac{dN}{dt} = -kP
$$
Where this is always decreasing, integrating gives us: 
$$
N(t) = N(0)e^{-kt}
$$
For a Half Life: 
$$
\begin{align}
\frac{1}{2}N(0)  & = N(0) e^{-kt_{h}} \\
t_{2} & = \frac{\ln(2)}{k}
\end{align}
$$
#### Example
Consider that you had some material mass $m$ starting out at 10 years ago. Let $t=0$, and: 
$$
\begin{align}
4 = N_{0}e^{-k_{9}} \\
3 = N_{0}e^{-k_{10}}
\end{align}
$$
Then: 
$$
\frac{4}{3}=e^{-k(9-10)} = e^{k} \implies k =\ln\left( \frac{4}{3} \right) \approx 0.288
$$
Then: 
$$
\begin{align}
4 = N_{0}e^{k9} \implies N_{0} = 53.3
\end{align}
$$
Then, solving for the half life: 
$$
t_{h} = \frac{\ln(2)}{0.288} = 2.4\text{ years}
$$
### Compound Interest
Consider the concept of compound interest. Note that for Annual interest: 
$$
V(t) = V(0)(1+i)^{t}
$$
Where this represents the final value after a set of time, $V(0)$ represents the initial value, and $i$ represents the interest rate. For a semi-annual system, then: 

$$
V(t) = V(0) \left( 1 +\frac{i}{2} \right)^{2t}
$$
Generalizing this for any amount of times that we collect interest: 
$$
V(t) = V(0)\left( 1 + \frac{i}{n} \right)^{nt}
$$
Rewriting $V(0)=P$, then: 
$$
\begin{align}
V(t) = P\left( 1+\frac{i}{n} \right)^{nt}
\end{align}
$$
Consider what happens when we take continuous interest, that is we take the limit of $n\to \infty$, then:
$$
\begin{align}
V(t) &  = \lim_{ n \to \infty } P\left( 1 + \frac{i}{n} \right)^{nt}  & b=\frac{n}{i} \implies n=bi \\
 & = P\lim_{ b \to \infty } \left( \left( 1+\frac{1}{b} \right)^{b} \right)^{it}  \\
 & =P\left( \lim_{ b \to \infty } \left( 1+\frac{1}{n} \right)^{b} \right)^{it} & \lim_{ n \to \infty } \left( 1+\frac{1}{n} \right)^{n} = e \\
 & =Pe^{it}
\end{align}
$$
Applying this: 
$$
V(400) = 0.01e^{0.05*400} \approx 5\text{ million}
$$




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

> [!ila]- Newton's Law of Cooling
> The rate of cooling of an object is proportional to the temperature difference between the object and it's surroundings, if the temperature difference is not too large. In terms of a differential, we find that: 
> $$\frac{dT}{dt} = k(T-T_{s})$$
> Where $T_{s}$ represents the temperature of the environment, and $T$ represents the temperature at some time $t$, that is $T(t)$. 
> $$\frac{dT}{dt} = k(T(t)-T_{s})$$
> We can let $y(t) = T(t) - T_{s}$, and thus: 
> $$\frac{dy}{dt} = ky$$
> We note that this is similar to our earlier expressions, so we know $y(t)$ is some exponential. We note that at $y(0) = T(0)-T_{s}$, thus we find that: 
> $$y(t) = (T(0)-T_{s})e^{kt} = T(t) - T_{s}$$
> > Using a textbook example, 
> > Given that $T_{s} = 44$, $T(0)=72$, and $T(30)=61$, we find that: 
> > $$\begin{align}y(t)  & = (72-44)e^{kt} = 28e^{kt} \\y(30) & = T(30) - 44 = 61-44 = 17 = 28e^{30k} \\\frac{1}{30} \ln\left( \frac{17}{28} \right)  & =k \\k  & \approx -0.016633\end{align}$$
> > Thus our expression becomes: 
> > $$y(t) =28e^{-0.016633t}$$
> > Recalling that we defined $y(t) = T(t)-T_{s}$, then $T(t) = 44 + 28e^{-0.016633t}$. Noting that $t\to \infty$, $T(t) \to T_{s}$, which is to be expected. 

> [!ila]- Continuous Compounding Interest
> Recall the definition of compounding interest back in your old mathematics classes: 
> $$A_{t} = A_{0}\left( 1 + \frac{r}{n} \right)^{nt}$$
> Where $n$ corresponds to the amount of times interest accrues per year $t$, where the overall interest is defined as $\frac{r}{n}$. Consider the case in which we continuously take more and more terms of interest, then we find that: 
> $$\begin{align}A(t)  & = \lim_{ n \to \infty } A_{0}\left( 1+\frac{r}{n} \right)^{nt}  \\& =A_{0} \lim_{ n \to \infty } \left( 1+\frac{r}{n} \right)^{nt} & b = \frac{n}{r} , n\to \infty, b\to \infty, n = br \\& =A_{0}\lim_{ b \to \infty } \left( 1+\frac{1}{b} \right)^{brt} \\& =A_{0} \lim_{ b \to \infty } \left( \left( 1+\frac{1}{b} \right)^{b} \right)^{rt}  \\& =A_{0} \left( \lim_{ b \to \infty } \left( 1+\frac{1}{b} \right)^{b} \right)^{rt} & \lim_{ n \to \infty } \left( 1+\frac{1}{n} \right)^{n} = e \\& =A_{0}e^{rt}\end{align}$$
> Note that $\frac{dA}{dt} = rA_{0}e^{rt} = rA(t)$. 


## Population Growth (continued)
Continued from the previous section of this note, we note the following differential equations pertaining to various population models: 
$$
\begin{align}
\frac{dP}{dt} & = kP & \text{law of natural growth} \\
\frac{dP}{dt}  & = kP\left( 1-\frac{P}{M} \right) & \text{logistic differential} \\
\frac{dP}{dt} & =kP\left( 1-\frac{P}{M} \right)-c & \text{logistic differential with harvesting} \\
\frac{dP}{dt}  & = kP\left( 1-\frac{P}{M} \right)\left( 1-\frac{m}{P} \right) & \text{logistic differential with MVP}
\end{align}
$$
Noting that: 
* For the law of natural growth, the solution of $P(t) = P_{0}e^{kt}$ is valid. 
* For logistic growth with harvesting, we note that $c$ would be equivalent to some constant term of harvesting present. 
* For logistic growth with respects to a minimum viable population, we note that if $P<m$, $\frac{m}{P}>1$, thus our corresponding population will shrink. 

For the purposes of this section, we will consider analysing the Logistic Growth Formula: 
$$
\frac{dP}{dt} = kP\left( 1-\frac{P}{M} \right)
$$
Noting that the term on the right, $P\left( 1-\frac{P}{M} \right)$ is purely some function of $P$, then we note that this is a Separable equation, thus: 
$$
\begin{align}
\frac{1}{P\left( 1-\frac{P}{M} \right)}dP  & = k\,dt \\
\int \frac{1}{P\left( 1-\frac{P}{M} \right)}\,dP & = \int k \,dt \\
\int \frac{M}{P(M-P)} \,dP = \int \frac{1}{P}-\frac{1}{M-P}dP = \ln|P| - \ln|M-P|  & = kt +C  \\
\ln(M-P)-\ln(P)  & = -kt-C \\
\ln \left| \frac{P}{M-P} \right| & = -kt-C \\
\left| \frac{M-P}{P}\right|  & =e^{-kt-C}= e^{-kt}e^{-C} & e^{-C}=A\\
\frac{M-P}{P}  & = e^{-kt}A\end{align}
$$
If we set $t=0$, we find that $A=\frac{M-P_{0}}{P_{0}}$, where $P(0) = P_{0}$, or in other words, the starting population. Solving for P, we then get: 
$$
\begin{align}
M-P(t) & = e^{-kt}AP(t) \\
M & = Ae^{-kt}P(t) + P(t) = (Ae^{-kt}+1)P(t) \\
\frac{M}{1 + Ae^{-kt}}  & =P(t)
\end{align}
$$
Plugging in $A$, we then find the logistic population expression: 
$$
\frac{M}{1 + \frac{M-P_{0}}{P_{0}}e^{-kt}} = P(t)
$$
Note that normally we simply keep $A$ as $\frac{M-P_{0}}{P_{0}}$ just to make our expressions easier to work with. 



