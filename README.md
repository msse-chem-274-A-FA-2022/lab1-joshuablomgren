# Chem 274A - Lab 1

In this lab, you will be using the molecular simulation code we wrote in Chem 280 - Foundations of Molecular Modelling and Software Engineering.

## Exercises

### Section 1 - Makefile (Spend 30 minutes max on this)
1. Use the `makefile` to create an environment for this lab.
    ```
    cd mcsim_python
    make environment
    ```
2. Activate the environment created by the `makefile`
    ```
    conda activate chem274A_lab1
    ```
3. Use the `makefile` to install `mcsim`
    ```
    make install
    ```

4. Review the Makefile in `mcsim_python`. Write a comment above each target explaining what the target does.

### Section 2 - Runnning Simulations
1. Use the notebook `run_mcsim.ipynb` to run Monte Carlo simulations. Follow the instructions in the notebook.

## Answers to Notebook Questions

### Equilibration 
For the simulation with 100,000 steps, the more steps the simulation runs, energy per particle hovers around approximately -6, and pressure decreases down to around 3.8. 

For the simulation run with decreased steps, the energy per particle and pressure are both huge: 5001938027768.223 and 18006977280635.52 respectively. 

For the simulation with 100,000 steps, in the graph "Steps vs Energy per Particle", energy per particle starts off really at 8.191654e+07 and drastically decreases at 10,000 steps to 28.97 and crosses over to be negative starting at 20,000 steps. For the simulation with 1 step, the graph only has one dot. 


### Production
After reaching equilibrium, the next 100,000 steps bring energy per particle from -6.037 to -6.207, hovering around -6.0 to -6.2 fairly sporadically. Pressure continues to consistently decrease, going from 3.812 to 2.936. 

For the second simulation, the energy per particle and pressure decrease but only very slightly, the numbers are still huge (energy: 4990528607360.81, pressure: 17965903347728.914)

The graph for the RDF after 100,000 steps displays the probability of finding another particle a certain distance away from another particle. The RDF graph here looks like that of a Lennard Jones fluid. 

The RDF graph for the decreased steps has a huge peak at less than 0.1 and has sporadic tiny peaks everywhere.This is because the system is not near at all equilibrium in the trial with significally less steps because a lot for steps are necessary for the MC sim to bring the system closer to equilibrium. This does not look like what would happen in real life. 


Q4) For density=0.9, the RDF graph has a peak at around 1.1 sigma away and has subsequent peaks that gradually flatten out.
For density=0.009, the RDF graph has a similar peak around 1.1-1.3 sigma away, but then flattens out and has sporadic tiny peaks. 