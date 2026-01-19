# Differential Amplifier (5T) with Source Follower

## Overview
This project focuses on the design and simulation of a **CMOS Differential to Single-Ended Amplifier (5T)** integrated with a **Source Follower** output stage, designed and verified in **Cadence Virtuoso / Spectre**.
A key feature is the replacement of the standard input NMOS with a **Native NMOS (low-Vth)** device to extend the **tracking / saturation range** and significantly improve input-output following behavior.

## Architecture & Features
* **Stage 1:** Differential Pair with Active Current Mirror Load (5T topology).
* **Stage 2:** Source Follower (Common Drain) output buffer.
* **Feedback:** Configured as a **Unity Gain Buffer** connection.
* **Optimization:** Replaced input transistor **M1** with **Native NMOS** (low Vth) to extend the saturation/tracking range (up to ~1.59–1.6V).

## Key Specifications (Final)
Final simulations include compensation where the capacitor at node **N2** was increased to **1 pF** to ensure stability.

| Parameter | Value | Note |
|-----------|-------|------|
| **Open-Loop Gain** | ~37 dB | Matches theoretical design estimates. |
| **Phase Margin** | 69 deg | Improved after compensation (0.5pF → 1pF at node N2). |
| **Bandwidth (BW)** | ~7.35 MHz | Derived from settling-time analysis. |
| **Settling Time** | ~136 ns | Measured for a ±50mV step around Vin=850mV. |
| **Reference Current** | 3 uA | Optimized for headroom vs. operating range. |

## Project Contents (PDF)
The uploaded report covers the full design cycle:
* **Schematic Design:** Implementation of the 5T amplifier and source follower.
* **DC Sweep & Saturation Analysis:** Verification of tracking range and VDSAT margins.
* **Native NMOS Analysis:** Comparison vs. standard NMOS and impact on linear/tracking range.
* **Transient Analysis:** Step response simulations to measure settling-time and speed.
* **Stability / Compensation:** Analysis showing how increasing the capacitor at the intermediate node (N2) from **0.5pF to 1pF** improved PM from **55° to 69°**.

## Tools Used
* **Cadence Virtuoso** (Schematic & ADE)
* **Spectre Simulator**
