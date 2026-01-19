# Differential Amplifier (5T) with Source Follower

## Overview
This project focuses on the design and simulation of a **CMOS Differential to Single-Ended Amplifier (5T)** integrated with a **Source Follower** output stage, designed and verified in **Cadence Virtuoso / Spectre**.
A key feature is replacing the input NMOS with a **Native NMOS (low-Vth)** device to extend the **tracking / saturation range** and improve input-output following behavior. :contentReference[oaicite:0]{index=0}

## Architecture & Features
* **Stage 1:** Differential Pair with Active Current Mirror Load (5T topology).
* **Stage 2:** Source Follower (Common Drain) output buffer. :contentReference[oaicite:1]{index=1}
* **Feedback:** Configured as a **Unity Gain Buffer** connection. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}
* **Optimization:** Replaced transistor **1M** with **Native NMOS** (low Vth) to extend the saturation/tracking range (up to ~1.59–1.6V). :contentReference[oaicite:4]{index=4}

## Key Specifications (Final)
Final simulations include compensation where the capacitor at node **2N (N2)** was increased to **1 pF** to improve stability. :contentReference[oaicite:5]{index=5}

| Parameter | Value | Note |
|-----------|-------|------|
| **Open-Loop Gain** | ~37 dB | Matches the expected/theoretical estimate. :contentReference[oaicite:6]{index=6} |
| **Phase Margin** | 69 deg | Improved after compensation (0.5pF → 1pF at node 2N). :contentReference[oaicite:7]{index=7} |
| **Bandwidth (BW)** | ~7.35 MHz | Derived from settling-time relation. :contentReference[oaicite:8]{index=8} |
| **Settling Time** | ~136 ns | Measured for a ±50mV step around Vin=850mV. :contentReference[oaicite:9]{index=9} :contentReference[oaicite:10]{index=10} |
| **Reference Current** | 3 uA | Chosen as **u3 = Iref** for headroom vs. operating range. :contentReference[oaicite:11]{index=11} :contentReference[oaicite:12]{index=12} |

## Project Contents (PDF)
The report covers the full design cycle:
* **Schematic Design:** 5T amplifier + source follower implementation. :contentReference[oaicite:13]{index=13}
* **DC Sweep & Saturation Analysis:** Tracking range and VDSAT margin verification.
* **Native NMOS Analysis:** Comparison vs. standard NMOS and impact on linear/tracking range. :contentReference[oaicite:14]{index=14}
* **Transient Analysis:** Step response for settling-time and speed. :contentReference[oaicite:15]{index=15} :contentReference[oaicite:16]{index=16}
* **Stability / Compensation:** Increasing capacitor at node **2N** from **0.5pF to 1pF** improved PM from **55° to 69°**. :contentReference[oaicite:17]{index=17} :contentReference[oaicite:18]{index=18}

## Tools Used
* **Cadence Virtuoso** (Schematic & ADE)
* **Spectre Simulator**
