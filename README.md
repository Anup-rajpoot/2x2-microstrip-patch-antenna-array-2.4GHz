# 2×2 Microstrip Patch Antenna Array — 2.4 GHz WiFi

> Designed and simulated in **CST Microwave Studio 2025**  
> Department of Electronics & Communication Engineering, CU Jammu  
> April 2026

---

## Project Overview

This project presents the complete design, calculation, and simulation of a **2×2 microstrip patch antenna array** operating at **2.4 GHz** for IEEE 802.11 b/g/n WiFi applications.

Four identical rectangular patch elements are arranged in a 2-row × 2-column grid and fed through a **corporate T-junction feed network** on an FR4 substrate. Constructive interference from all four patches gives +3.28 dB gain improvement over a single patch element.

---

## Key Simulation Results

| Parameter | Value | Status |
|---|---|---|
| Operating Frequency | 2.4 GHz | ✅ |
| S11 at Resonance | −24.5 dB | ✅ Excellent |
| S11 at 2.4 GHz Marker | −18.95 dB | ✅ Good |
| VSWR at 2.4 GHz | 1.25 | ✅ Excellent |
| Bandwidth (−10 dB) | 90 MHz | ✅ |
| % Bandwidth | 3.75% | ✅ |
| WiFi Band Coverage | 2.355–2.445 GHz | ✅ Full Coverage |
| Directivity | 10.28 dBi | ✅ |
| Radiation Efficiency | 90.2% | ✅ |
| Realized Gain | 9.77 dBi | ✅ |
| Impedance at 2.4 GHz | 61 − j8.78 Ω | ✅ Near 50 Ω |
| Reflection Coefficient \|Γ\| | 0.126 | ✅ |
| Power Reflected | 1.6% | ✅ |
| Gain vs Single Patch | +3.28 dB | ✅ |

---

## Antenna Dimensions

| Parameter | Value |
|---|---|
| Substrate | FR4 (εr = 4.4, tan δ = 0.02) |
| Board Thickness | 1.6 mm |
| Copper Thickness | 0.035 mm (1 oz) |
| Patch Length (L) | 39.8 mm |
| Patch Width (W) | 55 mm |
| Element Spacing | 0.5λ = 62.5 mm |
| Ground Plane | 260 × 220 mm |
| Feed Line Width | 3.1 mm (50 Ω) |
| Quarter-λ Section | 1.55 mm (70.7 Ω) |
| Inset Feed Depth | 8.0 mm |

---

## CST Simulation Model

![CST Model](images/cst_simulation_model.jpg)

---

## Simulation Results

### S11 Return Loss
![S11](results/s11_return_loss.jpg)

### VSWR
![VSWR](results/vswr_plot.jpg)

### Smith Chart
![Smith Chart](results/smith_chart.jpg)

### 3D Radiation Pattern
![Broadside](results/radiation_pattern_broadside.jpg)
![Elevation](results/radiation_pattern_elevation.jpg)

### Farfield Summary
![Farfield](results/farfield_summary.jpg)

---

## Design Calculations Summary

### Patch Width
W = (c / 2f₀) × √(2 / (εr + 1))
W = 38 mm → CST optimised: W = 55 mm

### Effective Dielectric Constant
εeff = (εr+1)/2 + (εr−1)/2 × (1 + 12h/W)^(−½)
εeff = 4.163

### Patch Length
L_eff = c / (2 × f₀ × √εeff) = 30.6 mm
L = L_eff − 2ΔL = 29.1 mm → CST optimised: L = 39.8 mm

### VSWR Verification
|Γ| = 10^(−17.95/20) = 0.1264
VSWR = (1 + 0.1264) / (1 − 0.1264) = 1.29 ✓

### Gain
Radiation Efficiency = 10^(−0.4447/10) = 90.2%
Realized Gain = 10.28 + (−0.5149) = 9.77 dBi
Array improvement = +3.28 dB over single patch

---

## Tools Used

- **CST Microwave Studio 2025** — Full-wave EM simulation
- **FR4 PCB** — Substrate material

---

## Documents

- 📄 [Full HTML Report](docs/antenna_report.html)
- 📊 [Report PDF](docs/Array_Antenna.pdf)

---

## Author

**Anup Singh**  
B.Tech ECE, University of Jammu (CU Jammu)  
April 2026

---

## Tags

`antenna-design` `microstrip` `patch-antenna` `cst-studio` `rf-engineering`  
`2.4ghz` `wifi` `ieee-802-11` `fr4` `ecedepartment` `antenna-array`
