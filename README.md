# Isolated DC-DC Converter

Design, simulation, PCB implementation, and experimental evaluation of a
100 W isolated DC-DC converter developed as a Bachelor's thesis project.

## Project Overview

This project focuses on the design and implementation of an isolated DC-DC
converter capable of stepping up a 20 V input to an 80 V output.

The converter was designed for a 100 W output power and a switching frequency
of 100 kHz. MATLAB/Simulink was used to model and simulate the converter,
followed by PCB implementation and hardware testing.

## Design Specifications

| Parameter | Value |
|---|---:|
| Input voltage | 20 V |
| Output voltage | 80 V |
| Output power | 100 W |
| Switching frequency | 100 kHz |
| Transformer turns ratio | 1:4 |
| Inductors | 180 µH each |
| Output capacitor | 22 µF |

## Converter Topology

The proposed converter uses three active MOSFET switches and two equal
inductors.

The inductors are charged in parallel during the energy-storage intervals
and subsequently discharged in series during the energy-transfer interval.
A high-frequency transformer provides galvanic isolation and voltage step-up.

The converter operates through three main switching modes:

1. Energy storage with the inductors connected to the input.
2. Continued inductor charging while the output capacitor supplies the load.
3. Energy transfer from the inductors to the high-voltage output.

## Design and Analysis

The project involved:

- Converter topology analysis
- Inductor and capacitor sizing
- Transformer turns-ratio selection
- Semiconductor switch selection
- Voltage-stress analysis
- Current and voltage ripple analysis
- Efficiency analysis
- MATLAB/Simulink modelling

The design targeted approximately 10% inductor-current ripple and 2% output
voltage ripple.

## Simulation

The converter was modelled and simulated in MATLAB/Simulink.

The simulation examined:

- MOSFET gate signals
- Inductor currents
- Primary and secondary currents
- Capacitor and load currents
- Inductor voltage
- Input and output voltages
- Steady-state converter behaviour

The documented simulation uses duty ratios of D1 = 0.50 and D2 = 0.25 at
100 kHz. :contentReference[oaicite:2]{index=2}

## Hardware Implementation

A PCB prototype was designed and fabricated based on the proposed converter
topology.

The hardware implementation included:

- Power-stage PCB
- MOSFET switches
- High-frequency transformer
- Two inductors
- Output capacitor
- Separate gate-driver circuitry
- Variable resistive load
- DC power supplies

The hardware design also considered PCB routing, loop area, EMI, grounding,
and MOSFET thermal management. :contentReference[oaicite:3]{index=3}

## Results

The thesis reports an approximately 80 V output from a 20 V input in the
simulation, with an output-voltage ripple target of approximately 1.6 V
(2% of 80 V). :contentReference[oaicite:4]{index=4}

The hardware implementation used the same nominal 20 V input, 100 kHz
switching frequency, 180 µH inductors, and 22 µF capacitor specified for
the design. :contentReference[oaicite:5]{index=5}

## Project Structure

```text
isolated-dc-dc-converter/
│
├── README.md
│
├── docs/
│   └── project-summary.pdf
│
├── simulation/
│   ├── cap_mainckt.slx
│   └── figures/
│
├── hardware/
│   ├── pcb/
│   ├── photos/
│   └── gerbers/
│
└── results/
    └── figures/
