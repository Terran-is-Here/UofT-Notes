Prove the following: 
$$
\lim_{ x \to c } f(x) + g(x) = L + M
$$
From $\epsilon-\delta$: 
$$
\begin{align}
\forall\epsilon>0, \exists\delta>0 \text{ s.t } \\
|x-c| < \delta \implies |f(x) + g(x) &  - L - M| < \epsilon
\end{align}
$$
Analyzing these individually: 
$$
\begin{align}
|x-c| < \delta_{1} \implies |f(x) - L | <\epsilon \\
|x-c| < \delta_{2}\implies |g(x) - M | <\epsilon 
\end{align}
$$
Note that $|f(x)+g(x) -L-M| = |(f(x) - L) + (g(x)-M)| \leq |f(x)-L| + |g(x)-M|$ (from triangle inequality) 

Then: 
$$
|f(x)+g(x) - L - M| \leq |f(x)-L| + |g(x)-M| < \epsilon
$$
Note if $|f(x)-L| < \epsilon, |g(x)-M| <\epsilon \implies |f(x)-L| + |g(x)-M| <2 \epsilon$; meaning that for each case here, set $|f(x)-L| <\frac{\epsilon}{2}, |g(x)-M| < \frac{\epsilon}{2}$; thus giving our result as desired; where $\delta=\text{min}\{ \delta_{1},\delta_{2} \}$. 

Then: 
$$
\begin{align}
\forall\epsilon>0, \exists\delta>0.\ \delta = \min\{ \delta_{1},\delta_{2} \}; \\
|x-c| < \delta_{1} \implies |f(x_{x})-L | < \frac{\epsilon}{2} \\
|x-c| < \delta_{2} \implies |g(x) - M| < \frac{\epsilon}{2} \\
\implies |x-c| < \delta \implies |f(x) - L| 
\end{align}
$$