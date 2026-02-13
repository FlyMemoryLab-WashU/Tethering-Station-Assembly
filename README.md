# Instructions for Building the Inexpensive Tethering Station

<div align="center">
  <img width="483" height="445" alt="Figure 1" src="https://github.com/user-attachments/assets/d91770e0-0f53-46a8-992f-4401d05d4d97" />
  <br>
  <em><strong>Figure 1:</strong> Fly tethering station.</em>
</div>

---

## 📑 Table of Contents
1. [Prepare all needed parts](#1-prepare-all-needed-parts)
2. [Assemble the acrylic frame](#2-assemble-the-acrylic-frame)
3. [Assemble the chiller](#3-assemble-the-chiller)
4. [Mount the micromanipulator](#4-mount-the-micromanipulator)
5. [Install the thread adapter and Mini-V clamp](#5-install-the-thread-adapter-and-mini-v-clamp)
6. [Install the fly-holding rod and fly holder](#6-install-the-fly-holding-rod-and-fly-holder)
7. [Power on and set the chiller temperature](#7-power-on-and-set-the-chiller-temperature)
8. [Required Parts List (BOM)](#8-required-parts-list-bom)

---

## 🛠️ Assembly Steps

### 1. Prepare all needed parts

#### 1.1 Verify purchasable items
- [ ] Confirm you have all **purchasable components** listed in the [Required Parts List](#8-required-parts-list-bom) below.
- [ ] Purchase any missing items before starting the build.

#### 1.2 Prepare custom acrylic parts
Obtain the acrylic-sheet parts by either laser-cutting the acrylic sheets yourself or ordering them from a service (e.g., Ponoko). 

> **Note on Acrylic Thickness:** Check thickness before cutting/ordering. The SVG filenames indicate the required thickness (**1.5 mm / 1/16"** or **6 mm / 1/4"**). All paths in the SVG files are intended to be **cut**, not engraved.

**Required custom acrylics:**
- [ ] **Acrylic fly holder**
  <img width="289" height="376" alt="Figure 2" src="https://github.com/user-attachments/assets/bc54cf4e-6676-4bef-9208-de54c92412dd" />
  <br><em><strong>Figure 2:</strong> Acrylic fly mount, 1.5mm (1/16”) thickness.</em>

- [ ] **Acrylic assembly for the mounting station**
  <img width="1004" height="773" alt="Figure 3" src="https://github.com/user-attachments/assets/654cf831-6301-422c-8e93-609468d172ba" />
  <br><em><strong>Figure 3:</strong> CAD rendering of the mounting station's acrylic assembly, designed in FreeCAD.</em>

#### 1.3 Tap threads in the baseplate
- [ ] Tap **M3 threads** into the baseplate holes used to mount the micromanipulator.

#### 1.4 Prepare 3D-printed parts
Obtain the 3D-printed parts by printing them yourself or using a service (e.g., Craftcloud). 
* **Recommended filament:** **PLA** (general use) or **ASA** (for UV resistance).
* **Suggested settings:** 0.2 mm layer height, NO supports.
- [ ] Print all required parts.
- [ ] **Mini-V clamp:** Insert **M3 nuts** into both slots.

---

### 2. Assemble the acrylic frame

- [ ] Assemble the main structure using the acrylic parts, following the render in **Figure 5** *(Ensure Figure 5 is uploaded to your repo)*.
- [ ] Fasten all acrylic joints with **cyanoacrylate adhesive** (super glue).

> **💡 Optional:** For better grip between the baseplate and the table, attach **four rubber feet** under the baseplate—one at each corner.

---

### 3. Assemble the chiller

#### 3.1 Build the W1209 temperature controller
- [ ] Assemble the **W1209 temperature controller**. (If your unit includes an acrylic housing, assemble the housing first).

> **⚠️ Wiring Safety Note**
> Do **not** splice wires by twisting metal-on-metal only. Poor splices can overheat under load. Use one of the following:
> * Solder + heat-shrink
> * Proper connectors (e.g., crimp connectors or WAGO lever nuts)

#### 3.2 Wire the temperature controller 


[Image of W1209 temperature controller wiring diagram]


**Prepare:**
- [ ] 1x **3" red wire** (cut + strip ends)
- [ ] 1x **10" black wire** (cut + strip ends)
- [ ] **12V power supply**, **female barrel connector**, and **rocker switch**

**Wiring sequence:**
- [ ] **a.** Connect the **3" red wire** from terminals **K1** → **12V** on the W1209.
- [ ] **b.** Connect one end of the **10" black wire** to **GND** on the W1209.
- [ ] **c.** Connect the other end of the **10" black wire** to the **negative (−)** terminal of the female barrel connector.
- [ ] **d.** Connect the **black wire** of the rocker switch to **12V** on the W1209.
- [ ] **e.** Connect the **red wire** of the rocker switch to the **positive (+)** terminal of the female barrel connector.

**Chiller load wiring (Peltier + fan assembly):**
- [ ] **Red wires** → **K0**
- [ ] **Black wires** → **GND**
*(Note: You can wire the chiller load now or after mounting it to the acrylic structure).*

#### 3.3 Prepare and mount the aluminum T-bar
- [ ] **a.** Cut a **40 mm** section of the aluminum T-bar (a bandsaw works well).
- [ ] **b.** Apply **thermal paste** to the bottom face of the T-bar (orientation as in **Figure 1A**).
- [ ] **c.** Place the **NTC temperature probe** so it touches **both** the rim of the T-bar and the cold plate. Add thermal paste to thermally couple the probe to both surfaces.
- [ ] **d.** Secure the T-bar using **thermal tape** (use 4 × 10 mm strips) as shown in **Figure 1A**. *(Note: Do not remove the blue liner from the tape after applying it).*

#### 3.4 Seat the chiller on the acrylic frame
- [ ] Place the chiller into its seat.
- [ ] *(Optional)* Use cyanoacrylate adhesive (super glue) for additional fastening.

---

### 4. Mount the micromanipulator

- [ ] **a.** Place the micromanipulator on the acrylic baseplate **with the 6 mm raising platform underneath**.
- [ ] **b.** Slide the lowest platform to an **edge position** to expose the screw holes on the opposite side.
- [ ] **c.** Insert **M3 × 12 mm** screws and fasten the micromanipulator into the baseplate.
- [ ] **d.** Move the platform to the other edge position and repeat to install the remaining screws.

---

### 5. Install the thread adapter and Mini-V clamp

- [ ] **a.** Screw your chosen **thread adapter** into the top surface of the micromanipulator.
- [ ] **b.** Wrap **one layer** of PTFE tape or electrical tape around the exposed threads to add friction.
- [ ] **c.** Attach the **Mini-V clamp** above the thread adapter.

> **Notes by clamp version:**
> * **3D-printed version:** The “thread adapter” is an M3 × 36 threaded rod (fabricated by cutting an M3 × 40 screw down). Fasten the rod by threading it into the micromanipulator platform hole closest to the T-bar, then add a washer + nut to lock it.
> * **Thorlabs-parts version:** You may need M3 standoffs to reach the height of the aluminum T-bar apex.

---

### 6. Install the fly-holding rod and fly holder

- [ ] **a.** Insert the appropriate **thumb screw** into the top of the Mini-V clamp.
- [ ] **b.** Insert the **fly-holding rod** (Thorlabs or 3D-printed) into the Mini-V clamp and secure it with the thumb screw.
- [ ] **c.** Attach the acrylic fly holder to the rod using an **M2.5 screw + nut** or a **#2-56 screw + nut**.
- [ ] **d.** Use the small hole at one end of the fly-holding rod for the fly holder fastener.

---

### 7. Power on and set the chiller temperature

- [ ] **a.** Plug the **12V power supply** into the female barrel connector.
- [ ] **b.** Turn on the **rocker switch** when you are ready to cool.

#### Recommended temperature setpoint
Target keeping the **cold plate at ~0 °C**. Because the NTC probe may not report the cold-plate temperature perfectly, setting the controller to **+10 °C** generally produces a cold-plate temperature of ~0 °C.

**How to set the W1209:**
1. **Click** (do not long-press) the **SET** button until the display flashes.
2. Use **+** and **−** to adjust the set temperature.
3. Wait briefly for the value to be accepted (flashing stops).

---

## 📦 8. Required Parts List (BOM)

### Main Components

| Name | Qty | Description | Link |
|---|:---:|---|---|
| **Tap Wrench Set** | 1 | Mesee 6 Pcs Tap Wrench Tool Set (M3–M8) | [Link](https://a.co/d/hpTYyof) |
| **Super Glue** | 1 | Loctite Professional Liquid, 20 g | [Link](https://a.co/d/eSluuwc) |
| **Temp Controller** | 1 | HiLetgo W1209 (12V) Digital Temp Controller | [Link](https://a.co/d/bQPwmGg) |
| **WAGO Splices** | 5 | Push-in butt splice connector, 12–24 AWG | [Link](https://www.digikey.com/short/qq5hc085) |
| **Hook-up Wire** | 1 | 22 AWG, 25 ft (Black & Red needed) | [Black](https://www.digikey.com/short/qm3t1whb) / [Red](https://www.digikey.com/short/whnmh5cv) |
| **Rocker Switch** | 1 | SPST, 20A (AC) 125V, panel mount | [Link](https://www.digikey.com/short/8pzjtrjv) |
| **Thermal Tape** | 1 | Double-sided thermal adhesive (10 mm) | [Link](https://a.co/d/jgPTIG2) |
| **Thermal Paste** | 1 | Thermal silicone compound, 1 g syringe | [Link](https://www.digikey.com/short/015wb8zm) |
| **Cooler** | 1 | Direct-to-air thermoelectric assembly | [Link](https://www.digikey.com/short/zvf0w91p) |
| **Power Supply** | 1 | 12V 8A (96W) AC/DC power adapter | [Link](https://a.co/d/hwq6SQs) |
| **Micro-Manipulator**| 1 | XYZ axis manual precision linear stage | [Link](https://a.co/d/8RHpoLn) |
| **Aluminum T-Bar** | 1 | 6061 T-bar, 1/2" H × 1" W, 1/8" wall (Cut to 40mm) | [Link](https://www.mcmaster.com/1668T72-1668T722/) |
| **Plate-Holding Rod**| 1 | ER90C - 90° "T" Extension *(Thorlabs or 3D print)*| [Link](https://www.thorlabs.com/thorproduct.cfm?partnumber=ER90C) |
| **Cage Rod** | 1 | ER2 - Cage Assembly Rod, Ø6 mm | [Link](https://www.thorlabs.com/thorproduct.cfm?partnumber=ER2) |
| **Electrical Tape** | 1 | 3/4" wide, 60 ft, black | [McMaster](https://www.mcmaster.com/7619A11/) / [DigiKey](https://www.digikey.com/short/hzwqm2b5) |
| **PTFE Seal Tape** | 1 | Plumber’s tape, 1/2" × 520" | [Link](https://a.co/d/2TIa52S) |
| **Bumper Feet** *(Opt)*| 4 | Square tapered polyurethane bumper feet | [Link](https://www.digikey.com/short/tmd9vchq) |

### Clamp Options (Choose One)

**Option A: Imperial (8-32)**
| Name | Qty | Description | Link |
|---|:---:|---|---|
| **Thumb Screw** | 1 | #8-32 hex head, nylon | [Link](https://www.digikey.com/short/10z84wm7) |
| **Thread Adapter** | 1 | Male hex thread adapter, 8-32 to M3 × 0.5 | [Link](https://www.mcmaster.com/91091A527/) |
| **Clamp** | 1 | VH1 - Miniature V-Clamp, 8-32 tapped | [Link](https://www.thorlabs.com/thorproduct.cfm?partnumber=VH1) |

**Option B: Metric (M4)**
| Name | Qty | Description | Link |
|---|:---:|---|---|
| **Thumb Screw** | 1 | #8-32 hex head, nylon *(Swap for metric if preferred)*| [Link](https://www.digikey.com/short/10z84wm7) |
| **Thread Adapter** | 1 | Male hex thread adapter, M3 × 0.5 to M4 × 0.7| [Link](https://www.mcmaster.com/93047A106/) |
| **Clamp** | 1 | VH1/M - Miniature V-Clamp, M4 tapped | [Link](https://www.thorlabs.com/thorproduct.cfm?partnumber=VH1/M) |

**Option C: Metric (3D-Printed Clamp)**
| Name | Qty | Description | Link |
|---|:---:|---|---|
| **Thumb Screw** | 1 | Knurled thumb screws, M3 × 20 | [Link](https://a.co/d/elruBuP) |
| **Thread Adapter** | 1 | M3 × 36 threaded rod | *(Fabricate from M3x40)* |

*Optional for all clamp versions: [M3 Standoff Kit](https://a.co/d/eljB6fC) for height tuning.*

### Fasteners

| Name | Qty | Description | Link |
|---|:---:|---|---|
| **M3 × 12 mm Screws**| 1 | 316 stainless button head hex drive | [Link](https://www.mcmaster.com/94500A264/) |
| **M3 Nuts** | 1 | Zinc-plated steel hex nut | [Link](https://www.mcmaster.com/90591A121/) |
| **M3 Washers** | 1 | 18-8 stainless washer | [Link](https://www.mcmaster.com/93475A210/) |
| **#2-56 Screw** | 1 | Pan head slotted drive nylon screw | [Link](https://www.digikey.com/short/0jq8jp8r) |
| **#2-56 Nut** | 1 | Hex nut, nylon | [Link](https://www.digikey.com/short/2qt794vw) |

*Alternative to individual M3 parts: [M3 Fastener Assortment Kit](https://a.co/d/aGirgUi).*

### Acrylic Sheets (If laser cutting in-house)

| Name | Qty | Description | Link |
|---|:---:|---|---|
| **1.5 mm Sheet** | 1 | Clear acrylic sheet, 12" × 12" × 1/16" | [Link](https://www.mcmaster.com/8589K11/) |
| **6 mm Sheet** | 1 | Clear acrylic sheet, 12" × 12" × 1/4" | [Link](https://www.mcmaster.com/8589K81/) |
