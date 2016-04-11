Data from snap assembly work in simulation with the HIRO Robot. In particular this package is focusing on dual arm assembly under different coordination schemes. Male-push female-hold (MPFH) and male-hold female-push (MHFP) for specific failure cases. Location: Guangzhou, China. Dates: 2015.

Each folder contains data for: (i) the left and right arms and (ii) state estimation files related to the RCBHT. Also note that the experimental data is grouped into different under different coordination schemes. So far: MPFH and MHFP.

(i) Arm Data
- L_/R_Angles: Current Joint Angles (7 DoF)
Format: time th1 th2 ... th7

- L_/R_CartPos: EndEffector Cartesian Position
Format: time x y z r p y

- L_/R_Torques: Wrench data wrt the tool. No gravity compensation.
Format: time Fx Fy Fz Mx My Mz

- L_/R_GC_Torques: Gravity compensated wrench data wrt the tool. 
Format: time Fx Fy Fz Mx My Mz

- L_/R_GC_worldTorques: Gravity compensated wrench data wrt the world. 
Format: time Fx Fy Fz Mx My Mz

- L_/R_State: State Transition Time Vector.
Format: time

Note:
In our current simulation data set, the noise function which introduces variation into the model was not working properly. All trials within a coordination scheme currently report exactly the same data :(


