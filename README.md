# Precision XY Gantry System for X-ray Diffraction Mammography

![Gantry System](./images/hero.png)

## 📌 Overview

This project is part of the development of a next-generation **4D mammography system** that incorporates **X-ray diffraction imaging** to extract **tissue density** data—aiming to drastically reduce false positives in breast cancer detection.

The XY gantry system was designed to **precisely position an X-ray filter** along two axes to scan and reconstruct a full diffraction image. The positioning stage required **sub-millimeter accuracy**, low vibration, and mechanical stability for reliable data acquisition.

---

## 🧠 Problem Statement

Conventional mammography has an alarmingly high false-positive rate, leading to unnecessary biopsies and patient anxiety. The company I worked with is pioneering a **4D imaging system**, where the fourth dimension—**density**—is derived using **X-ray diffraction**.

To extract diffraction data, the system needs to **position an X-ray filter** in the XY plane with extreme precision. Off-the-shelf solutions were too large, imprecise, or prohibitively expensive for integration into a compact medical device.

---

## ⚙️ My Role & Contributions

- **Evaluated drive mechanisms** (belt vs. screw) for precision and vibration resistance
- **Selected dual T8 lead screws** to optimize for accuracy, backlash elimination, and mechanical simplicity
- **Designed the XY gantry frame** using aluminum extrusions, stepper motor mounts, and custom brackets
- **Iterated on linear rail support**: switched from a single rail to **dual linear guide rails** after observing deflection and instability in initial prototype
- **Performed FEA analysis** in Fusion 360 to validate structural stiffness of dual-rail design
- **Manufactured all mechanical components**:
  - CNC machining for metal motor mounts and end brackets
  - 3D printing for rapid prototyping and test fitting

---

## 🛠 Key Design Decisions

| Design Element        | Chosen Approach                     | Rationale                                  |
|-----------------------|--------------------------------------|--------------------------------------------|
| Drive Mechanism       | Dual T8 Lead Screws                 | Higher accuracy and lower vibration than belts |
| Guide Rail System     | Dual MGN12H Linear Rails            | Eliminated rotational deflection and uneven loading |
| Materials             | Aluminum Extrusions + Steel Rails   | Rigid, lightweight, and easily machinable   |
| Motion Control        | Stepper Motors with TMC2209 Drivers | Silent, precise microstepping               |

---

## 📐 CAD & Simulation

CAD was developed in **Fusion 360**, with multiple design iterations and static structural analysis.

<p align="center">
  <img src="./images/gantry-cad.png" width="600" alt="CAD Model">
</p>

### 🔍 FEA Results
- Max deflection under simulated load: < 0.05 mm
- Peak stress remained well below yield strength of aluminum structure

<p align="center">
  <img src="./analysis/fea-results.png" width="600" alt="FEA Stress Analysis">
</p>

---

## 🧪 Fabrication & Testing

- Used **Tormach CNC mill** for metal parts and laser-cutting for plate brackets
- Rapid prototyped alignment fixtures using **FDM 3D printing**
- Verified mechanical alignment and measured backlash with test dial indicator
- System achieved **< ±0.1 mm repeatability**

---

## 📁 Files

- 📄 [Full Project Report (PDF)](./files/Full-Report.pdf)
- 📦 [CAD Files (.f3d, STEP)](./CAD/GantrySystem_v2.f3d)
- 🧾 [Bill of Materials](./files/BOM.xlsx)
- 🔧 [Motor Mount Drawings](./files/mount-drawings.pdf)

---

## 🚀 Future Improvements

- Add closed-loop encoder feedback for drift detection
- Integrate automated homing and calibration sequence
- Evaluate belt-drive Y-axis tradeoff for speed vs. accuracy

---

## 📖 License

MIT License — reuse and attribution encouraged.
