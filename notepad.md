$$
\begin{align}
y & =\sin ^{-1}(x) \\
\sin(y) & =x \\
\frac{d}{dx}\sin(y)  & = \frac{d}{dx}x \to \cos(y) \frac{dy}{dx}=1 \\
\frac{dy}{dx} & =\frac{1}{\cos(y)}  & \text{note}: \cos(y) &  = \sqrt{ 1-\sin ^{2}(y) } \\
\frac{dy}{dx} & = \frac{1}{\sqrt{ 1-\sin^2 (y)}} & \text{note:} \sin(y)  & = x \\
\frac{dy}{dx} & = \frac{1}{\sqrt{ 1-x^{2} }}
\end{align}
$$
So basically..
$$
\begin{align}
y  & = f^{-1}(x)  \\
f(y) & =x \\
 \\
\frac{d}{dx}f(y) &  = \frac{d}{dx} x \\
f'(y) \frac{dy}{dx} & = 1 \\
\frac{dy}{dx} & = \frac{1}{f'(y)} & \text{let } f'(y) \to f'(f^{-1}(x)) &  & \text{let }  \frac{dy}{dx} = y' = [f^{-1}(x)]' \\
[f^{-1}(x)]' & = \frac{1}{f'(f^{-1}(x))}
\end{align}

$$

---

$$
\begin{align}
y  & = \tan ^{-1}(x)  \\
\tan(y)  & = x \\
 \\
\frac{d}{dx}\tan(y) &  =\frac{d}{dx}x \\
\sec ^{2}(y) \frac{dy}{dx} & = 1  \\
\frac{dy}{dx} & =  \frac{1}{\sec ^{2}(y)}  & \sec ^{2}(y) = 1 + \tan ^{2}(y) \text{ as } \frac{1}{\cos ^{2}(y)} = \frac{\cos ^{2}(y)+\sin ^{2}(y)}{\cos ^{2}(y)} \\
\frac{dy}{dx} & = \frac{1}{1+\tan ^{2}(y)} = \frac{1}{1+x^{2}}
\end{align}
$$

---
$$
\begin{align}
y & =\ln(x) \\
e^{y}  & = x \\
 \\
\frac{d}{dx}e^{y} & = \frac{d}{dx}x \\
[e^{y}]'  \frac{dy}{dx} & = 1 \\
\frac{dy}{dx} & = \frac{1}{[e^{y}]'} & e^{y} = e^{\ln(x)} \\
\frac{dy}{dx} & = \frac{1}{[e^{\ln(x)}]'}
\end{align}
$$