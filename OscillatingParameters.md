## Branching and Oscillations in Neuronal Avalanches

This was a project in collaboration with Rosalba Garcia-Millan and Gunnar Pruessner. Most of the results were published with open access in _Sci. Rep._ **10**:13678 (2020) under the title: time‐dependent branching processes: a model of oscillating neuronal avalanches.

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"> 
</script>
# Motivation
Avalanches in the brain exhibit two seemingly contradicting characteristics: they show time-scale invariance when the statistics of avalanche lengths or sizes are considered, hinting at critical behaviour, **but** they also show time-scale dependent oscillations as modulations of avalanches.
The article explores how both properties can coexist by considering branching processes close to criticality for which the extinction rate oscillates.

# Methods and Results
The article is based on the project on the field theory of [branching processes](Branching.md) and adjusts the used action to include oscillating parameters. In particular, the extinction rate $$\epsilon$$ was set to be

$$\epsilon(t)=s(p_0-A\sin(\nu t))$$

where $$p_0$$ is the probability to for a particle to disappear without branching at an event, $$s$$ is the overall time scale of the system $$A$$ is the amplitude of the oscillation and $$\nu$$ its frequency.

We find that the oscillations are visible at criticality in the moments, survival probability, length and size distributions, correlation functions and avalanche shape conditioned to fixed time of death. However, they do not seem to remain a feature when avalanche shapes are calculated by rescaling their length to unity. Here, oscillations seem to be averaged out and a parambola-like shape is recovered. Details can be found in the open-access paper above.
