# TC40 Tripod Caster Adapter (FreeCAD Project)

This project provides a modular, 3D-printable collar and base-plate adapter that attaches removable castor wheels to the **ZWO TC40 tripod**, used with a **Celestron EdgeHD 9.25** or similar astrophotography rig. The goal is to make rolling the fully-built telescope in and out of observing position easier, while maintaining rigidity and vibration control once the wheels are removed and imaging begins.

---

## ✨ Features

- Split-collar design with M2 keeper bolt (no scratching of carbon-fiber tripod legs)
- Spacer seat that registers on the TC40 factory end-piece to eliminate vertical play
- Remove-when-not-needed wheel system (best stability for long-exposure imaging)
- Fully parametric using a FreeCAD Spreadsheet — adapt to different wheels in minutes
- Printable on consumer FDM printers (PLA+, PETG, ASA, ABS)

---

## 📌 Parametric Spreadsheet (FreeCAD)

> **IMPORTANT:**  
> The **Base Plate** and **Bolt Pattern** parameters define the *physical bolt layout and footprint of the castor wheel you are using*. These values **MUST be updated** to match your specific castor hardware.

| Parameter | Value | Description |
|---|---|---|
| **tube_ID** | 41 mm | Inner diameter of main adapter tube |
| **tube_wall** | 4.5 mm | Tube wall thickness |
| **tube_len** | 50 mm | Tube length |
| **leg_angle_deg** | 27° | Tripod leg angle |
| **tube_OD** | `tube_ID + 2 × tube_wall` | Derived outer diameter |

**Base Plate (modify for your castor wheel)**

| Parameter | Value | Description |
|---|---|---|
| **base_x** | 82 mm | Base plate X dimension |
| **base_y** | 68 mm | Base plate Y dimension |
| **base_thick** | 12 mm | Base thickness |

**Bolt Pattern (modify for your castor wheel)**

| Parameter | Value | Description |
|---|---|---|
| **bolt_x_centers** | 60 mm | Bolt spacing (X) |
| **bolt_y_centers** | 42 mm | Bolt spacing (Y) |

**Gussets**

| Parameter | Value | Description |
|---|---|---|
| **gus_thick** | 6 mm | Gusset thickness |
| **gus_len** | 14 mm | Gusset length |
| **gus_height** | 14 mm | Gusset height |

**Bracket**

| Parameter | Value | Description |
|---|---|---|
| **bracket_angle** | 60° | Bracket angle |
| **bracket_base** | `base_y / 2` | Centered location |
| **bracket_holeHeight** | `gus_height + 10 mm` | Keeper bolt Z height |
| **bracket_thickness** | 10 mm | Bracket thickness |

**Collar (Tripod Interface)**

| Parameter | Value | Description |
|---|---|---|
| **CollarTopHeight** | 4 mm | Top lip height |
| **CollarOffset** | 0.3 mm | Fit tolerance |
| **SpacerOD** | `tube_ID - 2 × CollarOffset` | Spacer outer diameter |
| **SpacerID** | 36.2 mm | TC40 leg diameter |
| **SpacerHeight** | 10 mm | Spacer depth |

**Post / Guide (Split Collar Alignment)**

| Parameter | Value | Description |
|---|---|---|
| **guidewidth** | 1.1 mm | Guide width |
| **guidelength** | 5 mm | Guide length |
| **guidedepth** | 3 mm | Guide depth |
| **guidetolerance** | 0.2 mm | Clearance |
| **postwidth** | `guidewidth - guidetolerance` | Post width |
| **postlength** | 4 mm | Post engagement |
| **postdepth** | `guidedepth - guidetolerance` | Post depth |

**Hardware Reference**

| Parameter | Value | Description |
|---|---|---|
| **m4_hole** | 4.2 mm | M4 clearance |
| **m6_hole** | 6.6 mm | M6 clearance |
| **m6_head** | 10 mm | M6 head diameter |
| **m6_nut** | 11.4 mm | M6 nut width |
| **m8_hole** | 8.8 mm | M8 clearance |
| **m8_hexhead** | 14.8 mm | M8 hex head diameter |
| **m2_insert** | 3.4 mm | Heat-set insert |
| **m2_hole** | 2.0 mm | M2 clearance |
| **m2_head** | 3.4 mm | M2 head diameter |

---

## 🧪 Test Bodies (Print Before the Final Part)

Two small test bodies are provided for fit-checking:

| FreeCAD Body | Purpose |
|---|---|
| **TestTube** | Confirms tube/collar fits your TC40 tripod leg with correct tolerance |
| **TestBase** | Confirms bolt-hole spacing matches your castor wheel base |

> **Recommended:** Print and validate both before committing to a full print.

---

## 🖨️ Printing Recommendations

| Setting | Recommendation |
|---|---|
| Material | PETG (best), PLA+ (prototype), ASA/ABS (outdoor) |
| Perimeters | 4 |
| Infill | 25–40% |
| Orientation | Split face down, axis vertical |
| Supports | Not required |

---

## 🧰 Hardware Needed

- M2 × 8–10 mm bolt + M2 heat-set insert for collar keeper
- Your chosen castor wheels and mounting bolts

---

## 📦 Files in This Repository