# Instructions for building the inexpensive tethering station

---

### Table of Contents
- [1. Prepare the needed parts for assemble](#1-laser-cut-acrylic-parts)
- [2. Acrylic Assembly](#2-acrylic-assembly)
- [3. 3D Printed Parts](#3-3d-printed-parts)
- [4. Chiller Assembly](#4-chiller-assembly)
- [5. Micro-Manipulator Assembly](#5-micro-manipulator-assembly)
- [6. Required Parts List](#6-required-parts-list)

  
## 1. Prepare the needed parts for assemble

Before starting the assembly, make sure all parts and tools are ready.

### 1) Gather purchasable parts (BOM)
- Check that you have all items listed in the **Bill of Materials (BOM)** table.
- If anything is missing, purchase it before proceeding.

### 2) Prepare custom acrylic parts
- Obtain the custom acrylic-sheet parts by either:
  - laser-cutting the acrylic sheets yourself, or
  - ordering laser-cut parts from a service (e.g., Ponoko).
- **Confirm acrylic thickness before cutting/ordering.** The SVG filenames indicate the required thickness:
  - **1.5 mm (1/16")**
  - **6 mm (1/4")**
- **Cut paths only:** all paths in the SVG files are intended to be **cut**, not engraved.

### 3) Tap threads in the baseplate
- Tap **M3 threads** into the baseplate at the holes used to mount the micromanipulator.

### 4) Prepare 3D-printed parts
- Obtain the 3D-printed parts by either:
  - printing them yourself, or
  - ordering prints from a service (e.g., Craftcloud).
- Recommended filament:
  - **PLA** (works well for most uses)
  - **ASA** (recommended if you need improved UV resistance)
- Suggested print settings:
  - **0.2 mm layer height**
  - **No supports**
- **Mini-V clamp:** insert **M3 nuts** into both slots.


---

## 2. Acrylic Assembly

[cite_start]To assemble the main acrylic frame, please refer to the FreeCAD render in Figure 6 for guidance on how the parts fit together[cite: 1].

* [cite_start]Use `M3 20mm screws`, `M3 nuts`, and `M3 washers` to fasten the acrylic pieces together[cite: 1].
* [cite_start]Attach the 4 rubber feet to the underside of the base plate, placing one at each corner[cite: 1].

_Figure 6: Assembly Render_
![Placeholder for Figure 6](https://via.placeholder.com/400x300.png/cccccc/000000?Text=Figure+6+--+Assembly+Render)

---

## 3. 3D Printed Parts

The smaller components should be 3D printed. [cite_start]You can print these locally or use an online service like [Craftcloud](https://craftcloud3d.com)[cite: 1].

* [cite_start]**Material:** Standard **PLA** plastic works well[cite: 1]. [cite_start]If there is concern about the nearby UV lamp, a UV-resistant alternative is **ASA** plastic[cite: 1].
* **Printing Settings:**
    * [cite_start]No supports are needed for these parts[cite: 1].
    * [cite_start]A brim is recommended for better bed adhesion[cite: 1].
    * [cite_start]The parts have been tested with a `0.2mm` layer thickness[cite: 1].
* [cite_start]**Mini V-Clamp Assembly:** Before use, insert an `M3 Nut` into both slots on the mini v-clamp part[cite: 1].

---

## 4. Chiller Assembly

[cite_start]The chiller component follows the instructions from the Reiser Lab's Component Designs website[cite: 1].

* [cite_start]**Primary Instructions:** Follow the guide available here: [Reiser Lab Inexpensive Treadmill Chiller](https://reiserlab.github.io/Component-Designs/how-to-build-inexpensive-treadmill#tethering-station-chiller)[cite: 1].
    * [cite_start]Focus on sections **4.3.2**, **4.3.3**, **4.3.4**, and **4.3.6**[cite: 1].
* **Modifications for this Build:**
    * [cite_start]The rocker switch should be inserted within the power supply circuit[cite: 1].
    * Instead of the PLA "sarcophagus" described on the website, this build uses an **aluminum T-bar**. [cite_start]You will need to cut the T-bar to a **40mm** length[cite: 1].
    * To fasten the T-bar, first apply thermal paste to its underside. [cite_start]Then, use thermal tape to cover the upper side and secure it in place[cite: 1].

---

## 5. Micro-Manipulator Assembly

The final step is to assemble the micro-manipulator stage.

## 6. Required Parts List

| Part Name | SKU / Part Number | Quantity | Notes | Link | Description |
| :--- | :--- | :---: | :--- | :--- | :--- |
| **Arduino Uno R3** | `A000066` | 1 | The main microcontroller. |
| **DHT22 Sensor** | `AM2302` | 1 | For temperature and humidity. |
| **M3 Screws** | `HW-102` | 8 | `12mm` length. |

* [cite_start]Fasten the linear stage to the 3D printed adapter piece using `M3 8mm screws` and `M3 nuts`[cite: 1].
* [cite_start]Fasten the 3D printed adapter to the **6mm-thick** baseplate using `M6 12mm screws` and `M6 nuts`[cite: 1].
* On the thread adapter, wrap one layer of electrical tape around the thread. [cite_start]This provides resistance and prevents unwanted rotation[cite: 1].
