# Modelling and Control of a DC Microgrid

This repository contains the design, modelling, and control implementation of a 48 V DC microgrid integrating renewable energy sources and hybrid energy storage to ensure stable, reliable, and efficient off-grid power delivery. The system is developed in MATLAB/Simulink and demonstrates coordinated converter control, energy management, and DC bus voltage regulation under variable load and fluctuating renewable generation.

---

## ⚡ System Overview

The DC microgrid integrates the following components:

- **Solar PV Array** – primary renewable source with MPPT-controlled boost converter
- **Wind Generator** – secondary renewable source with AC–DC conversion and MPPT
- **Battery** – long-term energy storage for slow power fluctuations
- **Supercapacitor** – high-power storage for fast transient support
- **Hybrid Energy Storage System (HESS)** – coordinated use of battery + supercapacitor
- **48 V DC Bus** – regulated bus supplying a variable residential/apartment-type load

The system aims to maintain a constant 48 V DC bus voltage while meeting the varying load demand and compensating for intermittent solar and wind power generation.

---

## 🧠 Control & Energy Management

### 1. Maximum Power Point Tracking (MPPT)

MPPT algorithms are implemented to maximise renewable power harvesting:

- PV MPPT using **Perturb & Observe (P&O)** or **Incremental Conductance (INC)**
- Wind MPPT using **Tip-Speed Ratio (TSR)** or power-coefficient-based control

### 2. Converter-Level Control

All converters are PWM-controlled and designed for dynamic and stable operation:

- **Boost Converters (PV & Wind):** regulate input voltage and track maximum power
- **Bidirectional Buck-Boost Converter (Battery):** handles charging/discharging to balance load and generation
- **Supercapacitor Converter:** responds rapidly to transients to stabilise the DC bus

### 3. Energy Management System (EMS)

The EMS coordinates power flow among renewables and storage:

- Allocates **low-frequency** power balancing to the battery
- Assigns **high-frequency** transient support to the supercapacitor
- Ensures efficient use of storage, protects battery health, and improves stability

---

## 🔍 Key Features

- 48 V DC microgrid suitable for small-scale residential or off-grid applications
- Variable load demand profile for realistic operation
- Hybrid energy storage for enhanced performance, stability, and battery longevity
- Integrated MPPT, converter control, and EMS
- Modular architecture allowing system expansion

---

## 📂 Repository Structure


---

## 📊 Simulation Capabilities

This model enables simulation and analysis of the following:

- PV and wind variability and weather-dependent power production
- EMS response to changing load and renewable conditions
- DC bus voltage stability and transient behaviour
- Battery State of Charge (SoC) and supercapacitor energy usage
- Converter duty cycles and closed-loop control responses

---

## 🚀 Future Enhancements

Planned or recommended improvements include:

- Model Predictive Control (MPC) for enhanced DC bus regulation
- DC fault detection, isolation, and protection system
- Hardware-in-the-Loop (HIL) implementation
- AI-assisted forecasting for EMS optimisation

---

## 🧑‍💻 Requirements

- MATLAB R2022b or later
- Simulink + Simscape Electrical
- Control System Toolbox


