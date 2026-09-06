# A3 – [Parametric and FEA]

## Objective
- Use axial deflection modeling to design its dimensions
- Use parametric design to determine a bars length
- Introduce you to FEA (Finite Element Analysis)
- Introduce you to linking dimensions to appropriate parameters in CAD.
- Compare and contrast the different analysis
 ![Description](./Beam-Description.jpg)

## Design Process


### Design Drawing / Calculations
![Design](./design-drawing.jpeg)
Given the beam description and the provided values, I was tasked to construct a beam with a circular cross section and find the optimal length that could satisfy a max axial deflection of .009in and withstand a tensile load of 400lb. to do this I chose a diameter of .5in and solved for the cross-sectional area. After finding the cross-sectional area, I was able to derive the beam length from the direct tension elongation equation. 

### CAD Design 
![CAD Beam](./bar-overall-structure.jpg)

To design a beam with specific parameters and an Aluminum material I used Creo because it had more freedom in terms of what parameters could be set and how they were utilized. 
- Step 1 (Parameters): Before creating a sketch, I opened the parameters settings underneath the modify bar in Creo and entered in the given values for force, axial deflection, elasticity for aluminum, and the diameter for the bar. In order to check my hand calculations, the cross-sectional Area equation and Length equation was plugged into the relations box. this worked similar to an excel sheet by allowing the user parameters to work directly with these equations.

![Parameters](./parameter-table-CAD.jpg)

![Parameters](./parameter-equations-CAD.jpg)

- Step 2 (Sketch & Extrude): Now that the parameters were set, I drew a simple circular sketch and directly applied the user parameters by labeling my dimension as d0. From here the circle was extruded into a cylindrical beam and given a length of d1 which equaled the length equation that was previously put into the relations box. In Creo for a design to contain a material it must first be a 3D model, so now I was able to go into the modify materials settings under file>prepare and change it to Aluminum.

![Sketch](./DIameter-Sketch.jpg)

![Extrude](./bar-length.jpg)

![Material](./Material-CAD.jpg)

- Step 3: 
 
## Design Reflection 
![Design Reflection](./design-reflection.jpeg)


## Decide


## Communicate

