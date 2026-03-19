# Parametric-Bolt-Design-SolidWorks-Automation-System

A web-based engineering tool for **ISO-standard hex bolt design** integrated with **automated SolidWorks macro generation**.
Built for engineers who prefer precision over guesswork.

---

##  Overview

This project transforms bolt design from a manual, table-driven process into a **parametric, automated workflow**.

Instead of flipping through tables in Shigley, this system:

* Computes bolt geometry instantly
* Ensures ISO compliance (4014 / 4017)
* Generates a **ready-to-run SolidWorks VBA macro**
* Bridges **theory → design → CAD execution**

---

##  Features

###  Parametric Bolt Design

* Supports metric sizes from **M4 to M64**
* Automatic pitch, head size, and geometry selection
* ISO standard compliance:

  * **ISO 4014 (Partial Thread)**
  * **ISO 4017 (Full Thread)**

###  Intelligent Engineering Calculations

* Thread length estimation (based on ISO rules)
* Core & pitch diameter calculation
* Tensile stress area (At)
* Thread depth & revolutions

###  SolidWorks Automation

* Generates **fully functional VBA macro**
* One-click workflow:

  1. Generate specification
  2. Generate macro
  3. Paste → Run → Done

###  Data Export

* Export bolt data as **JSON**
* Useful for:

  * Simulation pipelines
  * Design databases
  * Automation scripts

---

##  Engineering Backbone

This system is not guesswork—it follows:

* **Shigley’s Mechanical Engineering Design**
* ISO standard proportions for hex bolts
* Empirical thread geometry relations

Key computed parameters include:

* Pitch diameter (d₂)
* Core diameter (d₃)
* Tensile stress area (Aₜ)
* Thread engagement length

---

##  How to Use

### 1. Generate Bolt Specification

* Select diameter (e.g., M10)
* Enter desired length
* Choose thread type and grade
* Click **"Generate Spec"**

### 2. Generate SolidWorks Macro

* Click **"Generate SW Macro"**
* Copy the generated VBA code

### 3. Run in SolidWorks

```
Tools → Macro → New
Paste the code → Run (F5)
```
 The bolt is generated automatically in 3D.

---

##  System Architecture

* **Frontend:** HTML + CSS + JavaScript
* **Logic Layer:** Parametric equations + ISO rules
* **CAD Integration:** SolidWorks API (VBA Macro)

This creates a pipeline:

```
User Input → Engineering Model → CAD Automation
```

---

##  File Structure

```
index.html   # Main application (UI + logic + macro generator)
README.md         # Project documentation
```

---

##  Example Output

**Input:**

* Diameter: M10
* Length: 47 mm

**Output:**

* Standardized Length: 50 mm
* Thread Length: Calculated automatically
* Tensile Area: Computed
* Full SolidWorks macro generated

---

## ⚠️ Limitations

* Depends on SolidWorks environment for macro execution
* Thread generation uses predefined profile path:

  ```
  C:\ProgramData\SolidWorks\...\Metric Die.SLDLFP
  ```
* No FEM or stress simulation (yet)

---

##  Future Improvements

*  Add **FEA integration (ANSYS / Python)**
*  Include **fatigue & preload calculations**
*  Support **fine threads & custom threads (ACME, square)**
*  Direct **STEP/Parasolid export**
*  Cloud-based CAD integration

---

## 📚 References

* Shigley, *Mechanical Engineering Design*
* ISO 4014 / ISO 4017 standards

---

## 👨‍💻 Author

**Arafat Hossain** Mechanical Engineering Student

---
