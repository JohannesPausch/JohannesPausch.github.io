The finding of this project were published in _Phys. Rev. Res._ *4* 023212 (2022). 

One of the challenges has been the linking of models of neuronal populations to the actually observed times series of spikes of single neurons. The common method has been to use discrete time bins where the number of spikes within a time bin was interpreted as the number of active neurons at that time. Thus, time series of spikes are transformed into time series of avalanches/cascades. The length of the time bins has been determined heuristically and sometimes was tuned to create a branching-like process close to criticality.  In particular with a discrete time set-up the time bin size cannot be determined intrinsicially in the model.

The problems that come with imposing a time bin can be circumvented by a continuous-time model. Here a formula for the moments of interspike time can be derived:
 
 $$\mathbb{E}[T^n|N=m]=$$
 
 $\mathbb{E}[T^n]=\sum\limits_{N=0}^\infty f \mathbb{E}[T^n|N=m]$
