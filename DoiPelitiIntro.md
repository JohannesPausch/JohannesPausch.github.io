# Brief introduction to 
# Doi-Peliti Field Theory

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"> </script>
<link rel="stylesheet" type="text/css" href="https://tikzjax.com/v1/fonts.css">
<script src="https://tikzjax.com/v1/tikzjax.js"></script>

Doi-Peliti Field Theory is a method to describe stochastic processes which can be cast in a Master Equation. It is an equivalent representation to the Master Equation and does inprinciple not involve simplifications or approximations which can occur when deriving Fokker-Planck Equations or Langevin Equations.
The reason why I present some introductory information about Doi-Peliti Field Theory here is that there are not many textbook-level notes avilable and easily accessible. The derivation of Doi-Peliti Field theory follows three steps:
 <ol>
  <li>Set-up of Master Equation</li>
  <li>Using Second Quantization to derive an equivalent Equation of the Probability Generating Function</li>
  <li>Deriving the Action of the Field Theory</li>
</ol> 

A useful introductory example is the system in which particles undergo an extinction process and a spontaneous creation process. We use $$\epsilon$$ as extinction rate and $$\gamma$$ as spontaneous creation rate. Then the three derivation steps work out as follows:

## Master Equation

Let's denote the probability that the system contains $$n$$ particles at time $$t$$ by $$P(N=n,t)$$. Then the Master Equation is

$$\frac{\partial}{\partial t}P(N=n,t)=\epsilon\Bigl((n+1)P(N=n+1,t)-nP(N=n,t)\Bigr)+$$

$$\qquad\quad+\gamma\Bigl(P(N=n-1,t)-P(N=n,t)\Bigr)$$

Although we only wrote one equation, the Master Equation is a system of infinitely many linear coupled ordinary differntial equations - one equation for every $$n\in\mathbb{N}_0$$.

The Master Equation could be solved directly, but here we want to illustrate how to derive a Doi-Peliti field theory in principle.

## Second Quantization

Second Quantization is a language that hides some of the complicated functions we are dealing with behind nice notation. If the system contains $$n$$ particles, we write $$\vert n\rangle $$. We introduce operators $$a$$ and $$a^\dagger$$ which have the following properties:

$$[a,a^\dagger]=aa^\dagger-a^\dagger a=1$$

$$a|n\rangle=n|n-1\rangle$$

$$a^\dagger|n\rangle=|n+1\rangle$$

The operators allow us to increase or decrease the number of particles in the system one particle at a time, much like climbing up or down a ladder. The operators are therefore called ladder operators. Given their effect on the particle number, $$a$$ is called annihilation operator and $$a^\dagger$$ is called creation operator. We can write the probability generating function of the system as follows

$$|\mathcal{M}(t)\rangle=\sum\limits_{n=0}^\infty P(N=n,t)|n\rangle.$$

Taking its time-derivative and using the Master Equation to replace the occuring time-derivatives of $$P$$, we find

$$\frac{\partial}{\partial t}|\mathcal{M}(t)\rangle=\underbrace{\Bigl(\epsilon(1-a^\dagger)a+\gamma(a^\dagger-1)\Bigr)}_{=:\mathcal{H}[a^\dagger,a]}|\mathcal{M}(t)\rangle$$

## The Action of the Field Theory

Once the equation for $$\partial\vert\mathcal{M}(t)\rangle/\partial t $$ is derived the action of the field theory can be readily written down as follows

$$\mathcal{A}[\widetilde\phi,\phi]=\int\widetilde\phi(-\partial_t)\phi+\mathcal{H}[\widetilde\phi+1,\phi]\,\text{d}t$$

$$n$$-point correlation functions can then be calculated from the Path Integral

$$\langle\bullet\rangle=\int\mathcal{D}[\widetilde\phi,\phi]\bullet e^{\mathcal{A}[\widetilde\phi,\phi]}$$

For example, in order to calculate the mean number of particles in the steady state, we calculate

$$\mathbb{E}[N]=\langle\phi(t)\rangle=\int\underbrace{\frac{\delta(\omega+\omega')e^{-i\omega t}}{-i\omega+\epsilon}}_{\text{propagator}}\underbrace{\gamma\delta(\omega')}_{\text{source}}\text{d}\omega'\text{d}\omega=\frac{\gamma}{\epsilon},$$

which would be represented by this admittedly simple Feynman diagram

<script type="text/tikz">
  \begin{tikzpicture}
    \filldraw[very thick,color=teal] (-0.5,0) -- (0.5,0) circle [radius=0.1cm];
    \draw[->] (-1.9,-1.6) node {$$propagator$$} -- (-0.1,-0.1);
    \draw [->] (2.0,-1.6) node {$$source$$} -- (0.6,-0.1);
  \end{tikzpicture}
</script>

In particular, the Feynman diagrams of a Doi-Peliti Field theory are read from right to left.
