# Stochastic Processes - Models and Simulations

I'm interested in stochastic processes in neuroscience, biology and physics. They can be microscopic, for example in chemical reactions or macroscopic like dynamics of population; they can be on short time scales, as in the propagation of action potentials between neurons, or over a long time such as during the evolution of organisms. 

More about me is [here](CV.md).
My website at Imperial College London is [here](https://www.imperial.ac.uk/people/j.pausch15). I work in the group of [Philipp Thomas](https://www.ma.imperial.ac.uk/~pthomas/) on time-dependent models of cell populations in cooperation with the group of [Alexis Barr](https://lms.mrc.ac.uk/research-group/cell-cycle-control/) at the MRC London Institute of Medical Sciences.

My workflow:
- Identifiy what are the important features (space, interactions, memory?)
- Build analytically tractable model that shares these features
- Compare to simulations and real world
- Get confused/awed by real world and start workflow at the top again

There is a plethora of methods for analytical models out there and a large spectrum of techniques to create simulations. Similarly, analysing data can be done in a hundred different ways. Here are my personal favorites:
- [**Doi-Peliti field theory**](DoiPelitiIntro.md) for creating models. This class of models originated in in the 1970s and 80s in theoretical physics and has been used to understand emergent phenomena in chemical reactions and population dynamics. As a comparatively young theory, there is still a lot of research on what it can and cannot achieve. Of course _you shouldn't ask what field theory can do for you, but what you can do for field theory_. My Part III lecture notes on the topic can be found [here](NESFT-Pausch-LectureNotes2020.pdf).
- **C** for simulations. This is often debated: what programming language should you use. There are pros and cons for every language, but I rarely hear that C is slower than another language (unless you use assembler or highly optimized Fortran). In combination with the [**GNU Scientific Library**](https://www.gnu.org/software/gsl/), the stochastic world is your oyster.
- Comparing analytics to simulations and data can be tricky and I don't have any favorites here. But, fitting power laws is an art in itself. 
- [**gnuplot**](http://www.gnuplot.info/) is currently my preferred plotting program: it is fast and has a better implementation of LaTeX compared to matplotlib, imo.

## Projects
Here is an incomplete list of projects that I have worked on or am currently working on.
### [Phase transitions of Leaky integrate-and-fire models (2023)](LIF-PhaseTransitions.md)
### [Time-dependent cell population dynamics (2023)](PeriodicTreatment.md)
### [Neural Spikes (2022)](FromBranchingToSpikes.md)
### [Noisy Branching (2021)](NoiseDrivenBranching.md)  
### [Coupled Branching (2021)](CoupledBranching.md)
### [Branching and Oscillations in Neuronal Avalanches (2020)](OscillatingParameters.md)
### [Stochastic Filament Growth (2019)](Microtubule.md)
### [Branching (2018)](Branching.md)


