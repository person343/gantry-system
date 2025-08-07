# XY Gantry System – Calidar

This project documents the design, analysis, and fabrication of a high-precision XY gantry subsystem for use in an X-ray diffraction module as part of a next-generation 4D mammography device developed at **Calidar**, a stealth-mode medical imaging startup. The system emphasizes mechanical precision, structural stability, and vibration minimization during high-resolution imaging procedures.

---

## 📂 Repository Structure

```plaintext
├── cad_drawings/        # Technical manufacturing drawings (dimensioned)
├── images/              # FEA, assembly, and exploded view images
├── LICENSE              # Repository license (MIT)
├── README.md            # This file
└── XY_Gantry_Report_FINAL_Kevin_Yuan.pdf  # Full engineering report
```

---

## 🧠 Project Summary

The gantry is designed to move an X-ray detector module along two axes (X and Y) with high repeatability and minimal vibration. It uses custom-machined aluminum parts, precision linear rails, lead screw actuation, and NEMA 17 stepper motors.

- **Purpose:** Enable precise scanning for 3D reconstruction via diffraction  
- **Precision Goal:** <0.2 mm positional error  
- **Motion System:** Orthogonal screw-drive XY configuration with custom mounts

---

## 🔩 Key Features

- **Custom Mounting Hardware:** Designed and machined in-house to attach the Y-axis onto the X-axis rail securely  
- **C-Channel Gantry Arms:** Chosen for high torsional rigidity while minimizing mass  
- **Dual Linear Guides per Axis:** Significantly improves stiffness and eliminates tilt under load  
- **Stepper Motor Integration:** Enables repeatable microstepping control through onboard firmware

---

## 📐 CAD Drawings

All parts were modeled in Fusion 360 and manufactured in-house or CNC-machined. Drawings include full dimensioning for fabrication.

- [Gantry Arm Drawing](cad_drawings/gantry_arm_drawing.png)
- [X-to-Y Mount Drawing](cad_drawings/x_y_mount_drawing.png)
- [Lead Screw / Guide Rail Mount Drawing](cad_drawings/lead_screw_mount_drawing.png)

---

## 🛠️ Assembly & Fabrication Photos

Real-world assembly and photos of integration with the full mammography system:

- [Gantry Fully Assembled](images/gantry_assembled.jpg)
- [Exploded View for Fabrication](images/gantry_exploded.jpg)

---

## 📊 Finite Element Analysis (FEA)

A static load test was simulated using Autodesk Fusion 360 to ensure adequate structural integrity during operation:

- [FEA Safety Factor Visualization](images/fea_result.png)

---

## 📄 Full Engineering Report

Download the full PDF report describing the full engineering design process:

📎 [XY_Gantry_Report_FINAL_Kevin_Yuan.pdf](XY_Gantry_Report_FINAL_Kevin_Yuan.pdf)

---

## ⚙️ Technologies Used

- CAD: Autodesk Fusion 360  
- CAM: CNC Machining + FDM 3D Printing  
- Simulation: Static Stress (Fusion 360 FEA)  
- Materials: Aluminum 6061, hardened steel rails  
- Motors: NEMA 17 stepper motors with couplings and lead screws

---

## 🧑‍💻 Author

**Kevin Yuan**  
Mechanical Engineering @ Duke University  
Design Engineer at [Calidar](#) (Stealth-mode startup)

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
