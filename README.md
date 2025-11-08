# DC Motor Control Simulation — Electrical Machine 1 Laboratory

This repository contains the simulation project I have accomplished for the **Electrical Machine 1 Laboratory** course at **K. N. Toosi University of Technology**, instructed by **Dr. Ali Naghdi Moradi**.  
The project focuses on the **analysis, design, and comparison of single-loop and dual-loop control systems** for a **DC motor**, implemented using **MATLAB** and **Simulink**.

---

## 📘 Project Overview

This project presents a **comprehensive simulation study of DC motor control systems**, focusing on the comparative performance of **single-loop** and **dual-loop** speed control strategies.  

The **single-loop** system utilizes a single speed feedback controller, while the **dual-loop** system employs both current and speed feedback loops (inner and outer).  
The study evaluates their **dynamic behavior**, **transient response**, and **disturbance rejection** through MATLAB and Simulink simulations.

The models demonstrate the trade-off between **simplicity and precision**:  
- The **single-loop** system is easier to design but allows larger current spikes and slower disturbance rejection.  
- The **dual-loop** system improves **stability**, **motor protection**, and **tracking accuracy** at the cost of increased complexity.

---

## 🎯 Objectives
- Develop mathematical and Simulink models for DC motor systems.
- Implement **single-loop** and **dual-loop** control architectures using **PI controllers**.
- Evaluate motor **speed**, **torque**, and **current** responses under different conditions.
- Compare system performance based on **overshoot**, **settling time**, and **disturbance rejection**.
- Provide a detailed report analyzing trade-offs between simplicity, protection, and accuracy.

---

## 📊 Key Results & Takeaways

### Performance Summary
| Metric | Single-Loop | Dual-Loop |
|:--|:--:|:--:|
| Speed overshoot | **5.1%** | **5.5%** |
| Rise time | **0.13 s** | **0.54 s** |
| Settling time | **0.48 s** | **2.18 s** |
| Armature current during transients | **Peaks > 600 A** | **Limited/controlled** |
| Disturbance rejection | Moderate | **Strong** |
| Motor protection | Limited | **Improved** |

### Insights
- **Dual-loop** architecture (current inner + speed outer) delivers **better current limiting**, **stronger disturbance rejection**, and **overall stability**, ideal when motor protection matters.  
- **Single-loop** is **simpler** and faster to settle, but allows **large current spikes** and shows weaker disturbance handling.  
- Comparative plots and scripts are provided in:  
  - MATLAB: [`results-analysis-comparasion.m`](electrical-machine-1-lab-project/MATLAB-code/results-analysis-comparasion.m)  
  - Simulink: [`DC-dual-loop-single-loop-comparasion.slx`](electrical-machine-1-lab-project/simulink/DC-dual-loop-sinlge-loop-comparasion.slx)

> For full derivations, figures, and experiment details, see the report:  
> 📄 [`DC-motor-single-and-dual-controller-simulation-report.pdf`](electrical-machine-1-lab-project/report/DC-motor-single-and-dual-controller-simulation-report.pdf)

---

## 🧩 Repository Structure
```bash
electrical-machine-1-lab-project/
├─ MATLAB-code/
│  ├─ results-analysis-comparasion.m               # Compares dual-loop and single-loop results
│  ├─ results-analysis-dual-loop-current-loop.m    # Analyzes dual-loop current control
│  ├─ results-analysis-dual-loop.m                 # Analyzes dual-loop speed and torque results
│  ├─ results-analysis-single-loop.m               # Analyzes single-loop system performance
│
├─ simulink/
│  ├─ DC-dual-loop.slx                             # Dual-loop DC motor control model
│  ├─ DC-dual-loop_single-loop_comparasion.slx     # Comparative simulation model
│  ├─ DC-motor_single_loop.slx                     # Single-loop DC motor control model
│
├─ report/
│  └─ DC-motor-single-and-dual-controller-simulation-report.pdf
│
├─ paper/
  └─ drive-and-control-of-DC-motor-and-its-simulation.pdf

```
## 📦 Quick Access
---
### MATLAB Codes
| File | What it does |
|------|--------------|
| [results-analysis-comparasion.m](electrical-machine-1-lab-project/MATLAB-code/results-analysis-comparasion.m) | Side-by-side plots and metrics comparing **single** vs **dual** loop |
| [results-analysis-dual-loop-current-loop.m](electrical-machine-1-lab-project/MATLAB-code/results-analysis-dual-loop-current-loop.m) | Inner **current loop** analysis (overshoot/limits) |
| [results-analysis-dual-loop.m](electrical-machine-1-lab-project/MATLAB-code/results-analysis-dual-loop.m) | Dual-loop **speed/torque/current** evaluation |
| [results-analysis-single-loop.m](electrical-machine-1-lab-project/MATLAB-code/results-analysis-single-loop.m) | Single-loop performance (speed, torque, current) |

### Simulink Models
| Model | Description |
|------|-------------|
| [DC-dual-loop.slx](electrical-machine-1-lab-project/simulink/DC-dual-loop.slx) | Dual-loop (speed outer, current inner) |
| [DC-dual-loop_single-loop_comparasion.slx](electrical-machine-1-lab-project/simulink/DC-dual-loop_sinlge-loop_comparasion.slx) | Combined model to compare **single** vs **dual** loop |
| [DC-motor-single-loop.slx](electrical-machine-1-lab-project/simulink/DC-motor-single-loop.slx) | Single-loop speed control |

### Reports & Paper
| File | Description |
|------|-------------|
| [DC-motor-single-and-dual-controller-simulation-report.pdf](electrical-machine-1-lab-project/report/DC-motor-single-and-dual-controller-simulation-report.pdf) | Full project report, figures, and methods |
| [drive-and-control-of-DC-motor-and-its-simulation.pdf](electrical-machine-1-lab-project/paper/drive-and-control-of-DC-motor-and-its-simulation.pdf) | Reference paper used in the study |


