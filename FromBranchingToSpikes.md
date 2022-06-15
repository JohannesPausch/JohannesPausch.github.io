<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"> </script> 

The finding of this project were published in _Phys. Rev. Res._ *4* 023212 (2022). 

One of the challenges has been the linking of models of neuronal populations to the actually observed times series of spikes of single neurons. The common method has been to use discrete time bins where the number of spikes within a time bin was interpreted as the number of active neurons at that time. Thus, time series of spikes are transformed into time series of avalanches/cascades. The length of the time bins has been determined heuristically and sometimes was tuned to create a branching-like process close to criticality.  In particular with a discrete time set-up the time bin size cannot be determined intrinsicially in the model.

The problems that come with imposing a time bin can be circumvented by a continuous-time model. Here a formula for the moments of interspike time can be derived:
 
 $$\mathbb{E}[T^n|N=m]=\sum\limits_{\ell=0}^m (\ell sp_2+\gamma)\left(-\frac{d}{d\gamma}\right)^n\left(\frac{1}{\ell s+\gamma}\prod\limits_{k=\ell+1}^m \frac{ksp_0}{ks+\gamma}\right)$$
 
 where $\gamma$ is the rate of spontaneous activation of a neuron, $s$ is the rate of a neuron to activate another neuron (with probability $p_2$) or not (with probability $p_0=1-p_2$).
 
 $$\mathbb{E}[T^n]=\sum\limits_{m=1}^\infty f(m-1\uparrow m)\mathbb{E}[T_s^n|N=m]$$

where $f(m-1\uparrow m)$ is the rate with which the state of $m$ active neurons is entered from the state with $m-1$ neurons (rather than $m+1$).
