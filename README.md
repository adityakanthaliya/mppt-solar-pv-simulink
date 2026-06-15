# Maximum Power Point Tracking System for Solar PV using MATLAB/Simulink

This repository documents an academic simulation project on Maximum Power Point Tracking for solar photovoltaic systems using MATLAB/Simulink.

The project focuses on studying, modelling, and simulating MPPT techniques that help solar PV systems extract maximum available power under changing irradiance and temperature conditions.

---

## Overview

Solar photovoltaic systems do not always operate at their maximum power point because their output depends on environmental conditions such as sunlight intensity and temperature.

This project studies Maximum Power Point Tracking techniques that help a solar PV system operate closer to its optimal power point.

Two classical MPPT algorithms were studied and simulated:

- Perturb and Observe
- Incremental Conductance

The system was modelled in MATLAB/Simulink using a PV array, DC-DC boost converter, measurement blocks, MPPT algorithm blocks, and duty cycle control.

---

## Problem Statement

Solar PV cells have non-linear voltage-current and power-voltage characteristics. Their maximum power point changes with irradiance and temperature.

Without MPPT, the system may operate away from the optimal point, reducing the total power extracted from the solar panel.

The objective of this project was to model and simulate MPPT techniques that can track the maximum power point and improve solar energy utilization.

---

## Objectives

- Study the need for renewable energy and solar photovoltaic systems.
- Understand the working and modelling of PV cells, modules, panels, and arrays.
- Study the role of DC-DC converters in MPPT-based PV systems.
- Compare buck, boost, and buck-boost converter topologies.
- Implement and simulate two MPPT algorithms:
  - Perturb and Observe
  - Incremental Conductance
- Build a MATLAB/Simulink model of the MPPT system.
- Analyze system performance under constant and changing irradiance/temperature conditions.
- Compare the behaviour of both MPPT techniques using simulation results.

---

## Tools & Technologies Used

- MATLAB
- Simulink
- Simscape Electrical
- MATLAB Function Block
- PV Array Block
- Boost Converter Block
- Signal Builder
- Scope and Display Blocks
- Simulink Data Inspector

---

## System Components

The Simulink model consisted of the following major components:

- Solar PV array model
- Irradiance and temperature input generation
- DC-DC boost converter
- Voltage and current measurement blocks
- Power calculation block
- MPPT algorithm block
- Duty cycle control
- Scope and display blocks for output visualization

The model was also modified to allow switching between MPPT algorithms using variant and triggered subsystems.

---

## MPPT Algorithms Studied

### Perturb and Observe

Perturb and Observe is one of the most widely used MPPT algorithms because of its simplicity.

The algorithm continuously perturbs the operating voltage and observes the corresponding change in output power. Based on whether the power increases or decreases, the operating point is moved toward the maximum power point.

However, under rapidly changing irradiance conditions, this method can sometimes track inaccurately because it may interpret environmental changes as the result of its own perturbation.

### Incremental Conductance

Incremental Conductance improves upon the Perturb and Observe method under rapidly changing atmospheric conditions.

It uses voltage and current samples to determine whether the operating point has reached the maximum power point. This allows the algorithm to better track changes in irradiance.

The main trade-off is that Incremental Conductance is more complex than Perturb and Observe.

---

## Methodology

The project followed a simulation-based research approach.

1. Studied renewable energy sources with a focus on solar photovoltaic systems.
2. Reviewed MPPT techniques from research papers, journals, NPTEL lectures, MathWorks learning tools, and online tutorials.
3. Studied PV cell modelling concepts such as:
   - short-circuit current
   - open-circuit voltage
   - fill factor
   - maximum power point
   - irradiance and temperature dependency
4. Compared DC-DC converter topologies used in solar PV systems.
5. Selected a boost converter for the MPPT model due to its simplicity and ability to step up PV output voltage.
6. Built a PV array model in MATLAB/Simulink.
7. Added signal inputs to simulate constant, step, and ramp-up/down irradiance conditions.
8. Implemented Perturb and Observe and Incremental Conductance algorithms using MATLAB Function Blocks.
9. Connected the MPPT algorithm output to the duty cycle input of the boost converter.
10. Simulated the system under constant and rapidly changing environmental conditions.
11. Compared output waveforms using scopes and Simulink Data Inspector.

---

## Simulation Scenarios

### Case 1: Constant Temperature and Irradiance

The system was simulated at constant temperature and irradiance. In this condition, both Perturb and Observe and Incremental Conductance showed similar results.

### Case 2: Rapidly Changing Temperature and Irradiance

The system was also tested under changing irradiance and temperature conditions. Differences were observed between the two MPPT techniques, especially in tracking behaviour and steady-state oscillations.

---

## Results

The simulation results were consistent with the literature reviewed during the project.

Key observations:

- Both algorithms were able to track the maximum power point under stable conditions.
- Under constant irradiance, both techniques produced similar output.
- Under changing irradiance, differences were observed between Perturb and Observe and Incremental Conductance.
- Steady-state oscillations were observed around the maximum power point.
- The simulated algorithms were able to harvest approximately 94–96% of the solar energy incident on the solar modules.
- The project helped compare the behaviour of classical MPPT techniques in a controlled simulation environment.

---

## Key Learnings

Through this project, I learned:

- Why renewable energy systems require power optimization techniques.
- How solar PV output varies with irradiance and temperature.
- How photovoltaic cells, modules, panels, and arrays are modelled.
- The importance of maximum power point tracking in solar PV systems.
- The role of DC-DC converters in transferring maximum power from a PV module to a load.
- The difference between buck, boost, and buck-boost converter topologies.
- How Perturb and Observe and Incremental Conductance algorithms work.
- How to build and analyze simulation models in MATLAB/Simulink.
- How to interpret simulation outputs using scopes and Simulink Data Inspector.
- The trade-off between algorithm simplicity and tracking accuracy.

---

## Limitations

- The project was simulation-based and did not include hardware implementation.
- Only two classical MPPT algorithms were implemented.
- Advanced MPPT techniques such as fuzzy logic, neural network-based MPPT, and hybrid methods were not implemented.
- The model was tested in a simulation environment, not with real-world solar panel data.
- Steady-state oscillations were observed around the maximum power point.
- The project focused more on understanding and simulation rather than product-level implementation.

---

## Future Scope

The project can be extended in the following ways:

- Implement advanced MPPT techniques such as fuzzy logic or neural network-based MPPT.
- Compare classical and intelligent MPPT techniques under dynamic weather conditions.
- Use real-world solar irradiance and temperature datasets for testing.
- Reduce steady-state oscillations around the maximum power point.
- Build a hardware prototype using:
  - solar panel
  - DC-DC converter
  - voltage and current sensors
  - microcontroller
  - PWM control
- Compare simulation results with hardware output.
- Explore hybrid MPPT techniques for better accuracy and faster response.

---

## Repository Contents

```text
mppt-solar-pv-simulink/
│
├── README.md
├── docs/
│   └── mppt-solar-pv-project-report-public.pdf
│
└── references/
    └── references.md
