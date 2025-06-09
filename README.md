# Protection-Coordination-in-a-Smart-Microgrid-System



## Project Overview

This project focuses on the design and simulation of protection coordination strategies for smart microgrid systems. With the increasing penetration of distributed energy resources (DERs) such as solar, wind, and energy storage, microgrids require sophisticated protection schemes to ensure reliability, safety, and seamless operation during faults and islanding conditions.

The goal is to develop a coordinated protection system that effectively detects and isolates faults, minimizes downtime, and ensures stable operation of both grid-connected and islanded microgrid modes.

---

## Table of Contents
- [Background](#background)
- [Objectives](#objectives)
- [System Architecture](#system-architecture)
- [Key Features](#key-features)
- [Protection Devices and Settings](#protection-devices-and-settings)
- [Simulation Setup](#simulation-setup)
- [Results and Analysis](#results-and-analysis)
- [Technologies Used](#technologies-used)
- [Usage Instructions](#usage-instructions)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Background

Smart microgrids integrate multiple distributed generation sources and loads with advanced control and communication technologies. Protection coordination in such systems is critical to quickly isolate faults while maintaining service continuity to unaffected loads. Traditional protection schemes often fail due to bidirectional power flow and variable system configurations.

This project explores adaptive and coordinated protection schemes using time-current characteristic curves, directional relays, and communication-assisted tripping.

---

## Objectives

- Design an adaptive protection coordination scheme tailored for smart microgrid architectures.
- Model key protection devices including relays, circuit breakers, and fuses.
- Simulate fault scenarios such as short circuits, islanding events, and load changes.
- Optimize relay settings to minimize fault clearing time and avoid nuisance tripping.
- Evaluate system stability and protection reliability under varied operating conditions.

---

## System Architecture

The smart microgrid modeled includes:

| Component                | Description                                      |
|--------------------------|-------------------------------------------------|
| Distributed Generators   | Solar PV, wind turbines, and battery storage     |
| Loads                   | Residential, commercial, and critical loads       |
| Protection Devices      | Overcurrent relays, directional relays, breakers |
| Communication Network   | For relay coordination and adaptive settings      |
| Control Center          | Monitors microgrid operation and fault events     |

---

## Key Features

- **Adaptive Relay Settings:** Dynamic adjustment based on microgrid mode (grid-connected or islanded).
- **Directional Overcurrent Protection:** Ensures correct fault direction identification.
- **Communication-Assisted Coordination:** Uses IEC 61850 protocols for relay communication and coordination.
- **Fault Detection and Isolation:** Fast and selective clearing to minimize service interruption.
- **Simulation of Various Fault Types:** Including line-to-ground, line-to-line, and three-phase faults.
- **Integration with Microgrid Control:** Seamless switching between grid-tied and islanded modes.

---

## Protection Devices and Settings

| Device               | Setting Parameter        | Typical Value     | Description                       |
|----------------------|--------------------------|-------------------|---------------------------------|
| Overcurrent Relay    | Pickup Current (Ip)       | 1.2 × Load Current | Minimum current to trigger relay|
| Time Dial Setting (TDS) | 0.1 - 1.0               | Defines relay operating time   |
| Directional Relay    | Phase Angle Threshold     | 30°               | Determines fault direction       |
| Circuit Breaker      | Trip Time                 | < 100 ms          | Breaker operating speed          |

---

## Simulation Setup

- Modeled the microgrid system using MATLAB/Simulink and Simscape Power Systems.
- Incorporated protection relay logic with time-current characteristic curves.
- Simulated fault conditions at various points in the network under different microgrid modes.
- Tested relay coordination with and without communication assistance.
- Logged relay operating times, fault currents, and system voltages for analysis.

---

## Results and Analysis

- Coordinated protection scheme effectively cleared faults within specified time limits.
- Adaptive relay settings ensured proper operation during islanded and grid-connected modes.
- Communication-assisted coordination reduced fault isolation time by 20% compared to traditional schemes.
- Nuisance trips minimized through directional relay implementation.
- System stability maintained during simulated transient events.

### Sample Time-Current Characteristic Curve

![TCC Curve](docs/tcc_curve.png)

### Fault Clearing Times Summary

| Fault Type           | Clearing Time (Traditional) | Clearing Time (Adaptive) |
|----------------------|-----------------------------|-------------------------|
| Line-to-Ground       | 500 ms                      | 350 ms                  |
| Line-to-Line         | 400 ms                      | 280 ms                  |
| Three-Phase          | 350 ms                      | 250 ms                  |

---

## Technologies Used

- MATLAB / Simulink
- Simscape Electrical / Power Systems Toolbox
- IEC 61850 Protocol Simulation
- Relay Coordination Algorithms (implemented via MATLAB scripts)

---

## Usage Instructions

1. Clone the repository:

```bash
git clone https://github.com/yourusername/smart-microgrid-protection.git
cd smart-microgrid-protection
