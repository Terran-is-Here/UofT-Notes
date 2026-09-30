Given Wire ABC: 
* Wire Segment AB: 
	* $d_{AB}=12mm \implies r_{ab} = 6mm$
	* $L_{0}=1200mm$
* Wire Segment BC: 
	* $d_{BC}=5mm \implies r_{bc} = 2.5mm$
	* $L_{0}=1200mm$
* Weight: 
	* $m=4kg$
	* $h=?$
* Material Properties: 
	* $E=200,000MPa$

## Energy in Segment BC: 
> We know stress is *correct*. 
> What the FUCK is strain? 


Simple approach for $\epsilon_{bc}$
$$
\begin{align}
\sigma_{bc} &= \frac{F_{A}}{\pi r_{bc}^2} \\
\epsilon_{bc} &= \frac{\Delta L}{L_{0}} & \text{Take simple approach} \\
\text{Energy}_{BC} &=\frac{\sigma_{bc}\epsilon_{bc}}{2} *V \\
&= \frac{F_{A}\Delta L}{2\pi r_{bc}^2L_{0}}*\pi r_{bc}^2*L_{0} \\
&=\frac{F_{A}\Delta L}{2}
\end{align}
$$

Try a different approach; Strain then stress? 
$$
\begin{align}
\epsilon_{bc} &= S = \frac{\Delta L}{L_{0}}\\
\sigma_{bc} &=E\epsilon_{bc}  \\
&= ES = E\frac{\Delta L}{L_{0}} \\
\text{Energy} &= \frac{\sigma_{bc}\epsilon_{bc}}{2}V_{0} \\
&= \frac{E\Delta L^2}{2L_{0}^2}L_{0}A_{0} \\
&= \frac{E\Delta L^2}{2L_{0}}A_{0}
\end{align}
$$

$$
\begin{align}
\text{Total Energy }&= \frac{E\Delta L^2}{2L_{0}}A_{0} + \frac{E\Delta L^2}{2L_{0}}A_{1} \\
mgh &= \frac{E\Delta L}{2L_{0}}\left[A_{0} + A_{1}\right] \\
h&= \frac{E\Delta L\pi}{2L_{0}mg}\left[r_{bc}^2 + r_{ab}^2\right] \\
\end{align}

$$
Invalid approach... 

Ok, try this 
$$
\begin{align}
\sigma_{BC} &= \frac{F_{A}}{A_{bc}} \\
\epsilon_{BC} &= \frac{\Delta L}{L_{0}} = \frac{\sigma_{bc}}{E} \\
&= \frac{F_{A}}{EA_{bc}} \\
\text{Total Energy} &= \frac{F_{A}^2}{2EA_{bc}^2} A_{bc}L_{0} \\
&= \frac{F_{A}^2}{2EA_{bc}}L_{0}
\end{align}
$$