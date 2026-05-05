[![LiaScript](https://github.com/LiaScript/LiaScript/blob/ffe73bc438077d2d5a2e6a755ffe1e445449f9d5/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/AetherHey008/FDM-Presentation_ENGCSRB/refs/heads/main/FDM-Presentation.md)

# <p style="text-align:center"> FDM Printing

![](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMDlydjQ5ZjA3ZTAyMmFtc3I2MWgxYmdnOW9mb3hmdzlxb29saTQxbSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/NPDydge3v69UIYtVCe/giphy.gif)<!--style="width: 100%; max-width: 80%;text-align: center;"-->

Matteo Poma</p>

---

### What is 3D Printing?

3D printing creates physical objects from digital models using an **additive approach** — material is deposited layer by layer.

- Also called **Additive Manufacturing**
- Used in prototyping, medicine, and aerospace
- Enables complex geometries impossible with traditional methods

---

## Types of 3D Printers

| Method | Process | Strengths | Limitations |
|--------|---------|-----------|-------------|
| Resin (SLA/DLP) | UV light cures liquid resin | High detail, smooth surfaces | Post-processing required |
| Powder (SLS/MJF) | Laser fuses powder layers | Strong parts, no supports | Expensive |
| Filament (FDM) | Heated nozzle extrudes plastic | Low cost, easy to use | Visible layers |

---

|SLA – Formlabs Form 4|SLS – AFS LaserCore 5300|FDM – Elegoo Centauri Carbon|
|![](https://formlabs.com/_next/image/?url=https%3A%2F%2Fformlabs-media.formlabs.com%2Ffiler_public_thumbnails%2Ffiler_public%2F20%2F5d%2F205d8a5a-3296-4581-9ea9-d2378bcd7abb%2Fformlabs_f4_persp_cover_closed_eng_light_ik_240321_store.png__1354x0_subsampling-2.png&w=3840&q=75)|![](https://www.3dnatives.com/en/wp-content/uploads/sites/2/2024/07/AFS-LaserCore-5300.jpg)|![](https://3d.nice-cdn.com/upload/image/product/large/default/elegoo-centauri-carbon-1-st-816923-de.jpg)|

---

### FDM in Detail

![](https://3d.nice-cdn.com/upload/image/product/large/default/elegoo-centauri-carbon-1-st-816923-de.jpg)

FDM builds objects by melting plastic filament and depositing it layer by layer onto a build platform.

**Key components:**

- **Extruder/Nozzle** – melts and deposits material
- **Build Plate** – print surface
- **Motion System** – controls X, Y, Z movement

---

### Process Breakdown

![](https://upload.wikimedia.org/wikipedia/commons/3/3d/FDM_printing_diagram.png)<!--style="width: 100%; max-width: 500px;"-->

1. **Extrusion** – Nozzle deposits molten plastic
2. **X/Y Movement** – Print head follows layer path
3. **Layer Completion** – Full 2D cross-section formed
4. **Z Movement** – System rises and repeats

---

### Core Components

**1. Extruder**
Feeds filament into the hotend with controlled force.

- **Direct drive** – motor on print head (better control)
- **Bowden** – motor separate (lighter head)

**2. Hotend / Nozzle**
Melts filament and extrudes it through a small opening.

- Standard nozzle: **0.4 mm**
- Smaller = more detail, longer print time

![](https://www.drdflo.com/assets/img/How-to-build-a-3d-printer/Anatomy-of-FFF-Extruder-01.png)<!--style="width: 100%; max-width: 400px;"-->

---

**3. Build Plate**
Surface where the object is printed — needs adhesion during print, easy release after.

![](https://de.elegoo.com/cdn/shop/files/Dual-Sided-Build-Plate-Pack-for-Centauri-Carbon-and-Centauri-1.jpg?crop=center&v=1750937412&width=1220)<!--style="width: 100%; max-width: 400px;"-->

- Heated beds reduce warping
- Common surfaces: glass, PEI, textured sheets

**4. Motion System**
Stepper motors move the print head precisely in X, Y, and Z axes.

- X/Y = horizontal layer path
- Z = vertical layer advance
- Precision within fractions of a millimeter

---

### Advantages, Constraints & Risks

**Advantages**
- Low cost, widely available
- Easy to operate and maintain
- Great for rapid prototyping

**Constraints**
- Limited resolution (nozzle diameter & layer height)
- Anisotropic strength (weaker between layers)
- Surface finish may need post-processing

**Risks**
- Toxic fumes (e.g. ABS printing)
- Print failures

![](https://dms-discourse-static.s3.dualstack.us-east-1.amazonaws.com/optimized/2X/1/1e0889f0d3cb71fe1a1dc15a23bcda8cf78d4241_2_596x500.jpg)<!--style="width: 100%; max-width: 400px;"-->

---

## From Model to Print

A 3D model must be translated into **machine instructions** before printing.

This is done by a **Slicer**.

![](https://preview.redd.it/benchy-spinning-360-gif-v0-94ql5pa87aif1.gif?width=1000&auto=webp&s=51a3c1d9a381b5cedf5dfea99afc62e8a2c2e928)<!--style="width: 50%; max-width: 400px;"-->

---

## Slicer (Orca Slicer)

Converts a 3D model into discrete layers and toolpaths the printer can execute.

!?[](https://www.youtube.com/watch?v=DVj4NW30TuM)

---

### Key Slicer Parameters

| Parameter | Effect |
|-----------|--------|
| **Layer Height** | Smaller = more detail, longer print |
| **Infill Density** | Higher = stronger, more material |
| **Temperature** | Too low: weak bonds — too high: stringing |
| **Print Speed** | Higher = faster, but lower quality |

---

## G-code
** What is G-code?**

A standardized command language for machines like 3D printers and CNC mills.

Each line = one command + optional parameters (position, speed, temperature).

---

### Common G-code Commands

| Command | Meaning |
|---------|---------|
| `G0` / `G1` | Move toolhead (G1 = controlled/printing move) |
| `G28` | Home all axes |
| `G90` / `G91` | Absolute / Relative positioning |
| `G92` | Set current position |
| `G29` | Auto bed leveling |

---

### Common M-code Commands

| Command | Meaning |
|---------|---------|
| `M104` / `M109` | Set nozzle temp (M109 waits) |
| `M140` / `M190` | Set bed temp (M190 waits) |
| `M106` / `M107` | Fan on / off |
| `M220` / `M221` | Speed / flow multiplier |
| `M204` | Set acceleration |
| `M112` | Emergency stop |

---

### Common Parameters

| Parameter | Meaning |
|-----------|---------|
| `X`, `Y`, `Z` | Position coordinates |
| `E` | Extrusion amount |
| `F` | Feedrate (speed) |
| `S` | Value (temp, fan speed, etc.) |

---

### Example G-code

```gcode "full-example"
; EXECUTABLE_BLOCK_START
EXCLUDE_OBJECT_DEFINE NAME=Cannonade_Cogfort.stl_id_0_copy_0 CENTER=128.5,128.5 POLYGON=[[72.73,106.132],[72.742,105.964],[72.778,105.832],[73.486,104.212],[73.63,104.044],[74.686,103.132],[94.474,88.216],[94.546,88.18],[114.082,84.952],[129.946,84.952],[169.354,88.192],[169.534,88.216],[169.582,88.24],[169.69,88.324],[170.182,88.84],[170.314,89.032],[170.35,89.128],[184.234,126.784],[184.246,126.868],[184.27,127.228],[184.258,131.488],[184.246,133.12],[184.21,133.24],[170.374,170.98],[170.338,171.076],[170.29,171.16],[169.798,171.652],[169.642,171.808],[169.534,171.856],[168.886,171.88],[158.458,172.048],[157.63,172.048],[94.63,171.856],[94.534,171.844],[94.45,171.808],[94.366,171.736],[93.97,171.388],[93.778,171.208],[93.766,171.196],[93.694,171.1],[77.434,129.472],[77.386,129.34],[73.882,116.896],[72.73,106.132]]
M106 S0
M106 P2 S0
;TYPE:Custom
;;===== date: 20240520 =====================
;printer_model:Elegoo Centauri Carbon
;initial_filament:PLA
;curr_bed_type:Textured PEI Plate
M400
M220 S100
M221 S100
M104 S140
M140 S60
G90
G28
M729
M106 P2 S255
M190 S60
M106 P2 S0

M106 P3 S255

M204 S5000

G1 X128.5 Y-1.2 F20000
G1 Z0.3 F900
M109 S220
M83
G92 E0
G1 F1280 
G1 X-1.2 E10.156
G1 Y98.8 E7.934
G1 X-0.5 Y100 E0.1
G1 Y-0.3 E7.934
G1 X78.5 E6.284
G1 F256 
G1 X98.5 E2
G1 F1280 
G1 X118.5 E2
G1 F256 
G1 X138.5 E2
G1 F1280 
G1 X158.5 E2
G1 F1280 
G1 X178.5 E2
;End PA test.
```


---

## Summary

- FDM builds objects **layer by layer** using melted plastic filament
- Simple, affordable, and widely used for **prototyping**
- Key steps: **Model → Slicer → G-code → Print**
- Trade-offs in precision and surface quality, but highly accessible

**ANY QUESTIONS?**
