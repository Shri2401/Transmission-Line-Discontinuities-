# Analysis of Transmission Line Discontinuities using Time Domain Reflectometry

## Authors
- **Ankit Kumar**
  - Electrical and Computer Engineering, University of Colorado, Boulder, USA
  - Email: [ankit.kumar@colorado.edu](mailto:ankit.kumar@colorado.edu)
- **Shrinithi Venkatesan**
  - Electrical and Computer Engineering, University of Colorado, Boulder, USA
  - Email: [shrinithi.venkatesan@colorado.edu](mailto:shrinithi.venkatesan@colorado.edu)

## Overview
This project analyzes the effects of return path discontinuities, specifically slots, on transmission lines using Time Domain Reflectometry (TDR). A methodology to mitigate these effects by introducing additional capacitance via patches is proposed and evaluated. The project includes simulation, design, and experimental verification using a printed circuit board (PCB) setup.

## Abstract
The study presents a method to address the effects of return path discontinuities caused by slots in transmission lines. By adding capacitance through patches above the slots, impedance stabilization is achieved. This approach is validated using TDR responses, showing improved signal integrity and reduced impedance variability in high-frequency electronic systems.

## Table of Contents
1. [Introduction](#introduction)
2. [Theoretical Development](#theoretical-development)
3. [Project Flow](#project-flow)
4. [Experimental Setup](#experimental-setup)
5. [Results](#results)
   - [Measured TDR Plot for 25 Ω](#measured-tdr-plot-for-25-Ω)
   - [Measured and Simulated TDR Plots for 25 Ω](#measured-and-simulated-tdr-plots-for-25-Ω)
   - [Measured and Simulated TDR Plots for 50 Ω](#measured-and-simulated-tdr-plots-for-50-Ω)
   - [Measured and Simulated TDR Plots for 75 Ω](#measured-and-simulated-tdr-plots-for-75-Ω)
   - [Reverse Engineering the Measured Plots for 25 Ω Transmission Line](#reverse-engineering-the-measured-plots-for-25-Ω-transmission-line)
6. [Conclusions](#conclusions)

## Introduction
The project addresses the challenge of maintaining signal integrity in transmission lines on PCBs at high frequencies. Discontinuities such as slots in the ground plane can cause return path discontinuities (RPD), leading to impedance mismatches and signal reflections. TDR is used to analyze these discontinuities and the effectiveness of the proposed solution.

## Theoretical Development
Two methods to mitigate return path discontinuities are considered:
1. **Making the Discontinuity Transparent:** By reducing the discontinuity's geometry to less than 1/3 of the spatial extent of the signal edge.
2. **Adding Capacitance:** By increasing the width of the transmission line at the discontinuity, thus increasing capacitance and reducing impedance.

## Project Flow
The project follows these steps:
1. **Simulation:** Using Ansys HFSS to simulate transmission lines and obtain design parameters.
2. **Board Design:** Designing the PCB with Altium Designer and obtaining 1-port measurements using a Vector Network Analyzer (VNA).
3. **TDR Measurements:** Importing s1p files into Keysight ADS, plotting, and analyzing TDR data.
4. **Reverse Engineering:** Comparing and analyzing simulated and measured results.
5. **Comparison:** Comparing plots for measured and simulated data.
6. **Verification:** Verifying the best design and measurement practices.

## Experimental Setup
Transmission lines with impedance values of 25 Ω, 50 Ω, and 75 Ω were tested. A microstrip structure was created, and slots were introduced in the return path. The slot dimensions were calculated based on the spatial extent of the signal. Additional capacitance was added through patches, and the designs were tested using TDR.
  ![Board Design](https://github.com/Shri2401/Transmission-Line-Discontinuities-/blob/main/supporting%20pics/Picture1.png)

## Results

### Measured TDR Plot for 25 Ω
- A characteristic impedance of 25 Ω is observed.
- Inductive behavior is indicated by peaks in the impedance.
- Capacitive behavior is indicated by dips in the impedance.
- Combination of slot and patch shows a compensated impedance close to 25 Ω.

### Measured and Simulated TDR Plots for 25 Ω
- Simulated plot shows a characteristic impedance of 24.8 Ω.
- Measured results show minimal discrepancy, with an error percentage of 0.4%.

### Measured and Simulated TDR Plots for 50 Ω
- Simulated characteristic impedance is 49.9 Ω.
- Measured characteristic impedance shows a maximum discrepancy of 6.2%.

### Measured and Simulated TDR Plots for 75 Ω
- Simulated characteristic impedance is 75.6 Ω.
- Measured characteristic impedance shows a maximum discrepancy of 12%.

### Reverse Engineering the Measured Plots for 25 Ω Transmission Line
- Inductance and capacitance values for the transmission lines are obtained through detailed TDR plot analysis.

## Conclusions
The study demonstrates that by introducing patches to counteract the effects of slots, the characteristic impedance of transmission lines can be effectively managed. The results highlight the importance of maintaining a uniform return path for optimal signal integrity in high-frequency systems. The practical guidelines provided are valuable for transmission line design.

---

For detailed steps and data analysis, please refer to the full paper and supplementary materials provided. If you have any questions or need further assistance, feel free to contact the authors at their respective emails.
