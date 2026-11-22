# A11 – Motor Selection

## Objective
Develop the motorized drive and structural integration for the 2 kN tensile tester, focusing on motor selection, mounting, frame stability, and clamp design. This phase will ensure that the crosshead moves smoothly under controlled torque and speed while maintaining precise load alignment and secure specimen gripping.

![Description](./description.jpg)

## Motor Selection
This assignment requires us to mount a motor to our previously designed tensile tester for assignment 10. In order to do so the first thing I did was write down my knowns from the previous assignment, since I already had the range of speed and torque determined I could do some research to determine a motor. After doing some research I decided a stepper motor would be the best fit for my application, more specifically I went with a 15:1 Nema 23 Stepper Motor. I utilized the CAD download and torque curve from [Stepper Online](https://www.omc-stepperonline.com/nema-23-stepper-motor-l-56mm-gear-ratio-15-1-high-precision-planetary-gearbox-23hs22-2804s-hg15) but eventually decided that buying one from [Phidgets](https://www.phidgets.com/?prodid=352#Tab_Downloads) would be more cost effective. 

![Description](./motorselection.jpeg)
![Description](./motormount.jpeg)
![Description](./torquecurve.jpg)


## Motor Mount Design
The next step in the process was designing a motor mount/bracket for the stepper motor. First things first I listed my knowns and unknowns of the design and created a simple free body diagram of where the forces would be applied to the bracket. The FBD remained fairly simple because I was able to use the provided schematics of the motor have a general idea on what the dimensions should be. This allowed me to apply bearing stress calculations to derive the necessary thickness for the bracket. 

![Description](./motordimensions.jpg)
![Description](./motormount.jpeg)

![Description](./motormount.jpg)
![Description](./motormount1.jpg)
![Description](./motormount2.jpg)
![Description](./motormount3.jpg)
![Description](./motormount4.jpg)



## Coupler Design
In order for the lead screws to fit into the bracket I needed to design a coupler. Using shear stress torsion analysis to determine the inner and outer diameter of the coupler, I first came up with some assumptions for the yield strength and shear stress of the coupler based on using steel as the coupler material. Using torque analysis, I landed as 20mm as my thickness, this allows me to buy a coupler rather than design and manufacture one. 

![Description](./coupler.jpeg)
![Description](./setscrew.jpg)



## Frame Analysis and Design
Before adding to the previous design I needed to allowable stress acting on the frame due to the torque caused by the motors. to do so I listed the knowns and unknowns, and I drew a FBD with the combined forces acting on the frame. I stated in the assumptions that I would be using M5 screws bought from Grainger to bolt the frame together. Using shear stress analysis the allowable stress range came out to be between 50.93mpa and 278.07mpa. 

![Description](./frame.jpeg)

## FEA on Frame
Before starting the analysis, I went ahead and applied the wide corner brackets from Grainger to the frame but did not apply each of the screws because it was very tedious to do. Using the 2kn load at the top cross bar and constraining the bottom legs to a fixed constraint, I ran three meshes. The deflection converged fine, but the stress did not converge and was way higher than the max allowable stress. The reason for the excessively high stress was due to there being no screws and the bad convergence was due to the sharp corners of the bracket. This could be fixed by adding fillets to the corner of the bracket or adding a web in the middle of the bracket. An alternative method and arguably a better method would be welding the frame together with TIG process or a MIG process with an aluminum spool torch. 

![Description](./feamesh1stress.jpg)
![Description](./feamesh1deflection.jpg)
![Description](./feamesh2stress.jpg)
![Description](./feamesh2deflection.jpg)
![Description](./feamesh3stress.jpg)
![Description](./feamesh3deflection.jpg)
![Description](./convergence.jpg)

## Bearing Mount Design
To design a bearing mount with an RC3 fit I needed to utilize the machinery's handbook. Referencing Table:8a on page 654 I listed my known outer diameter and needed tolerances for the design. From here I drew the FBD and proceeded to solve for the thickness and diameter of the inner wall using torque analysis equations. 

![Description](./bearingmount.jpeg)
![Description](./bearingmount1.jpg)
![Description](./bearingmount2.jpg)
![Description](./bearingmount3.jpg)
![Description](./bearingmount4.jpg)
![Description](./bearingmount5.jpg)

## Bill of Materials 
| Item # | Quantity | Name | Cost/Item | Cost | Purchase Link |
| :--- | :---: | :--- | ---: | ---: | :--- |
| 804T48 | 1 | T-Slot Framing System: Rectangle, 40 Series, Smooth, Double, 3 m Nom Lg, 80 mm x 40 mm, 6 Slots, Std | $245.87 | $245.87 | [Grainger](https://www.grainger.com/product/80-20-T-Slot-Framing-System-Rectangle-804T48) |
| 95120A119 | 2 | 932 Bearing Bronze Acme Flange Nut | $138.20 | $276.40 | [McMaster-Carr](https://www.mcmaster.com/95120A119/) |
| 98935A914 | 2 | Carbon Steel Acme Lead Screw | $10.29 | $20.58 | [McMaster-Carr](https://www.mcmaster.com/98935A914/) |
| 3333_0 | 2 | Nema 23 Stepper Motor | $72.00 | $144.00 | [Phidgets](https://www.phidgets.com/?prodid=352#Tab_Downloads) |
| 5JRU7 | 6 |  Wide Inside-Corner Bracket | $10.92 | $65.52 | [Grainger](https://www.grainger.com/product/80-20-Inside-Corner-Bracket-Wide-5JRU7) |
| 55MT26 | 24 | Hammer Nut | $3.50 | $21.00 | [Grainger](https://www.grainger.com/product/FATH-INC-Hammer-Nut-M5-Size-55MT26) |
| 3613N15 | 2 | Set Screw Shaft Coupling | $74.49 | $148.98 | [Mcmaster-Carr](https://www.mcmaster.com/3613N15/) |
| | | | Total Cost | $655.48 | |

## Labor Cost
| Person | Hours Worked | Cost/Hour | Cost |
| :--- | :---: | :--- | ---: | 
| Keegan Fine | 25hrs | $35/hr | $875 | 

## Total Cost of Project
| Total Cost | $1530.48 | 
| :--- | ---: |

## Final Assembly Design 
After tabulating the costs and running the FEA analysis I designed and assembled the final tensile tester. To offset the excess stress and stability I added the wide brackets and hammer nuts to corners as well as adding legs out of the extra T-slot frame to create stability when under load. 

 ![Description](./assembly.jpg)


## Lessons Learned 

Part 1 and 2 of this assignment took me a total of around 25 hours to complete. The biggest lesson I learned was using SolidWorks to assemble a motor onto an assembly as well as using FEA in a real-world application. Due to the heavy CAD design and dimension analysis, I learned how to research motors and using the torque curve to pick the correct one as well as being able to know when to buy vs design certain parts such as the coupler. Using the Design calculations sections of the Thesis on Design and Manufacturing from Stella Demmel was very helpful when figuring out how to find the correct dimensions and thickness for the bearing mount design and the coupler design. Overall, this project tested my knowledge, work ethic, and ability to problem solve and research parts and equipment. 

## CAD Files
[Download Assembly (.zip)](./assemblymotor.zip)


























