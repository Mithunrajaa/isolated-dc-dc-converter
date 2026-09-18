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

## Simulation

The converter was modelled and simulated in MATLAB/Simulink.

The simulation was used to examine the switching behaviour, inductor currents,
transformer currents, and input/output voltage characteristics.

### Simulink Model

![Converter simulation model](simulation/converter_model.jpg)

### Gate Signals

![Gate signals](simulation/gate_signals.jpg)

### Inductor Currents

![Inductor currents](simulation/inductor_currents.jpg)

### Primary and Secondary Currents

![Primary and secondary currents](simulation/primary_secondary_currents.jpg)

## Hardware Implementation

A hardware prototype of the converter was developed and experimentally
evaluated following the simulation and design stages.

The hardware implementation included the power stage, high-frequency
transformer, inductors, switching devices, gate-driver circuitry, and
supporting measurement and power-supply equipment.

### Hardware Setup

![Hardware setup](hardware/photos/hardware_setup.jpg)

## Results

The simulation results were evaluated using the converter's key electrical
waveforms.

### Input and Output Voltage

![Input and output voltage](results/input_output_voltage.jpg)

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
│   ├── Main_circuit.slx
│   └── figures/
│
├── hardware/
│   ├── pcb/
│   ├── photos/
│   └── gerbers/
│
└── results/
    └── figures/
