# Differential Amplifier (5T) with Source Follower

## Overview
This project focuses on the design and simulation of a **CMOS Differential to Single-Ended Amplifier (5T)** integrated with a **Source Follower** output stage. The design meets strict stability and linearity requirements using **Cadence Virtuoso**.
A key feature of this design is the utilization of **Native NMOS** transistors to significantly enhance the input dynamic range and tracking capabilities.

## Architecture & Features
* **Stage 1:** Differential Pair with Active Current Mirror Load (5T topology).
* **Stage 2:** Source Follower (Common Drain) acting as an output buffer.
* **Feedback:** Configured as a Unity Gain Buffer.
* **Optimization:** Replaced standard input transistors with **Native NMOS** (low Vth) to extend the saturation range and improve input-output tracking.

## Key Specifications (Post-Optimization)
Based on final simulations with a 1pF load capacitor:

| Parameter | Value | Note |
|-----------|-------|------|
| **Open-Loop Gain** | ~37 dB | Validated vs. theoretical model |
| **Phase Margin** | 69 deg | Stable (>60 deg) after load optimization |
| **Bandwidth (BW)** | 7.35 MHz | Derived from settling time analysis |
| **Settling Time** | ~136 ns | Measured for +/- 50mV step |
| **Reference Current** | 3 uA | Optimized for optimal headroom |

## Project Contents (PDF)
The report covers the full design cycle:
* **Schematic Design:** Implementation of the 5T amp and source follower.
* **DC Sweep & Saturation Analysis:** Verifying tracking range and Vdsat margins for all transistors.
* **Native Transistor Analysis:** Demonstrating the impact of Native NMOS on the linear range compared to standard NMOS.
* **Transient Analysis:** Step response simulations to measure settling time and stability.
* **Stability Compensation:** Increasing load capacitance (from 0.5pF to 1pF) to improve Phase Margin from 55 deg to 69 deg.

## Tools Used
* **Cadence Virtuoso** (Schematic & ADE)
* **Spectre Simulator**


