# A7 – [Bracket FEA]

## Objective
- Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
- Ensure high stiffness, strength, and lightweight optimization through iterative design.
- Conduct multiple FEA simulations, refining geometry based on results.
- Perform static stress analysis, including constraints, loading, and meshing selection.
- Interpret data by identifying max stress, displacement, and safety factors.
- Optimize the design by modifying geometry to enhance performance.
- Document the entire process with images, calculations, and insights.
- Reflect on key engineering lessons learned and time spent.

## Description
The task is simply to create a high stiff, high strength, and lightweight component. Use Finite Element analysis to drive your decision making process throughout your design. Each step of the analysis and before you make geometric changes make sure the component’s results (stress/displacement/Safety Factor) converge on a 7% difference. Achieve this by modifying the number of elements. If after three attempts to converge use the stiffness and stress from the finer mesh size use the finest mesh size and proceed through the process.
![Description](./description.jpeg)

## Designs

### Design 1
In order to achieve a convergence of 7% or less for stress, displacement, and safety factor, I started with my original design from assignments 5 and 6. Once I had this part pulled up on Creo I went back to edit the material and make sure everything was up to date and to the correct specs, throughout each design I also kept track of the mass. Afterwards I went ahead and started my simulation process by adding a downward force of 600lb to the circular shaft and a fixed force on the bottom face of the E section of my bracket. With these forces I ran 3 simulations for course mesh, fine/course mesh, and fine mesh, out of the three I was able to achieve less than 7% convergence on mesh 2 and 3. However my safety factor was still far below the threshold of 1, which meant I still needed to make some design adjustments in order for my bracket not to fail under load. 

![Description](./materialproperties.jpg)
![Description](./mass.jpg)
![Description](./design1.jpg)
![Description](./forces.jpg)


#### Mesh 1
![Description](./d1mesh1stress.jpg)
![Description](./d1mesh1deform.jpg)


#### Mesh 2
![Description](./d1mesh2stress.jpg)
![Description](./d1mesh2deform.jpg)








## Decide


## Communicate

