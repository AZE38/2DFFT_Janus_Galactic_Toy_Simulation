# 2DFFT_Janus_Galactic_Toy_Simulation

2D Toy model Janus Fluids anti gravity Effects (Jean Pierre Petit Newtonian model) : "IN PROGRESS"

axisymmetrical "unphysical" Test model to play with anti gravity effect on a disk shaped rotating disk galaxy and 2D (pseudo-3D Poisson) FFT solver and leapfrog update.



in first we initialise the density with random exp disk shaped galactic fluids of positive mass wihtout velocity.

To initialise the negative points mass Fluids population around the galaxy we perform " Backward integration technics " and imposed Boundary condition at the border of a periodic 2D box domain , solving by iteration and self consitency , we converge on a final density and velocity distribution that is in steady states , around the fixed initial disk shaped of positive mass (easly applicable to a random 3D shape for futur simulation in 3D).
 
Example of initial state of Negative Density FLuid around the fixed galaxy:
![image](https://github.com/user-attachments/assets/2624d861-6cac-422b-bdd9-5d889abcc8a2)


on the positive masse galaxtic fluids , we impose some random initial condition with anisotropic dispersion , and calculate the equilibrium of the pur circular velocity orbit of the initial disk shaped density on the combined potential of positive and negative masses using Fast Fourier Transform on periodic domain.


in a future work we need to derive a real steady state of the galaxy too.

the initial density repartition of the galaxy can be exponential disk , gaussian 

EXAMPLES: 

      Curve V_circ without or very low density of negative masses : 
    ![image](https://github.com/user-attachments/assets/f768da25-a18a-4180-9f6c-2a8546aeefbd)


     Curve V_circ with high negative masses (rising effect at large radius from the hole confinement):    
    ![image](https://github.com/user-attachments/assets/65a3a9f1-bdad-436c-940c-e20742804473)


Running the simulation , we can observe some spirals formations or different galaxy structure , in function of initials conditions with low dissipation , 1) and 2) dont display the negative mass fluids but its present in simulation:

1: initial Large Scale Radius, low dispersion + pur circular velocity equilibrium 
  a.  ![Capture d’écran 2025-01-06 121007](https://github.com/user-attachments/assets/827ef366-6cf2-4061-b26a-90200166adc2)

  NGC6684 comparison :
  b.![image](https://github.com/user-attachments/assets/6114eaa2-cb01-4835-afd2-29f15db47810)

  c. ![image](https://github.com/user-attachments/assets/58faec3d-1653-44c0-9baa-6ed30304c9c8)

  d. 3-Arms to "NGC 6684" 
  ![Density_animation33](https://github.com/user-attachments/assets/8bbd7b8d-3fd3-4f11-818c-9dde94e7ba94)




2: No Rotation , Steady state Anisotropic
![stableAnisotropicNoRot](https://github.com/user-attachments/assets/fb7d5b4b-8fac-4921-b01e-1b4ade37e5e0)


3: See other Gif or image examples into the repo..

  



Images in log colors

Potential Issues :

    0 - Need to review code and check errors calculs

    1 - when making the backwards integrations methods , we impose the same distribution on the boundary of the simulation, if the domain is "circular" its good , but we have a box domain and for more accurate steady state (when negative mass density is high), we need to shift a little bit the distribution function in energy (and anistropy ?) to reach a better steady state (" à faire " futur work). The point of view used to solve the potential is reverted and the galaxy act as the negative mass on the backwarded fluids, to make easier the implementation and change nothing on the result.., its just observer dependent with same anti gravity effect.

    in fact the boundary distribution function need to be calculate with the JCM model after the Very Large Structures formation, its the residual gas , not collapsed into Proto Giant negative stars (Janus Cosmological Model). ("à faire") At this time we have a simple truncated Maxwellian keeping only hign energy , that are the unbounded particle residual gas.

    2 - the galaxy structure depend on initial condition , high or low anistropic dispersion , initial added rotation , value of negative density and velocity.   Need explorations , what if we start more from steady state without rotation from spherical galaxy ? multiple galaxies interaction ? to give realistic initial rotation impulse ?

    3 - We use 3D Poisson equation and solve it in a "slice" 2D periodic domain, It's UNPHYSICAL but we can see some interresting feature on the circular velocity curve rising due to negative density hole effect, and less dissipation of spirals arms structure.

    4- Need to add some circular rotation plot curve during the simulation steps.

    5- From bi metric point of view , we keep symmetrical spacetime factors between both metrics -> [g/h]^1/2 = 1.

    6 - Need to review code and check errors calculs a second time !! ;) 

    7 - Need to list some fixed value paramters that produce few differents galaxies types, and find mechanism of the formation.

    8 - Need to add multiple component fluids of galaxy , like stars + gas .

    9 - Make better rendering of particles

this Code produce some density plot at interval dt , and make a gif of the result skipping some frame (Beware of the stroboscopic effect illusion on the rotation of the galaxy on the gif with skipped frames !! )

You can run the code in Notebook , modify parameters and/or adapt your own intial function or adapt the code as needed.

(need to refactor and optimize correctly all the code and make comment on all paramaters used , in few days...)

PS:

 J.Petit - F.Lhanseat from : https://www.jp-petit.org/science/f300/f3900/f3906.htm 

we can Read from another Simulation test : 
"Anyway, F.Lhandseat adjusted the conditions empirically and found that the things looked good when the characteristic rotation velocity (the maximum value) was   about ten times smaller than the mean thermal in the cluster (positive mass sub-system)"

They start from steady state without rotation , and add some circular velocity according to " r * cp.exp(-r / R0) " expression and the condition of smaller characteristic rotation velocity that dispersion
when assigning curve like J.Petit - F.Lhanseat like 

but here in this simulation , its possible to find some steady state solution with some large radius anisotropic with good value of dispersion but when assigning the profil of circular velocity of J.Petit - F.Lhanseat to the cluster with different value of peak characteristics , we cant find same spiral solution like in their simulation.

we find some spiral structure when we start from initial large scale radius exponential, gaussian  density profil , with high circular equilibrium velocity component and very low dispersion component.

(may be we have calculs error , or artifact from our periodic domain ?).

Conclusion : The code seem to produce some didactic features of the galactic dynamics , like the rising effect of the hole confinement of negative masse on 
    the circular velocity at large radius .

    Global structure of galaxy strongly depends on the initial condition given.

keepind in mind that our simulation is unphysical because of the 2D sheet domain with 3D FFT Poisson concept , we can explore some parameters and hope that in Full
3D simulation , some characterstics of the dynamic are present too. 




