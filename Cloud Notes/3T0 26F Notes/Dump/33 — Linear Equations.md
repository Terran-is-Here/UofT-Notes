---
updated_at: 2026-11-27T13:55:00.610-05:00
edited_seconds: 1150
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 33
Lecture Date: 2026-11-30
Week:
Created: November 22nd 2026, 11:55:55 am
---
Hub: [[ESC194 Hub]]
Previous: [[32 — Exponential Growth, Decay and Population Growth]]
Next: [[34 — Complex Numbers]]
> [!quote] Recommended Reading 
> Stewart Section 9.5 and [[31 —Differentials and Separable Equations]]

--- 
# Lecture Notes
## Linear Equations (LEC) 
A linear equation is generally any equation that can be written within this form: 

$$
y' + p(x)y = q(x)
$$
We notate this as a first order differential equation, where we required that $p(x),q(x)$ are continuous on some interval $I$. For instance, take the following expression: 
$$
xy' + y = x^{2}  \implies y' + \frac{1}{x}y = x
$$
Consider taking the derivative of $(xy)'$ then we see that $xy' + y$, then: 
$$
(xy)' = x^{2}
$$
To solve this, simply integrate both sides: 
$$
\begin{align}
xy & = \frac{x^{3}}{3} + C \\
y & = \frac{x^{2}}{3} + \frac{C}{x}
\end{align}
$$
To generalize this, we generally find an integrating factor, where this simply solves to being the derivative of the expression on the right side. 
### Integrating Factor (LEC) 
We will define the following function as the Integration Factor:
$$
H(x) = \int p(x)\,dx 
$$
Where we note that we set $C=0$ , as we simply want to find one solution / expression. Taking the derivative of the following shows us that: 
$$
\begin{align}
\frac{d}{dx} e^{H(x)} = e^{H(x)} \frac{d}{dx}H(x) = e^{H(x)}p(x)
\end{align}
$$
Then we note that: 
$$
\begin{align}
\frac{d}{dx}(ye^{H(x)})  & = y'e^{H(x)} + ye^{H(x)}p(x) \\
 & = e^{H(x)}(y' + p(x)y)
\end{align}
$$
Where $e^{h(x)}$ is our integrating factor, t hen: 
$$
\begin{align}
\frac{d}{dx}(ye^{H(x)})  & = e^{H(x)}q(x) \\
ye^{H(x)} & =\int e^{H(x)}q(x)\,dx + C
 \\
y & = \frac{1}{e^{H(x)}}\left( \int e^{H(x)}q(x)\,dx + C \right)\end{align}
$$
Where this gives us the solution for $y$. From here, we can solve for $C$ if we have some set of initial values. Take the following example: 

### Examples 
Take the following: 
$$
y' + 2y = 4
$$
Finding our integrating factor: 
$$
H(x) \int2x \,dx = 2x \implies \text{IF} = e^{2x}
$$
Then: 
$$
\begin{align}
e^{2x}y' + 2e^{2x}y & = e^{2x}4 \\
(e^{2x}y)'  & = e^{2x}4 \\
e^{2x}y & =\int e^{2x}4 \,dx + C \\
e^{2x}y  & = 2e^{2x} + C \\
y & = 2 + \frac{C}{e^{2x}}
\end{align}
$$
Consider now the following: 
### Newton's Law of Cooling (LEC)
Newton's Law of Cooling states that an object's change in temperature, is proportional to the difference between the temperature of the object, and the temperature of the surroundings.
Then: 
$$
\frac{dT}{dt} = -k(T-\tau) 
$$
Then: 

$$
\begin{align}
\frac{dT}{dt}  & = -kT + k\tau \\

\end{align}
$$

See the picture future me .

### More Examples
Consider the following Initial Value Problem: 
Solving for our factor of integration, then: 


$$
\begin{align}
y' + \frac{2}{x}y  & =  5x^{2} \\
p(x) = \frac{2}{x}, q(x) = 5x^{2} \implies \text{IF}  = e^{\ln(x^{2})} = x^{2} \\
H(x) = \int \frac{2}{x}\,dx = \ln (x^{2}) \\
x^{2}y' +2xy  & = 5x^{4} \\
x^{2}y = 5 \int x^{4}\,dx  \\
x^{2}y  & = x^{5} +C \\
y & = x^{3} + \frac{C}{x^{2}} \\
y(1) = 0 \iff C = -1
\end{align}
$$

### Logistic Equation with Active Predation
Note the Logistic Equation: 
$$
\frac{dP}{dt} = kP\left( 1-\frac{P}{M} \right)
$$
Note how this is not a linear system, as we have some function of $P^{2}$, meaning that this is inherently not a linear equation. Let us substitute that $z=\frac{1}{P}$, then: 
$$
\begin{align}
k=\frac{1}{P}  & \implies P =\frac{1}{z} \\
\frac{dP}{dt} & = -\frac{1}{z^{2}} \frac{dz}{dt} \\
\implies -\frac{1}{z^{2}} \frac{dz}{dt}  & = \frac{k}{z}\left( 1- \frac{1}{zm} \right) \\
\frac{dz}{dt} & = -kz + \frac{k}{m} \\
\frac{dz}{dt} - kz & = \frac{k}{m} &  \int k\,dt = kt \implies \text{IF} = e^{kt} \\
z & =e^{-kt}\left( \int e^{kt} \frac{K}{M}\,dt + C \right) \\
z & = \frac{1}{M}t + \frac{C}{e{kt}} = \frac{t}{M} + \frac{C}{e^{kt}} & P = \frac{1}{z} \\
 P & = \frac{1}{z} = \frac{M}{1 + MCe^{-kt}} \\
P(t=0)  & = P_{0}  \\
P  & = \frac{M}{1 + Ae^{-kt}}, A=  \frac{M-P_{0}}{P_{0}}
\end{align}
$$

---
# Pre-Lecture Notes
## Linear Equations
Recall that in our notes about [[31 —Differentials and Separable Equations|Separable Equations]], we noted that we are currently only able to solve a differential equation of the following form: 

$$
\frac{dy}{dx} = \frac{f(x)}{g(y)}
$$

However, following this section, we should be able to solve the field of *first order linear differential equations*: 

$$
\frac{dy}{dx} + P(x)y = Q(x)\tag{1}
$$

Where $P,Q$ are continuous functions on some interval $I$. For instance: 

$$
y' + \frac{1}{x}y = 2
$$

This is an example of a First Order Linear Differential Equation. Note that if we multiply both sides by $x$, we can note that from product rule: 

$$
xy' + y = 2x \implies (xy)' = 2x
$$

Then integrating, we find that: 

$$
\begin{align}
\int(xy)' \,dx  & = \int2x\,dx \\
xy & = x^{2}+C \\
y & = x + \frac{C}{x} \\
\implies y' & =1 -\frac{C}{x^{2}}
\end{align}
$$

Noting that this is a valid solution to our expression: 

$$
\begin{align}
1 - \frac{C}{x^{2}} + \frac{1}{x}\left( x+\frac{C}{x} \right)  = 1 - \frac{C}{x^{2}} + 1 + \frac{C}{x^{2}} = 2 
\end{align}
$$

as desired. 
## Generalizing
Note that how in our previous example, we multiplied both sides by some function $I(x)$ which allows us to integrate it, a function that we note as an "integration factor". Recalling $(1)$ from earlier: 

$$
\frac{dy}{dx} + P(x)y = Q(x)\tag{1}
$$

We want to multiply some function $I(x)$ such that the left side of our equation above, becomes the derivative of the product $I(x)y$, that is: 

$$
I(x)\left( \frac{dy}{dx} + P(x)y \right) =(I(x)y)' \tag{2}
$$

If such a function exists, then: 

$$
(I(x)y)' = I(x)Q(x) 
$$

Considering this, taking expression $(2)$(and substituting $\frac{dy}{dx}=y'$ notation-wise), we find that: 

$$
\begin{align}
I(x)(y' + P(x)y) & = (I(x)y)' \\
I(x)y' + I(x)P(x)y & = I(x)y' + I'(x)y \\
I(x)P(x)y & =I'(x)y \\
I(x)P(x) & = \frac{dI}{dx} \\
\end{align}
$$

Noting that this is a separable differential equation, then: 

$$
\begin{align}
P(x)\,dx & = \frac{1}{I(x)}\,dI \\
\int P(x)\,dx & = \int \frac{1}{I(x)}\,dI \\
\int P(x)\,dx & = \ln \left| I(x)\right|+C \\
e^{\int P(x)\,dx} & = I(x) e^{C} & A=\pm e^{C} \\
I (x) & =Ae^{\int P(x)\,dx}  & A=1 \text{ to simplify} \\
I(x) & =e^{\int P(x)\,dx}

\end{align}
$$

Thus, with our expression in this form, we note now that to simply solve a linear differential equation of the first order, we simply multiply by this function on both sides then integrate. 
> [!theorem] Solving First Order Linear Differential Equations 
> Given a linear differential of the first order: 
>
> $$y' + P(x)y = Q(x)$$
>
> This can be solved by multiplying both sides by the integration factor of $I(x) = e^{\int P(x)\,dx}$, then integrating the expression from there.
>
> $$e^{\int P(x)\,dx}(y' + P(x)y)=  e^{\int P(x)\,dx}Q(x)$$
>
> As: 
>
> $$\begin{align}e^{\int P(x)\,dx}y' + e^{\int P(x)\,dx}P(x)y  & = e^{\int P(x)\,dx}Q(x) \\\frac{d}{dx}\left( e^{\int P(x) \, dx}y \right)  & = e^{\int P(x)\,dx}Q(x)\end{align}$$
>
> And then from here, you can solve for $y$ by solving for the integral as per usual. 

### Example(s)
Consider the following differential: 
$$
\frac{dy}{dx} + 3x^{2}y = 6x^{2}
$$
Noting that $P(x)=3x^{2}$, then we can find our integration factor: 
$$
\begin{align}
I(x) & =e^{\int 3x^{2}\,dx}= e^{x^{3}}
\end{align}
$$
> (Note that we don't have a $e^{C}$ term present **for the integration factor**, as from our earlier algebra, this expression is actually $I(x)=\frac{e^{\int P(x)\,dx}}{e^{C}}$, taking the corresponding antiderivative and adding the $+C$ term at the end cancels out.) 

Plugging this into our expression, then: 
$$
\begin{align}
e^{x^{3}}\left( y'+3x^{2}y \right)  & = e^{x^{3}}6x^{2} \\
e^{x^{3}}y' + e^{x^{3}}3x^{2}y & = e^{x^{3}}6x^{2} \\
\frac{d}{dx}(e^{x^{3}}y)  & =e^{x^{3}}6x^{2} \\
\int \frac{d}{dx}( e^{x^{3}}y)\,dx & =\int e^{x^{3}}6x^{2}\,dx \\
e^{x^{3}}y & =2e^{x^{3}} + C \\
y  & = 2 + \frac{C}{e^{x^{3}}}
\end{align}
$$

Consider now the following IVP: 
$$
x^{2}y' + xy = 1, x>0, y(1)=2
$$
Noting that we want to get to some $y' +P(x)y = Q(x)$, we divide by $x^{2}$ on both sides: 
$$
\begin{align}
\frac{1}{x^{2}}(x^{2}y' + xy) & = \frac{1}{x^{2}} \\
y' + \frac{1}{x}y & = \frac{1}{x^{2}}
\end{align}
$$
Finding our integration factor: 
$$
I(x) = e^{\int 1/x\,dx} = e^{\ln(x)} = x
$$
Multiplying on both sides, then: 
$$
\begin{align}
xy' + y  & = \frac{1}{x} \\
(xy)'  & = \frac{1}{x} \\
\int(xy)'\,dx & = \int \frac{1}{x}\,dx \\
xy & = \ln|x|+C \\
y  & = \frac{\ln|x|+C}{x}
\end{align}
$$
Noting that from our initial value, that $y(1)=2$, thus: 
$$
\begin{align}
y(1)=2=\frac{\ln|1|+C}{1} \implies C=2
\end{align}

$$
Thus our solution becomes: 
$$
y = \frac{\ln|x|+2}{x}
$$
