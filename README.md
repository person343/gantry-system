# Precision XY Gantry System for X-ray Diffraction Mammography

![Gantry System](./images/hero.png)

## 📌 Overview

This project supports the development of a next-generation **4D mammography device** that uses **X-ray diffraction** to extract tissue density — the “fourth dimension” — and reduce false positives in cancer screening.

I designed and fabricated a **stacked XY gantry system** that positions an X-ray filter across two dimensions with sub-millimeter accuracy. The filter captures diffraction patterns at each point in a 300mm × 300mm scan area, enabling image reconstruction based on tissue density variations.

---

## 🧠 Problem Statement

Standard mammography relies on X-ray absorption, which can misrepresent dense but benign tissue as malignant — leading to a high false positive rate.

To overcome this, the company I worked with is developing a 4D imaging system that incorporates **X-ray diffraction** to measure **material density**. This required a gantry system capable of:

- High positional accuracy
- Smooth motion across 2 axes
- **Tight spatial integration** into an existing 3D mammography system

---

## ⚙️ System Architecture

The gantry system consists of **two orthogonally stacked axes**:

- The **X-axis** base moves a carriage side-to-side using a **single T8 lead screw** and dual MGN12H linear rails
- The **Y-axis** is mounted to the X-axis carriage using **custom-designed aluminum mounts**, and moves front-to-back using its own **T8 lead screw** and linear rails

Each axis includes:
- **One T8 lead screw** with anti-backlash nut
- **Two MGN12H steel linear rails** for stability and load distribution
- **NEMA 17 stepper motors**, controlled via Arduino

This design delivers precise motion with minimal vibration while fitting within existing medical housing constraints.

---

## 🛠 Design Highlights

| Component            | Description |
|---------------------|-------------|
| Travel Range         | 300mm × 300mm total workspace |
| Frame Material       | CNC-machined aluminum extrusion and plates |
| Linear Motion        | 1× T8 lead screw + 2× MGN12H rails per axis |
| Drive System         | NEMA 17 stepper motors + screw couplings |
| Controller           | Arduino microcontroller (open-loop control) |
| Axis Integration     | Custom-designed Y-axis mounts on X-carriage |
| Fit Verification     | 3D printed mounts used to test fit before CNC fabrication |

---

## 🧪 Challenges & Solutions

### 🔧 Spatial Constraints  
The gantry had to be installed within the confined internal structure of a commercial 3D mammography machine.

- I custom-designed the Y-axis mounting hardware to fit securely on the X-carriage while keeping height and width within strict tolerances
- Used 3D-printed test pieces to prototype all mounting components and verify clearance
- Final parts were CNC-machined in aluminum for strength and dimensional accuracy

### 🚧 Vibration & Alignment  
The first iteration used a **single guide rail** per axis. This led to:

- Lateral drag against the rail
- Audible strain and near-stalling of stepper motors

✅ **Solution:**
- Switched to a **dual-rail configuration** per axis to balance load and eliminate misalignment
- Performed static FEA in Fusion 360 to confirm rigidity before final machining
- Final system operated quietly with smooth, backlash-free motion

---

## 📐 CAD & Simulation

CAD was designed in **Fusion 360**.  
I performed static structural FEA to evaluate rail mounting stiffness and support bracket deflection.

<p align="center">
  <img src="./images/gantry-cad.png" width="600" alt="CAD Assembly View">
</p>

<p align="center">
  <img src="./analysis/fea-results.png" width="600" alt="FEA Simulation">
</p>

---

## 🔧 Fabrication Process

- 🧰 CNC machined all aluminum plates and motor mounts using a **Tormach mill**
- 🖨️ Prototyped all structural components using a **Bambu Labs 3D printer**
- Used laser-cut jigs and manual alignment methods during final assembly

---

## 📊 Performance & Results

| Metric                  | Result |
|--------------------------|--------|
| Repeatability            | ±0.1 mm |
| Stepper Load/Overdrive   | Eliminated by dual-rail layout |
| Max Load Deflection      | <0.05 mm (validated in FEA) |
| Acoustic Noise           | Only stepper motor hum |
| Build Cost               | ~$130 USD |

---

## 📁 Files

- 📄 [Full Report (PDF)](./files/Full-Report.pdf)
- 🧾 [Bill of Materials (Excel)](./files/BOM.xlsx)
- 📦 [CAD Files (.f3d, STEP)](./CAD/GantrySystem_v2.f3d)

---

## 🚀 Future Work

- Integrate limit switches for homing and soft stops
- Add encoder-based closed-loop motion control
- Evaluate belt drive Y-stage for reduced cost and increased speed
- Automate scanning sequence with host controller interface

---

## 📖 License

Licensed under the MIT License — reuse and adaptation permitted with attribution.
