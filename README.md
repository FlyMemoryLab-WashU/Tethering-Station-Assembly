# Instructions for building the inexpensive tethering station

---

### Table of Contents
- [1. Prepare the needed parts for assemble](#1-laser-cut-acrylic-parts)
- [2. Assemble the main acrylic structure](#2-acrylic-assembly)
- [3. 3D Printed Parts](#3-3d-printed-parts)
- [4. Chiller Assembly](#4-chiller-assembly)
- [5. Micro-Manipulator Assembly](#5-micro-manipulator-assembly)
- [6. Required Parts List](#6-required-parts-list)

  
## Assembly Steps

### 1) Prepare all parts

#### 1.1 Verify purchasable items (BOM)
- Confirm you have all **purchasable components** listed in the **Bill of Materials (BOM)** table.
- Purchase any missing items before starting the build.

#### 1.2 Prepare custom acrylic parts
- Obtain the acrylic-sheet parts by either:
  - laser-cutting the acrylic sheets yourself, or
  - ordering laser-cut parts from a service (e.g., Ponoko).
- **Check acrylic thickness before cutting/ordering.** The SVG filenames indicate the required thickness:
  - **1.5 mm (1/16")**
  - **6 mm (1/4")**
- **Cut paths only:** all paths in the SVG files are intended to be **cut**, not engraved.

#### 1.3 Tap threads in the baseplate
- Tap **M3 threads** into the baseplate holes used to mount the micromanipulator.

#### 1.4 Prepare 3D-printed parts
- Obtain the 3D-printed parts by either:
  - printing them yourself, or
  - ordering them from a service (e.g., Craftcloud).
- Recommended filament:
  - **PLA** (works well for most uses)
  - **ASA** (recommended if you need improved UV resistance)
- Suggested print settings:
  - **0.2 mm layer height**
  - **No supports**
- **Mini-V clamp:** insert **M3 nuts** into both slots.

---

### 2) Assemble the acrylic frame
- Assemble the main structure using the acrylic parts, following the render in **Figure 5**.
- Fasten all acrylic joints with **cyanoacrylate adhesive** (super glue), as shown in **Figure 5**.

#### Optional: add rubber feet
For better grip between the baseplate and the table, attach **four rubber feet** under the baseplate—**one at each corner**.

---

### 3) Assemble the chiller

#### 3.1 Build the W1209 temperature controller
- Assemble the **W1209 temperature controller**.
- If your unit includes an acrylic housing, assemble the housing first.

> **Wiring safety note**
>
> Do **not** splice wires by twisting metal-on-metal only. Poor splices can overheat under load.
> Use one of the following:
> - solder + heat-shrink, or
> - proper connectors (e.g., crimp connectors or WAGO lever nuts).

#### 3.2 Wire the temperature controller (recommended order)
Prepare:
- one **3" red wire** (cut + strip ends)
- one **10" black wire** (cut + strip ends)
- **12 V power supply**
- **female barrel connector**
- **rocker switch**

Wire as follows:
1. Use the **3" red wire** to connect terminals **K1 → 12V** on the W1209.
2. Connect one end of the **10" black wire** to **GND** on the W1209.
3. Connect the other end of the **10" black wire** to the **negative (−)** terminal of the **female barrel connector**.
4. Connect the **black wire** of the **rocker switch** to **12V** on the W1209.
5. Connect the **red wire** of the **rocker switch** to the **positive (+)** terminal of the **female barrel connector**.

**Chiller load wiring (Peltier + fan assembly):**
- **Red wires → K0**
- **Black wires → GND**

You can wire the chiller load either **now** or **after** mounting the chiller to the acrylic structure.

#### 3.3 Prepare and mount the aluminum T-bar
1. Cut a **40 mm** section of the **aluminum T-bar** (a bandsaw works well).
2. Apply **thermal paste** to the bottom face of the T-bar (orientation as in **Figure 1A**).
3. Place the **NTC temperature probe** so it touches **both**:
   - the rim of the T-bar, and
   - the cold plate  
   Add thermal paste to thermally couple the probe to both surfaces.
4. Secure the T-bar using **thermal tape** (use **4 × 10 mm** strips) as shown in **Figure 1A**.
   - You do **not** need to remove the blue liner from the tape after applying it.

#### 3.4 Seat the chiller on the acrylic frame
- Place the chiller into its seat as shown in **Figure 1A**.
- Optionally use **cyanoacrylate adhesive** (super glue) for additional fastening.

---

### 4) Mount the micromanipulator
1. Place the micromanipulator on the acrylic baseplate **with the 6 mm raising platform underneath**.
2. To access the screw mounts:
   - Slide the lowest platform to an **edge position** to expose the screw holes on the opposite side.
3. Insert **M3 × 12** screws and fasten the micromanipulator into the baseplate.
4. Move the platform to the other edge position and repeat to install the remaining screws.

---

### 5) Install the thread adapter and Mini-V clamp

1. Screw your chosen **thread adapter** into the top surface of the micromanipulator.
2. Wrap **one layer** of **PTFE (thread seal) tape** or **electrical tape** around the exposed threads to add friction (prevents the clamp from rotating freely).
3. Attach the **Mini-V clamp** above the thread adapter.

#### Notes by clamp version

**3D-printed version (shown in Figure 1A)**
- The “thread adapter” is an **M3 × 36** threaded rod.
  - We made this by cutting an **M3 × 40** screw down to **36 mm** using a rotary tool + cutoff wheel (other methods are fine).
- Fasten the rod by:
  1. threading it into the micromanipulator platform hole closest to the T-bar, then
  2. adding a **washer + nut** to lock it in place.

**Thorlabs-parts version**
- You may need **M3 standoffs** to reach the height of the aluminum T-bar apex.
- This was not tested; an M3 standoff kit is included in the BOM as an option.

---

### 6) Install the fly-holding rod and fly holder
1. Insert the appropriate **thumb screw** into the top of the Mini-V clamp (type depends on your clamp choice).
2. Insert the **fly-holding rod** (Thorlabs or 3D-printed) into the Mini-V clamp and secure it with the thumb screw.
3. Attach the acrylic fly holder to the rod using one of the following:
   - **M2.5 screw + nut**, or
   - **#2-56 screw + nut**
4. Use the small hole at one end of the fly-holding rod for the fly holder fastener.

---

### 7) Power on and set the chiller temperature

1. Plug the **12 V power supply** into the **female barrel connector**.
2. Turn on the **rocker switch** when you are ready to cool.

#### Recommended temperature setpoint
- Target: keep the **cold plate ~0 °C**.
- The NTC probe may not report the cold-plate temperature accurately.
- Using an IR camera, we found that setting the controller to **+10 °C** produced the desired cold-plate temperature (~0 °C).

#### How to set the temperature on the W1209
1. **Click** (do not long-press) the **SET** button until the display flashes.
2. Use **+** and **−** to adjust the set temperature.
3. Wait briefly for the value to be accepted (flashing stops).


## 6. Required Parts List

| Part Name | SKU / Part Number | Quantity | Notes | Link | Description |
| :--- | :--- | :---: | :--- | :--- | :--- |
| **Arduino Uno R3** | `A000066` | 1 | The main microcontroller. |
| **DHT22 Sensor** | `AM2302` | 1 | For temperature and humidity. |
| **M3 Screws** | `HW-102` | 8 | `12mm` length. |

* [cite_start]Fasten the linear stage to the 3D printed adapter piece using `M3 8mm screws` and `M3 nuts`[cite: 1].
* [cite_start]Fasten the 3D printed adapter to the **6mm-thick** baseplate using `M6 12mm screws` and `M6 nuts`[cite: 1].
* On the thread adapter, wrap one layer of electrical tape around the thread. [cite_start]This provides resistance and prevents unwanted rotation[cite: 1].
