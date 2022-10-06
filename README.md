# force-inference
Application to find parameters of inter-particle forces from stochastic trajectories using Bayesian inference.

## About the project
Classical description of the constituents of matter using Newton's equations for every atom in the system tends to be intractable because of the high number of atoms. Hence, a small subset of them are characterised using Newtonian dynamics in so-called effective force fields with added stochastic components (Langevin equations).
The goal of this project was to determine these effective forces acting on one Newtonian particle given their trajectories that resemble Brownian motion in the limit of strong friction.

At first, stochastic trajectories of single particles in parametrised forces/potentials were generated using numerical integration of Fokker-Plack equation.
Given only the data on the trajectory, the parameters of forces/potentials were then determined using Bayesian inference. The likelihood function was taken as the solution of the Smoluchowski equation for a linear potential, which approximates the force field at every discrete step of the trajectory. 

The parameters converged to the correct values in all cases using less than half of the available data, even with an uninformative prior, thereby providing the advantage of saving computational time and storage space. 
The method, however, requires increasingly more computational resources once the number of parameter increases and when the intervals of possible values for the parameters are hard to be identified effectively.  

More details regarding the methods and results can be found in the [presentation slides](https://github.com/cristina-v-melnic/force-inference/blob/main/Force_Inference_talk.pdf).

## Credits
This project was part of the coursework of the MSc. Computational Sciences program at FU Berlin in 2020/21. It was initiated and supervised by Dr Mohsen Sadeghi and realised by me as an intern in the "Artificial Intelligence for the Sciences" group, led by Prof. Frank Noé.
