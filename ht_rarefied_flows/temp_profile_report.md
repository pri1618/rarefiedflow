# Temperature Profile

### Fluent Settings

**Pipe Characteristics**-

- Inlet length - 80 mm
Zero Heat Flux condition (insulated)
- Constant Wall Temperature - 1090 mm
T = 339K

Pipe Inner Diameter = 22.2 mm

2D Axis symmetric Analysis.

**Inlet Characteristics**-

Mean Kn = 0.00477
P_inlet = 74.4 Pa
P_exit = 55.9 Pa
Inlet Mass Flow Rate - 1.87217e-6 kg/s

T_inlet (Room Temperature) = 300K

**Meshing**-

10086 elements. Inflation at wall.
Growth Rate = 1
Layers = 6

**************Physics**************-

Laminar Model with Low Pressure Boundary Slip. Enabling Viscous Heating does not seem to affect temperature profile.
Energy coupling enabled.

******Material******-

N2 from Fluent Database.
Ideal Gas setting for density. Constant specific heat and thermal conductivity?

- Thermocouples in flow stream give Total Temperature. But Total Temperature and Static Temperature are almost same at subsonic stream velocities.

**************************************Boundary Conditions**************************************-

Pressure Inlet and Mass Flow Outlet.

### **************Plots**************

Temperature profile plot along the axis

![Total Temperature vs Axial position](images/Untitled%204.png)

Total Temperature vs Axial position

![Static Pressure vs Axial Position](images/Untitled%205.png)

Static Pressure vs Axial Position

### **Observations**-

![Untitled](images/Untitled%206.png)

At the end of insulated wall region (x = 0.08m), the total temperature is T = 335.05 K
At x = 0.1460m, the centerline temperature reaches the wall temperature T = 339 K

In my simulations, **89.8%** of the temperature difference is already reached before the fluid enters the constant wall temperature section.

In the experimental findings of Hemadri et al. **71.8%** of the temperature difference is reached before the fluid enters the constant wall temperature section.

Potential causes of the observed disparity-
- Constant Specific Heat and Thermal Conductivity were taken.
- The pressure drop does not match the given data (via mail). 
- Pressure Inlet and Mass Flow Outlet boundary conditions were used and P_exit was observed to be 74.3 Pa as opposed to the given 55.9 Pa.

$$
h = \frac{-K_{f}\frac{\partial(T)}{\partial{y}}}{T_{w} - T_{ax}}
$$

*(Solver was set to symmetric rather than axially symmetric, obtained results are therefore slightly off)*