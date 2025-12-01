# 💊 Geriatric Digoxin PK Digital Twin
### An Explainable, Patient-Specific Pharmacokinetic Simulator for Precision Geriatric Dosing

## 📖 Overview
This project is a fully client-side, web-based **Explainable Pharmacokinetic Digital Twin** that simulates how **Digoxin** behaves in:
- **Normal adults**
- **Frail geriatric patients** (reduced renal function, low body weight, sarcopenia)

Digoxin has a **Narrow Therapeutic Index (NTI)**. Small concentration increases can cause toxicity (arrhythmia, bradycardia, visual disturbances). The simulator demonstrates why **population-based dosing fails** in older adults and why **individualized PK** is essential.

👉 **Live Demo:** *(Add link)*

---

## 🧠 Core Idea
> **One dose does not fit all.**

This tool provides:
- Individualized PK parameters
- Concentration–time curves
- Steady-state metrics
- Explainable clinical insights
- Side-by-side comparison with healthy adults

---

## 💡 Key Features
### ✔ Patient-Specific PK Modeling
Inputs: age, sex, weight, Scr, dose, tau, number of doses  
Outputs: CrCl, CL, Vd, k, t1/2, Cmax_ss, Cmin_ss, exposure category

### ✔ Dual Digital Twin Comparison
Solid: patient  
Dashed: normal adult

### ✔ Explainable Clinical Interpretation  
Describes underexposure, accumulation, renal decline, dose needs.

### ✔ Fully Browser-Based  
No backend · No dependencies · Privacy-friendly

---

## 🔬 Scientific Background (Clinical PK)
| PK Factor | Normal Adult | Older Adult | Effect |
|----------|--------------|-------------|--------|
| CrCl | 80–120 mL/min | 30–50 mL/min | ↓ renal function |
| CL | 6–8 L/h | 3–4 L/h | ↓ 50% → accumulation |
| Vd | 6–7 L/kg | 5–6 L/kg | ↓ lean mass |
| t1/2 | 36–48 h | 60–80 h | ↑ 1.5–2× |
| Cmin_ss | 0.4–0.7 ng/mL | 0.8–1.5 ng/mL | ↑ toxicity |

References include findings from Jusko (1978), Koup (1980), Aronson, Brocks, Jelliffe.

---

## 🛠 Tech Stack
- HTML5 / CSS3 / Vanilla JS
- Chart.js
- Serverless client-side architecture

---

## 🚀 Getting Started

```bash
git clone https://github.com/yourusername/geriatric-digoxin-digitalTwin.git
cd geriatric-digoxin-digitalTwin
open version1.html   # or double-click
```

---

## 🧩 Versioned Modeling Assumptions

### 🔹 Version 1.0 — Educational PK Model (Current)
- One-compartment IV bolus
- Renal scaling:
  
CL = TV_CL × (CrCl/80)^0.75
- Weight scaling:
  
V = TV_V × (weight/70)
- Cockcroft–Gault CrCl
- Steady-state via exponential decay summation
- Therapeutic range: 0.5–1.0 ng/mL  
**Limitations:** No IIV, no Bayesian updating, no distribution phase

### 🔹 Version 2.0 — Mechanistic PopPK (Planned)
- Two-compartment model
- PopPK covariate models
- Inter-individual variability
- Bayesian MAP updating
- 95% prediction intervals

### 🔹 Version 2.5 — Clinical Decision Module
- P-gp interactions  
- Electrolyte effects (K+, Mg2+, Ca2+)  
- Precision dosing engine  

---

## 🏁 Summary
A transparent, interpretable Digital Twin for geriatric Digoxin dosing, integrating:
- Clinical pharmacology
- PK/PD modeling
- Explainable AI  
Ideal for:
- PhD applications  
- PK/PD portfolios  
- Precision medicine research  

---

## 📚 Citation

Jelliffe RW, Brooker G. A clinically useful method for the determination of digoxin doses and maintenance regimens. J Chronic Dis. 1974;27(1):15-22.
Koup JR, Green BL. Clinical pharmacokinetics of digoxin in the elderly. Clin Pharmacokinet. 1980;5(6):531-540.
Jusko WJ, Weintraub M., Vore M. Digoxin disposition in obesity. Clin Pharmacol Ther. 1978;24(1):28-35.
Brocks DR. The pharmacokinetics of digoxin in the elderly: a review. J Clin Pharm Ther. 2012;37(4):379-385.
Aronson JK. Clinical pharmacokinetics of digoxin 1980. Clin Pharmacokinet. 1980;5(2):167-179.


© 2025 Goyeun Yun. All rights reserved.
