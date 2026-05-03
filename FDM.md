[![LiaScript](https://github.com/LiaScript/LiaScript/blob/ffe73bc438077d2d5a2e6a755ffe1e445449f9d5/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/AetherHey008/FDM-Presentation_ENGCSRB/refs/heads/main/FDM.md)

#### FDM Printing

![](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMDlydjQ5ZjA3ZTAyMmFtc3I2MWgxYmdnOW9mb3hmdzlxb29saTQxbSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/NPDydge3v69UIYtVCe/giphy.gif)<!--style="width: 100%; max-width: 80%;"-->

---

### What is 3D printing in general?

3D printing describes the process of creating physical objects from digital 3D models.

Unlike traditional manufacturing methods, which remove material (e.g. milling),  
3D printing follows an additive approach:

**Material is deposited layer by layer until the final geometry is achieved.**

This enables the production of complex internal structures, overhangs,  
and geometries that would be difficult or impossible to manufacture otherwise.

Also referred to as Additive Manufacturing
Widely used in prototyping, medicine, aerospace
---



!?[](https://https://www.youtube.com/watch?v=EF8CNR-gcXo)<!--style="width: 100%; max-width: 80%;"-->
---



### Types of 3D Printers

| Method | Process | Strengths | Limitations |
|--------|--------|----------|-------------|
| Resin (SLA/DLP) | UV light cures liquid resin layer by layer | Very high detail, smooth surfaces | Requires post-processing, resin handling |
| Powder (SLS/MJF) | Laser fuses powder into solid layers | Strong parts, no support structures | Expensive systems and materials |
| Filament (FDM/FFF) | Heated nozzle extrudes molten filament | Low cost, simple operation | Visible layers, lower precision |

**Observation:**  
Different technologies optimize for different goals:  
detail (SLA), strength (SLS), or accessibility (FDM).

---
<br>
<br>
|SLA Printer|
Formlabs Form 4
![](https://formlabs.com/_next/image/?url=https%3A%2F%2Fformlabs-media.formlabs.com%2Ffiler_public_thumbnails%2Ffiler_public%2F20%2F5d%2F205d8a5a-3296-4581-9ea9-d2378bcd7abb%2Fformlabs_f4_persp_cover_closed_eng_light_ik_240321_store.png__1354x0_subsampling-2.png&w=3840&q=75)

|SLS Printer|
 AFS LaserCore 5300 Printer
![](https://www.3dnatives.com/en/wp-content/uploads/sites/2/2024/07/AFS-LaserCore-5300.jpg)

|FDM Printer|
Elegoo Centauri Carbon
![](https://3d.nice-cdn.com/upload/image/product/large/default/elegoo-centauri-carbon-1-st-816923-de.jpg)

### FDM Printers in Detail



![](https://3d.nice-cdn.com/upload/image/product/large/default/elegoo-centauri-carbon-1-st-816923-de.jpg)


---

FDM (Fused Deposition Modeling) constructs objects  
by depositing molten thermoplastic in a controlled manner.

The process is discrete and layered, meaning the final object  
is composed of many individual cross-sections stacked vertically.



---

### Process Breakdown

![](https://upload.wikimedia.org/wikipedia/commons/3/3d/FDM_printing_diagram.png)<!--style="width: 100%; max-width: 500px;"-->

---

The FDM process can be understood as a repeated sequence of steps:

1. **Material extrusion**  
   The nozzle deposits molten plastic onto the build surface 
<br>
   ![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Extruder_lemio-en.svg/500px-Extruder_lemio-en.svg.png) 
<br>

---
2. **Path following (X/Y movement)**  
   The print head follows a predefined path for each layer  
<br>
   ![](https://airwolf3d.com/wp-content/uploads/2017/01/core-XY.gif)
<br>

---
3. **Layer completion**  
   A full 2D cross-section of the object is formed  

<br>
![](https://i.all3dp.com/workers/images/fit=scale-down,w=1200,h=675,quality=79,gravity=0.5x0.5,format=auto/wp-content/uploads/2021/07/22135217/5ucqu7ycjwh21.jpg)
<br>

---
4. **Layer stacking (Z movement)**  
   The system moves vertically and repeats the process  
<br>
![](https://media.giphy.com/media/tKrpJSggdryRdJLfus/giphy.gif)
<br>

---
### Core Components

---

1. Extruder

The extruder is responsible for feeding filament into the hotend  
with controlled force and speed.

It determines how much material is pushed into the nozzle.


Direct drive: motor mounted on print head (better control)
Bowden: motor mounted separately (lighter print head)


2. Hotend / Nozzle

The hotend heats the filament beyond its melting point  
and forces it through a small nozzle.

The nozzle diameter directly affects print resolution.

Standard nozzle size: 0.4 mm
Smaller nozzle = higher detail, longer print time

---

<br>
![](https://www.drdflo.com/assets/img/How-to-build-a-3d-printer/Anatomy-of-FFF-Extruder-01.png)<!--style="width: 100%; max-width: 400px;"-->
<br>


---

---

3. Build Plate

The build plate is the surface on which the object is printed.

It must provide sufficient adhesion during printing  
while still allowing easy removal afterward.

![](https://de.elegoo.com/cdn/shop/files/Dual-Sided-Build-Plate-Pack-for-Centauri-Carbon-and-Centauri-1.jpg?crop=center&v=1750937412&width=1220)<!--style="width: 100%; max-width: 400px;"-->


Heated beds reduce warping
Common surfaces: glass, PEI, textured sheets


---

4. Motion System (Axes & Stepper Motors)

The motion system controls precise positioning  
in three dimensions (X, Y, Z).

Stepper motors move the print head and/or build plate  
according to the G-code instructions.

![](https://m.media-amazon.com/images/I/61n4yD2-UjL.jpg)<!--style="width: 100%; max-width: 400px;"-->


||
|X/Y = horizontal movement|
|Z = vertical layer movement|
|Precision is typically within fractions of a millimeter|

---

### Advantages, Constraints and Risks

**Advantages**
- Low entry cost and widely available systems  
- Straightforward operation and maintenance  
- Suitable for rapid prototyping  

**Constraints**
- Limited resolution due to nozzle diameter and layer height  
- Mechanical strength is anisotropic (weaker between layers)  
- Surface finish often requires post-processing  


**Risk**

- toxic gases (ABS-printing)
- printfails

---
![](https://dms-discourse-static.s3.dualstack.us-east-1.amazonaws.com/optimized/2X/1/1e0889f0d3cb71fe1a1dc15a23bcda8cf78d4241_2_596x500.jpg)<!--style="width: 100%; max-width: 400px;"-->

### From Model to Print

A 3D model alone is not sufficient for printing.

Printers require **explicit movement and control instructions**.

This translation step is handled by a slicer.

---

![](https://preview.redd.it/benchy-spinning-360-gif-v0-94ql5pa87aif1.gif?width=1000&auto=webp&s=51a3c1d9a381b5cedf5dfea99afc62e8a2c2e928)<!--style="width: 50%; max-width: 400px%;"-->

---
---

### Slicer (Orca Slicer)

A slicer converts a continuous 3D geometry  
into a sequence of discrete layers and toolpaths.

This is where the abstract model becomes machine-readable.

---

### Internal Slicing Steps

- The model is intersected with horizontal planes  
- Each intersection defines a 2D contour (layer)  
- Toolpaths are generated for perimeters and infill  
- Process parameters are applied to each path  

The result is a fully specified manufacturing plan.

---

### Key Parameters and Their Impact

**Layer Height**  
Determines vertical resolution and print time  
→ smaller layers increase detail but require more time  

**Infill Density**  
Controls internal structure and strength  
→ higher infill increases strength and material usage  

**Temperature**  
Affects viscosity and layer bonding  
→ too low: weak adhesion, too high: stringing  

**Print Speed**  
Impacts precision and reliability  
→ higher speed reduces quality and increases error risk  

---

### Output: G-Code

The slicer produces a G-code file.

This file contains a sequential list of instructions  
that fully define the printing process.

---

### G-Code Structure

G-code is a line-based command language.

Each line represents a single instruction  
executed in order by the printer firmware.

---

### Example

```gcode
G28        ; Home all axes
G1 X50 Y50 ; Move to position
G1 Z0.2    ; Set layer height
G1 E10     ; Extrude filament
