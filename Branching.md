 ## Continuous-time branching
 
 This was a project in collaboration with Rosalba Garcia-Millan, Benjamin Walter and Gunnar Pruessner. Most of the results were published in _Phys. Rev. E_ **98**, 062107 (2018)


The core code for simulating a continuous-time branching process draws exponentially distributed event times and updates the number of particles according to a offspring distribution (a geometric distribution in the example code below) 

```C
int currentparticlenumber = 1; // number of particles in the system at time currenttime
double currenttime = 0; // event times
double maxtime = 1000; // time when the simulation is aborted

while (currenttime < maxtime){
   currenttime = currenttime + gsl_ran_exponential(r,1.0/((double) currentparticlenumber)); // new event time is generated
   currentparticlenumber = currentparticlenumber+gsl_ran_geometric(r, p0)-2; // particles are created or destroyed
   // an OBSERVABLE can be placed here
}

```
