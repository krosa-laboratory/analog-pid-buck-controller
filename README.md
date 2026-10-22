# Pure Analog Control Computer & Power Stage

Official repository for the design, simulation, and development of a **pure closed-loop analog control system** for a DC-DC power converter (24V to 5V buck converter), implemented using discrete operational amplifiers, double-integration networks, and an analog PID compensator.

## Project Purpose
This project demonstrates the fundamental principles of classical control theory and analog computing (inspired by flight control architectures and aerospace systems). The core of the system operates in continuous real time, completely eliminating the latency, sampling, and quantization limitations inherent in digital microcontrollers within the main feedback loop.

### System Architecture
1. **Power Stage and Main Circuit (Buck Converter):** Second-order LC filter (24 V to 5 V) with dynamics governed by continuous differential equations.
2. **Analog Controller (PID / Type II):** A feedback loop based on precision op-amps to ensure stability, disturbance rejection, and robust phase margins.
3. **Supervisor Subsystem (ATE - Automatic Test Equipment):** An external microcontroller dedicated exclusively to telemetry, voltage/current monitoring, and parameter adjustment via digital potentiometers, without ever interfering with the critical analog control loop.

## Repository Structure
- `/simulations`: Circuit models, netlists, and `.ac` / `.trans` analyses (integration drift analysis and Bode plots).
- `/hardware`: Schematic diagrams of the power and analog control blocks & Layout files, design rules (DRC), and ground plane isolation.
- `/docs`: Mathematical design notes, transfer functions, and critical data sheets.
