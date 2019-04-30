 ## Continuous-time branching
 
 This was a project in collaboration with Rosalba Garcia-Millan, Benjamin Walter and Gunnar Pruessner. Most of the results were published in _Phys. Rev. E_ **98**, 062107 (2018)


```C
int currentparticlenumber = 1;
double currenttime = 0;
double maxtime = 1000;
double eventrate = (double) currentparticlenumber;

while (currenttime < maxtime){
 currenttime = currenttime + gsl_ran_exponential(r,1.0/mu);
 currentparticlenumber = currentparticlenumber+gsl_ran_geometric(r, p0)-2;
 eventrate = (double) currentparticlenumber;
}

```
