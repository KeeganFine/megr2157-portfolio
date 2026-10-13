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
![Description](./appendix.jpeg)

## Designs

### Design 1
In order to achieve a convergence of 7% or less for stress, displacement, and safety factor, I started with my original design from assignments 5 and 6. Once I had this part pulled up on Creo I went back to edit the material and make sure everything was up to date and to the correct specs, throughout each design I also kept track of the mass. Afterwards I went ahead and started my simulation process by adding a downward force of 600lb to the cylindrical shaft (section A) and a fixed force on the bottom face of Section E of my bracket; these forces created a virtual simulation of a fixed bracket being pulled by a tensile force of 600lbf. With these forces installed I ran 3 FEA simulations for course mesh, fine/course mesh, and fine mesh, out of the three I was able to achieve less than 7% convergence on mesh 2 and 3. However my safety factor was still far below the threshold of 1, which meant I still needed to make some design adjustments in order for my bracket not to fail under load. 

![Description](./materialproperties.jpg)
![Description](./mass.jpg)
![Description](./design1.jpg)
![Description](./forces.jpg)


**- Mesh 1:**
![Description](./d1mesh1stress.jpg)
![Description](./d1mesh1deform.jpg)


**- Mesh 2:**
![Description](./d1mesh2stress.jpg)
![Description](./d1mesh2deform.jpg)


**- Mesh 3:**
![Description](./d1mesh3stress.jpg)
![Description](./d1mesh3deform.jpg)


**- Convergence Calculations:**
![Description](./d1calc.jpeg)


**- Design 1 Table (Mesh 3 Values):**
|      | Design I | 
| :--- | :---: |
| Safety Factor | .180 |
| Max Stress (ksi)/Location | 221.76/Between A & B  | 
| Deflection (in)/Loaction | 0.136/Section B| 
| Mass (lbm) | .268|
| Element Count| 10021 |


### Design 2
In order to reduce the stress concentrations occurring between the cylindrical shaft (section A) and the neck/backplate (section B), I added a fillet of .10 in between the two sections. This modification slightly lowered the stress and deflection of the bracket. However after calculating for a safety factor of around .2 overall, I was still well below the threshold. For this design I ran an FEA simulation for course mesh, fine/course mesh, and fine mesh. The convergence for Mesh 1 and 2 was slightly over 7%, however the convergence for mesh 2 and 3 was able to yield a convergence of under 7%. 

![Description](./design2.jpg)
![Description](./design2fillet.jpg)


**- Mesh 1:**
![Description](./d2mesh1stress.jpg)
![Description](./d2mesh1deform.jpg)


**- Mesh 2:**
![Description](./d2mesh2stress.jpg)
![Description](./d2mesh2deform.jpg)


**- Mesh 3:**
![Description](./d2mesh3stress.jpg)
![Description](./d2mesh3deform.jpg)


**- Convergence Calculations:**
![Description](./d2calc.jpeg)


**- Design 1 & 2 Table (Mesh 3 Values):**
|      | Design I |  Design II |
| :--- | :---: | ---: |
| Safety Factor | .180 | .241 |
| Max Stress (ksi)/Location | 221.76/Between A & B  | 165.74/Between A & B |
| Deflection (in)/Location | 0.136/Section B| .130/Section B |
| Mass (lbm) | .268| .268 | 
| Element Count| 10021 | 27831 |

### Design 3 
The previous design still had a very high stress concentration between Section A and B even after slight modifications. In my final design I was able to fix that issue by adding a few larger modifications. I widened the backplate/neck (section B), this created a much stiffer and ore rigid design to keep from bending and deforming under load. To assist with this, I also added a front support beam between the shaft (section A) and the bottom of section C, this stopped the large amount stress from being concentrated Between sections A and B and become distributed along the shaft. The support beam allowed for almost no deflection under the 600lb load. After making thee modifications I added chamfers and fillets to needed sections to avoid stress concentrations. I then ran an FEA simulation for course mesh and fine/course mesh. The convergence for Mesh 1 and 2 was well under 7% with a calculated safety factor of 2.83 which meant this bracket would not fail under a load of 600lbf. 

 ![Description](./design3.jpg)
 
 ![Description](./design3neck.jpg)
 
 ![Description](./design3extrude.jpg)
 
 ![Description](./design3fillet.jpg)


 **- Mesh 1:**
![Description](./d3mesh1stress.jpg)
![Description](./d3mesh1deform.jpg)


**- Mesh 2:**
![Description](./d3mesh2stress.jpg)
![Description](./d3mesh2deform.jpg)


**- Convergence Calculations:**
![Description](./d3calc.jpeg)


**- Design 1, 2, and 3 Table (Mesh 3 Values):**
|      | Design I |  Design II | Design III |
| :--- | :---: | :---: |---: |
| Safety Factor | .180 | .241 | 2.83 |
| Max Stress (ksi)/Location | 221.76/Between A & B  | 165.74/Between A & B | 14.11/distributed across support beam, C, A, & B |
| Deflection (in)/Location | 0.136/Section B| .130/Section B | .0039/Section B & support beam |
| Mass (lbm) | .268| .268 | .293 |
| Element Count| 10021 | 27831 | 61431 |


## Lessons Learned

This assignment took about 8 hours total. A majority of that time was spent making sure every file and screenshot was saved as a jpeg and organized in a folder throughout the assignment. Doing so limited any user error or loss of work when it came time to put the information together in GitHub. The important lessons learned were using mesh with FEA simulations, convergence calculations, and element count. It originally took me about an hour to understand how to use mesh properly. I had to do some research on the mesh settings in Creo and was able to successfully use them after a few trial and errors. for my convergence calculations I learned to take the percent difference of the mesh 1 and 2 and mesh 3 and 4. The element count was an obstacle because I was unable to find the exact number on Creo so I learned how to manually calculate it. However, this may result in a slightly incorrect element count due to user error. By the end of this assignment, I felt very confident in my understanding on how FEA analysis works and how to visualize what's happening to a design when a load is implemented and how to better the design myself. 

## CAD Files 
[Download Design 1 (.zip)](./a7design1.prt.zip)
[Download Design 2 (.zip)](./a7desgn2.prt.zip)
[Download Design 3 (.zip)](./a7desgn3.prt.zip)


## Convergence Calculation Files
[Download Convergence Calculations (.pdf)](./docs/a7convergence.pdf)







 
















