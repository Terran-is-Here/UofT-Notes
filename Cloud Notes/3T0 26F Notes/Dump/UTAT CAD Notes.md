---
updated_at: 2026-09-26T16:15:24.379-04:00
edited_seconds: 500
course: N/A
tags:
  - Other
"Lecture #": 0
Lecture Date: 2026-09-18
Week:
created:
Created: September 18th 2026, 6:33:54 pm
---
Hub: [[Other Notes Hub]]
Related: [[CIV102 Hub]]

--- 

### Stress
The following are useful stress calculations for UTAT's pressure Vessel Design: 
$$
\begin{align}
\sigma_{\theta} &= \frac{pa}{t} & \text{Hoop Stress (stress around the tank, vertical failure) } \\ \\
\sigma_{ax} = \frac{\sigma_{t}}{2} &= \frac{pa}{2t} & \text{Axial Stress (horizontal failure)} \\
\end{align}
$$
Where: 
* $p$ is pressure; 
* $a$ is the radius of our tank; 
* $t$ is the thickness of our material. 

Note that these are only really effective for *cylindrical* pressure vessels. 

Recall from CIV120, if $\mu_{u} > \sigma_{\theta}$ (Note that this is in terms of the *ultimate strength*. This is the *failure* point of the material. $\mu_{y}$ or $\sigma_{y}$ simply gives us the point at which our material starts to plastically deform.  
### Failure Theory (EBK) 
Failure Theory allows us to compare multiple sources of stress (from FEA) into one value (in this case, $\sigma_{\theta}$ and $\sigma_{ax}$): 
$$
\sigma_{v} = \sqrt{ \sigma_{1}^2 + \sigma^2_{2} - \sigma_{1}\sigma_{2} }
$$
Where this is then the value that we compare between $\mu_{u}$ (ultimate tensile stress). Note that in this case, we can define $\sigma_{1} = \sigma_{\theta}$, and $\sigma_{2} = \sigma_{ax}$. 

### Example 
$$
\begin{align}
p = 1000\text{psi} \\
a = 3\text{in} \\
h = 0.125
\end{align}
$$
With a factor of safety of $2.5$. Solve for if it is valid: 

$$
\begin{align}
\sigma_{\theta} = \frac{pa}{t} = \frac{2500*3}{0.125} &= 60000 \\
\sigma_{2x} = \frac{\sigma_{\theta}}{2} &= 30000
\end{align}

$$
Then: 
$$
\begin{align}
\sigma_{v} = \sqrt{ 60000^2 + 30000^2 - 60000*30000 } &\approx 52000\text{psi} & \text{Note, }\sigma_{u} = 45000\text{psi} \\
\sigma_{v} &>\sigma_{u} & \therefore \text{Material fails at 45000 psi.}
\end{align}
$$
Note that at our desired operating regimens; then: 
$$
\begin{align}
\sigma_{\theta} = \frac{pa}{t} = \frac{1000*3}{0.125} &= 24000 \\
\sigma_{2x} = \frac{\sigma_{\theta}}{2} &= 12000
\end{align}
$$
$$
\begin{align}
\sigma_{v} = \sqrt{ 24000^2 + 24000^2 - 24000*12000 } &\approx 20800 \text{psi} & \text{Note, }\sigma_{u} = 45000\text{psi} \\
\sigma_{v} &<\sigma_{u} & \therefore \text{Material does not fail at operating pressure.}
\end{align}
$$
