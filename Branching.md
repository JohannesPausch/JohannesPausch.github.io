## Continuous-time Branching
This was a project in collaboration with Rosalba Garcia-Millan, Benjamin Walter and Gunnar Pruessner. Most of the results were published in _Phys. Rev. E_ **98**, 062107 (2018)

# Motivation
Branching processes are stochastic processes, in which a particle (or individual or item ..) can create copies of itself which follow the same process. How many and when these copies are created is random. Furthermore, particles can also disappear in an extinction process. Interesting questions are then: If the system starts with one particle, how many will we find later on? Will the system be empty at some point? If so, how long will that take? Is is possible that the system becomes empty? 

# Methods and Results 
Using Doi-Peliti field theory, we characterized analytically the behaviour of a large class of branching processes close to criticality. The central object from which all properties of the process are derived is the action
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"> 
</script>

$$ \mathcal{A}=\int \widetilde\phi(t)(-\partial_t-r)\phi(t)+\sum\limits_{j\ge2}q_j\widetilde\phi^j(t)\phi(t) dt $$

The core code for simulating a continuous-time branching process draws exponentially distributed event times and updates the number of particles according to a offspring distribution (a geometric distribution in the example code below) 

```C
// number of particles in the system at time currenttime
int currentparticlenumber = 1;
// event times
double currenttime = 0;
// time when the simulation is aborted
double maxtime = 1000; 

while (currenttime < maxtime){
   // a new random event time is generated
   currenttime += gsl_ran_exponential(r,1.0/((double) currentparticlenumber));
   // particles are randomly created or destroyed
   currentparticlenumber += gsl_ran_geometric(r, p0)-2; 
   // an OBSERVABLE can be placed here
}

```
