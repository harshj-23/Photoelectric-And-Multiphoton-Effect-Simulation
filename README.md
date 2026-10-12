# 🔬 Photoelectric & Multiphoton Effect Simulation

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Online-brightgreen?style=for-the-badge&logo=githubpages)](https://harshj-23.github.io/Photoelectric-And-Multiphoton-Effect-Simulation/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)

An interactive, self-contained HTML5/Canvas physics simulation modeling both **classical single-photon photoelectric emission** and **nonlinear multiphoton photoemission** using ultrafast femtosecond laser pulses.

🔗 **Live Preview:** [https://harshj-23.github.io/Photoelectric-And-Multiphoton-Effect-Simulation/](https://harshj-23.github.io/Photoelectric-And-Multiphoton-Effect-Simulation/)

---

## 📸 Overview

This simulation provides a visual and mathematical laboratory setup to explore light-matter interactions at macroscopic, phototube, and atomic scales:

- **Macroscopic Level:** Full electrical circuit with vacuum phototube, variable DC supply, ammeter, voltmeter, and moving wire-drift charges.
- **Tube Interior Level:** Enlarged phototube cross-section tracking incident photons and individual emitted photoelectron trajectories across the accelerating/retarding potential gap.
- **Atomic Level:** Quantum energy ladder and Bohr-style virtual excitation shells illustrating intermediate virtual-state transitions ($\vert{}v_n\rangle$) and the final threshold-breaking ionization step.

---

## ✨ Features

- **⚡ Clickable Light & Laser Sources:** The light source and femtosecond laser head start **OFF** by default. Click directly on the source chassis to toggle optical power **ON/OFF**.
- **💡 Dual Experimental Regimes:**
  - **Classical Photoelectric Effect (Einstein Regime):** Test monochromatic CW light across Cesium, Sodium, Potassium, Calcium, Zinc, and Gold to examine threshold frequencies and kinetic energy cutoffs ($KE_{\text{max}} = h\nu - \Phi$).
  - **Multiphoton Effect (Femtosecond Regime):** Switch to a mode-locked Ti:Sapphire pulsed laser ($\sim 800\text{ nm}$, $\sim 100\text{ fs}$). Demonstrates how sub-threshold photons liberate electrons through simultaneous multi-quanta absorption ($n \cdot h\nu \ge \Phi$, yield scaling nonlinearly as $I \propto \mathcal{P}^n$).
- **🔬 "At atomic level" Quantum View:**
  - Displays energy levels from Ground State ($E_0 = 0\text{ eV}$) through dashed virtual intermediate states up to the work function barrier ($\Phi$) and the continuum.
  - Step-by-step photon excitation animation: each incoming photon packet delivers $+h\nu$, exciting the electron until the final photon ionizes it into the vacuum.
- **📈 Real-Time $I\text{--}V$ Characteristic Graph:**
  - Live curve rendering showing stopping potentials ($-V_0$), accelerating saturation limits, and the live operating point marker.
  - **⛶ Enlarge Graph Modal:** Click the button at the top-right of the graph to pop out a centered, high-resolution modal for detailed data reading.
- **🖥️ Clean Responsive Design:**
  - High-contrast, left-aligned, readable typography.
  - Fixed viewport layout (`100vh`) with zero vertical or horizontal scrollbars.

---

## 📐 Physics Principles & Equations

### 1. Classical Photoelectric Effect (Einstein, 1905)
$$E_{\text{photon}} = h\nu = \frac{hc}{\lambda}$$
$$KE_{\text{max}} = h\nu - \Phi$$
$$eV_0 = KE_{\text{max}} \quad \implies \quad V_0 = \frac{h\nu - \Phi}{e}$$

### 2. Multiphoton Photoemission (Fowler–DuBridge Theory)
When photon energy is below the work function ($h\nu < \Phi$), intense optical fields crowd photons in space and time, allowing simultaneous absorption of $n$ photons:
$$n = \left\lceil \frac{\Phi}{h\nu} \right\rceil \quad \text{or} \quad n = \left\lfloor \frac{\Phi}{h\nu} \right\rfloor + 1$$
$$KE_{\text{max}} = n \cdot h\nu - \Phi$$
$$J_n \propto I^n \quad (\text{Nonlinear Yield Scaling})$$

---

## 🎛️ Controls & Parameters

| Parameter | Range | Description |
|---|---|---|
| **Target Metal** | Cs, Na, K, Ca, Zn, Au | Selects cathode material and sets work function $\Phi$ ($2.14\text{ eV}$ to $5.31\text{ eV}$) |
| **Wavelength ($\lambda$)** | $250\text{ nm} - 1000\text{ nm}$ | Tunable light wavelength (updates photon energy $h\nu$ and color) |
| **Intensity** | $0\% - 100\%$ | Controls optical irradiance and particle generation density |
| **Applied Voltage ($V$)** | $-5.0\text{ V} \text{ to } +5.0\text{ V}$ | Adjusts accelerating (+) or retarding ($-$) potential between plates |
| **Multiphoton effect** | Checkbox | Toggles CW Arc Lamp $\leftrightarrow$ Ultrafast Mode-Locked Laser |

---

## 🚀 Getting Started

Since the simulation is built with pure web standards (HTML5 Canvas, CSS, and Vanilla JavaScript), no build tools, bundlers, or package managers are required.

### Run Locally:
1. Clone the repository:
   ```bash
   git clone [https://github.com/harshj-23/Photoelectric-And-Multiphoton-Effect-Simulation.git](https://github.com/harshj-23/Photoelectric-And-Multiphoton-Effect-Simulation.git)
