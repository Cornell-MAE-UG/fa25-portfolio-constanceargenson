---
layout: project
title: No Fly Zone
description: Trellis-mounted spotted lanternfly lure-and-capture prototype
permalink: /projects/no-fly-zone/
image: /assets/images/no-fly-zone-final-prototype.jpg
---

# No Fly Zone  
## “Clearing the skies since 2026”

**Team Members:** Constance Argenson, Kate Collard, James Montague, Olivia Polsky, Joshua Tchou  

### Table of Contents
- [Context and Problem Statement](#context-and-problem-statement)
- [Final Prototype and Application](#final-prototype-and-application)
- [Testing and Results](#testing-and-results)
- [Prototype Details](#prototype-details)
- [Conclusions and Recommendations](#conclusions-and-recommendations)
- [Bill of Materials](#bill-of-materials)
- [References](#references)

---

## Context and Problem Statement
<a id="context-and-problem-statement"></a>

The spotted lanternfly (*Lycorma delicatula*), also known as SLF, is an invasive species spreading throughout North America. In vineyards, SLFs remain on grapevines during the harvesting process, contaminating grapes and reducing yields. There is currently no efficient way to remove SLFs directly from grapevines without damaging the plant or requiring significant manual labor. As a result, SLFs continue to feed on vines and remain present during harvest. This project focuses on a vine-level removal process that reduces SLF population density while minimizing labor requirements and avoiding physical damage to grapevines.

---

## Final Prototype and Application
<a id="final-prototype-and-application"></a>

Our team designed and developed a trellis-mounted device that attracts and removes spotted lanternflies directly from grapevines using sensory lures and motorized capture.

![Final prototype](/assets/images/no-fly-zone-final-prototype.jpg)

*Figure 1: Final No Fly Zone prototype.*

The device operates in two stages: attraction followed by capture. Wintergreen oil, a known SLF attractant, is placed near the opening of the device to lure SLFs inside. Once inside, the enclosure geometry guides them toward a secondary chamber, where a geared DC motor drives a rotating, toothed mechanism that directs SLFs into an isolated, removable collection chamber. This motorized system provides continuous movement to prevent escape while minimizing power requirements.

The device is designed to operate continuously throughout the growing season. Because the system is externally mounted and avoids direct contact with grapes or grapevines, it removes SLFs without physically damaging the plant.

---

## Testing and Results
<a id="testing-and-results"></a>

The first success criterion was to create a small, lightweight product, with a target mass of **1 kg** and a target volume of **1 L**. A small and lightweight product makes installation, transportation, and trellis mounting easier.

The second success criterion was to include a single, intuitive on/off switch so that the device would be simple for vineyard workers to operate.

The third success criterion was continuous operation for **24 hours** without running out of power. Ideally, with a solar power source, the product could operate for longer periods. Due to time constraints, this criterion was evaluated using battery power.

Mechanical and electrical testing demonstrated the feasibility of the design and manufacturing process. Most parts were 3D printed, and the system used a **4xAA battery pack**, resulting in a lightweight and energy-efficient device.

### Mechanical Rotation Test
The first test evaluated whether the rotating gate components could rotate **360 degrees** without friction or interference. After assembly, the trap rotated successfully with only slight power losses and friction. This confirmed that the main mechanical trapping component was operational and that 3D printed plastic was feasible for most parts.

### Motor Voltage Test
The second test measured the minimum voltage required for the motor to start and maintain rotation. The motor required **2.47 V** to start and **1.74 V** to sustain rotation. These values were within the capability of the **6 V battery pack**, confirming that the selected power source was sufficient.

### Battery Life
The device used a compact **4xAA battery pack**. Based on current calculations, the battery system can last approximately **six days**, exceeding the success criterion of 24 hours of operation.

### Motor Speed Test
The minimum rotating speed of the original motor was **45 rpm**, which was too fast for the intended trapping motion and could potentially scare SLFs away. As a result, the team decided to replace the motor with one capable of rotating at approximately **20 rpm**, allowing for smoother, slower, and more controlled operation while using less power.

---

## Prototype Details
<a id="prototype-details"></a>

Our prototype consisted of two main subsystems: a mechanical trapping mechanism and an electronics assembly, housed within a 3D printed structure.

The structural housing includes a shielded canopy top, cylindrical main body, and removable screw-in collection chamber. Inside the collection chamber, a wintergreen-oil-soaked sponge acts as the lure.

The trapping mechanism uses a rotating disk, or rotor, and a fixed disk, or stator. Their intersecting slots funnel SLFs downward without crushing them as the rotor spins. The rotor is driven by a DC motor connected to a drive shaft. The motor is controlled through an NPN transistor by an Arduino and operated using a side switch. An LED indicates when the motor is active. A flyback diode protects the motor, and all components share a common ground.

The electronics and battery pack are housed within the main body beneath the trapping mechanism. The collection chamber screws into the bottom for easy removal and emptying.

![Cross sectional diagram](/assets/images/no-fly-zone-cross-section.jpg)

*Figure 2: Cross-sectional diagram of the lure-and-trap prototype, showing the shielding, SLF entryway, Arduino-driven rotating trap disk, quarantine tubes, and removable collection chamber.*

![Rotating gate mechanism](/assets/images/no-fly-zone-rotor.jpg)

*Figure 3: Top-down view of the rotating gate mechanism, showing the direction of rotation that forces SLFs into the collection tubes.*

![Circuit diagram](/assets/images/no-fly-zone-circuit.jpg)

*Figure 4: Electrical schematic and Arduino wiring diagram for the motor control system.*

### Assembly Instructions

1. Glue the two top shade pieces together.
2. Assemble the circuit according to the diagram.
3. Insert the small stator pieces into the stator.
4. Slide the stator and spacing ring onto the shaft.
5. Press fit the shaft into the rotor piece.
6. Solder the shaft into the motor shaft, then place the motor into its housing.
7. Slide the assembled motor, stator, rotor, and spacer ring into the housing.
8. Insert the circuitry, battery, and wintergreen-oil sponge into the housing.
9. Fit the storage container lid into the bottom of the housing, making sure the tubes align with the holes.
10. Screw the storage container into the bottom of the housing.
11. Place the main top component into position and attach string at the top for hanging.

---

## Conclusions and Recommendations
<a id="conclusions-and-recommendations"></a>

Our design was built with scalability in mind. While the prototype works effectively, several changes would be needed before large-scale vineyard deployment.

First, we selected an Arduino instead of a simpler microcontroller because it allows future features to be added. For example, a control panel could be used to monitor battery life and functionality across multiple vineyard devices. This would allow the client to service only devices that need attention rather than checking each trap individually.

Second, solar panels could improve long-term usability. Since replacing batteries across hundreds of vineyard traps would be inefficient and labor-intensive, rechargeable batteries powered by solar panels would allow the devices to operate for longer periods with less maintenance.

Third, the lure system could be improved. While wintergreen oil is effective for a small-scale prototype, the scent fades over time and would require repeated replacement. A speaker emitting a **60 Hz frequency**, which has been shown to attract SLFs, could reduce or eliminate the need for wintergreen oil if powered by the solar system.

Finally, the device could be optimized to reduce size, weight, and cost. A smaller design would be more practical for large-scale deployment across vineyard trellises. Future iterations could test a different shape instead of a cylinder with a hood, or move the motor to another section of the body to improve space efficiency. Reducing material use would lower production costs, decrease structural strain, and make installation easier.

Given the resources and scope of the class, most functional testing was completed. The prototype met the team’s success criteria, operated efficiently, and captured model SLFs. To strengthen the design for real-world use, future testing should be conducted in a controlled environment with live SLFs to quantify attraction and capture performance.

---

## Bill of Materials
<a id="bill-of-materials"></a>

| Item | Price | Quantity |
|---|---:|---:|
| Drive shaft | $1.15 | 1 |
| Casing (RPL) | $19.32 | 1 |
| Rotor Disc 1 (RPL) | $1.93 | 1 |
| Stator Disc (RPL) | $2.85 | 1 |
| Rotors (RPL) | $0.31 | 1 |
| Stators (RPL) | $0.31 | 1 |
| Component 11 (RPL) | $0.90 | 1 |
| Component 12 (RPL) | $3.43 | 1 |
| Component 13 (RPL) | $4.34 | 1 |
| Component 14 (RPL) | $5.66 | 1 |
| Component 16 (RPL) | $6.74 | 1 |
| Component 18 (RPL) | $0.88 | 1 |
| Geared DC Motor 6V | $8.29 | 1 |
| Arduino Uno R3 | $27.60 | 1 |
| NPN Transistor (BJT) | $8.99 | 1 |
| Battery, 4xAA | Provided | 1 |
| Battery, 1x9V | $6.46 | 1 |
| Resistor Variety Pack | $4.99 | 1 |
| Wires and heat shrink tubing | $11.99 | 1 |
| Female/Male Header Crimps | $9.69 | 1 |
| Slide Switch | $4.99 | 1 |
| Wintergreen oil | $7.99 | 1 |
| Sponge | $2.99 | 1 |
| Green LED | $5.99 | 1 |
| 9V barrel jack | $3.97 | 1 |
| Diode | $4.03 | 1 |

**Total Cost:** **$155.79**

---

## References
<a id="references"></a>

Pinto, Allan F., et al. “Assessing the Potential Economic Impacts of Spotted Lanternfly (Hemiptera: Fulgoridae) Infestations on Grape Production in New York State.” *Journal of Integrated Pest Management*, vol. 16, no. 1, 2025.

“Spotted Lanternfly Reveals a Potential Weakness.” *USDA*, 10 Jan. 2025.

Williams, Larry E. “Modelling Water Use of Grapevine.” *HortScience*, vol. 28, no. 5, May 1993.
