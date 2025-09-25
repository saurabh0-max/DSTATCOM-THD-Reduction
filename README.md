# DSTATCOM for Power Quality Improvement

## Overview

This repository contains a MATLAB/Simulink implementation of a Distribution Static Compensator (DSTATCOM) designed to enhance power quality at the distribution level. The project focuses on mitigating current-related harmonics and improving voltage profiles in power systems affected by non-linear loads.

## Objective

This project implements and simulates a model to mitigate power quality problems. The primary goal is to compensate for current-related harmonics that are introduced into the power system by non-linear loads. The solution uses a Distribution Static Compensator (DSTATCOM) to improve the quality of the power at the distribution level.

## Technologies & Tools Used

- **Software:** The entire system is modeled and analyzed in the MATLAB and Simulink environment. It specifically uses the Simscape Electrical Specialized Power Systems toolbox, which requires the `powergui` block for simulation.
- **Core Technology:** A Voltage Source Converter (VSC) based DSTATCOM is implemented as the active power compensator. The converter is built with IGBT power switches for efficient and reliable operation.
- **Control Strategy:**
	- The DSTATCOM is controlled using the **Instantaneous Reactive Power Theory (IRPT)** algorithm, a robust time-domain control method.
	- Clarke Transforms are employed to estimate the required reference currents for harmonic compensation.
	- A **Hysteresis Current Controller** compares these reference currents to the actual sensed currents, generating precise PWM gating signals for the VSC.

## How to Run the Simulation

1. Open the `Main.slx` model file using MATLAB.
2. Run the simulation from the Simulink interface.
3. Observe the resulting waveforms for voltages and currents using the Scope blocks included in the model.
4. To analyze the harmonic content, use the FFT Analysis tool available within the `powergui` block.



---

For questions or contributions, please open an issue or submit a pull request.
