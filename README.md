# 4-Input XNOR Gate using 2x1 MUX

## Overview

This project presents the design and implementation of a **4-input XNOR gate** using cascaded **2x1 Multiplexers** at transistor level. The complete custom VLSI design flow was performed including schematic design, ELDO simulation, layout design, DRC/LVS verification, post-layout analysis, and Monte Carlo simulations.

* Vishal Kumar Singh (MT25157)

### Guided By
Anuj Grover

# Design Overview

The logic was implemented using:

* Cascaded 2x1 Multiplexers
* CMOS transistor-level design

### Technology Parameters

| Parameter      | Value   |
| -------------- | ------- |
| PMOS Width     | 0.54 µm |
| NMOS Width     | 0.27 µm |
| Channel Length | 0.06 µm |
| Supply Voltage | 1.08V   |

---

# Design Flow

The project included:

1. Schematic Design in Virtuoso
2. ELDO Simulation
3. Delay Verification
4. Layout Design
5. DRC & LVS Verification
6. Pre-layout and Post-layout Analysis
7. Monte Carlo Simulation

---

# Verification Methodology

Input stimuli were designed such that:

* All 16 possible input combinations were verified
* Individual input delays were measured accurately
* Other inputs remained constant during delay measurement

### Delay Measurement

Propagation delays were measured at:

* 50% input transition
* 50% output transition

---

# Pre-Layout Delay Results

| Input | TPLH      | TPHL      | TPD       |
| ----- | --------- | --------- | --------- |
| A     | 548.44 ps | 362.85 ps | 455.65 ps |
| B     | 568.43 ps | 377.44 ps | 472.93 ps |
| C     | 561.14 ps | 367.07 ps | 464.10 ps |
| D     | 447.33 ps | 378.80 ps | 413.06 ps |

---

# Post-Layout Delay Results

| Input | TPLH      | TPHL      | TPD       |
| ----- | --------- | --------- | --------- |
| A     | 656.13 ps | 418.08 ps | 537.11 ps |
| B     | 668.82 ps | 432.36 ps | 550.59 ps |
| C     | 650.00 ps | 416.05 ps | 533.03 ps |
| D     | 517.83 ps | 432.26 ps | 475.04 ps |

---

# Power Analysis

## Pre-Layout Power

| Condition        | Total Power |
| ---------------- | ----------- |
| SS, 1.08V, 125°C | 2.11 µW     |
| FF, 1.32V, -40°C | 2.90 µW     |

## Post-Layout Power

| Condition        | Total Power |
| ---------------- | ----------- |
| SS, 1.08V, 125°C | 2.58 µW     |
| FF, 1.32V, -40°C | 3.59 µW     |

---

# Layout Details

## 2x1 MUX Layout

* Final Tracks: 13
* Area: 6.76 µm²

## 4-Input XNOR Layout

* Final Tracks: 70
* Area: 36.40 µm²

### Improvements Made

* Proper routing on tracks
* Increased VDD/GND width
* Pins covering minimum two tracks
* Fixed SCONNECT LVS issues

---

# DRC & LVS Verification

Successfully completed:

* DRC Clean Layout
* LVS Matched Schematic and Layout

---

# Monte Carlo Simulations

Monte Carlo simulations were performed for:

* Delay variation analysis
* Power variation analysis
* PVT corner verification

### PVT Conditions

* SS, 125°C, 1.08V
* FF, -40°C, 1.32V

---

# Tools Used

| Stage             | Tool             |
| ----------------- | ---------------- |
| Schematic Design  | Cadence Virtuoso |
| Simulation        | ELDO             |
| Waveform Analysis | EZwave           |
| Layout Design     | Virtuoso Layout  |
| DRC/LVS           | Calibre          |

---

# Key Learnings

* Custom CMOS logic design
* Delay and power optimization
* Layout design constraints
* DRC/LVS debugging
* Post-layout parasitic effects
* Monte Carlo and PVT analysis

---

# Conclusion

The project successfully implemented a 4-input XNOR gate using 2x1 multiplexers at transistor level. The design was verified through schematic simulations, layout verification, post-layout analysis, and Monte Carlo simulations, demonstrating correct functionality and reliable performance across different PVT corners.
