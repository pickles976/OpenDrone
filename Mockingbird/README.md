# MockingBird

<img src="../images/mockingbird_proto_1.jpg" alt="Mockingbird Prototype from Below" width="500">
<img src="../images/mockingbird_proto_2.jpg" alt="Mockingbird Prototype from above" width="500">  


Mockingbird is intended to be the cheapest and simplest drone to make. It has an initial setup cost of about $250 (not including tools), but the unit cost is about $90. Most of that is the electronics.

Every component is designed to fit on the printing plate of a Bambu A1 mini. The design is intended to be slow-flying and stable, with glider-like performance characteristics. The wings can be constructed out of a single piece of 20"x30" 5mm thick foamboard. The design supports multiple receivers and batteries, with variable wing positioning to adjust the center of gravity accordingly.

# Wing Specs

- Armin Wing Design
- 2 parts, 10" x 30" foamboard
- assembled dimensions
    - chord: 0.15m
    - wingspan: 1.524m
    - area: 0.2286m^2
- aspect ratio: 10.15 (wingspan squared over wing area)
- taper ratio: 1

An aspect ratio of 10 just barely puts us into glider territory. The wing design is a modified [Armin wing design](https://www.youtube.com/watch?v=karr67ZYho4) tweaked to take up exactly one sheet of 20"x30" foamboard.

### Equations
```math
Aspect Ratio = \frac SA
```

```math
\begin{aligned}
Wing Loading = \frac WA \\
Wing Loading = \frac 12 \rho V_{stall}^2 C_{Lift Max}  \\
V_{stall} = \sqrt{\frac {2\frac WA} {\rho C_{Lift Max}}} \\

\rho = 1.225 \\
C_{Lift Max} = 1.5

\end{aligned}
```

![](./wing_loading.png)
Wing Loading Curve  


![](./stall_speed.png)
Stall Speed Curve   

Target weight is 650g, which would give us a stall speed of ~5mph.


#### Tips and Tricks

**Print the Electronics Payload at an angle on the Bambu A1 Mini**
There may be temperature issues at the edges of the printing plate on the Bambu A1 mini. Try printing it at an angle to see if that helps at all.

**Do your wing balancing before you cut your push rods for the tailfin control surfaces to length**   
It is easier to adjust your balance by moving the tailfin length, so the length of your tailfin will be dependent on the balance. Once that is determined, then you can adjust the length of your pushrods.

**Use 1.2mm wire control rods for tail control surfaces**  
The tail control surfaces are far away from the servos, and 0.64mm piano wire will deform. 1.2mm wire is thick enough to withstand the forces, while also deflecting the desired amount along its path from the servo to the control surface.