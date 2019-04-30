 ## Continuous-time branching
This was a project in collaboration with Rosalba Garcia-Millan, Benjamin Walter and Gunnar Pruessner. Most of the results were published in _Phys. Rev. E_ **98**, 062107 (2018)


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
