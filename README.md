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

(ii) RCBHT Information (Left and Right Arms)

- Segments:
contains information about how the original FT data is segmented by a regression fit for all 6 FT axes. Data include: iteration, average magnitude value, maximum magnitude value, minimum magnitude value, start time, finish time, gradient value, and gradient lable.

- Composites:
contains information of how neighboring segments are combined (though affected by MC filtering rules) for all 6 FT axes. Data include iteration, MC label, avg val across segments, root-mean-square value across segments, amplitude value across segments, gradient labels for both segments, start, end, avg time for both segments.

- llBehaviors:
- contains information of how neighboring actions are combined (though affected by LLB filtering rules) for all 6 FT axes. Data is kept in file (.txt) format and also in matlab format (.mat) and include the following info: iteration, llb label, avg. val for mc1 & mc2, avg val for combination of mc1&2, same for rms value and amplitude value, mc label 1 and 2, time they start and finish respectively, and the average time for both of them.