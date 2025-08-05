# Single Cycle Datapath – MIPS Architecture

## Author
**Kumar Krishna**  
BITS ID: 2022A3PS0392P

## Overview
This project implements a **Single Cycle Datapath** for the MIPS processor in **Verilog**. It includes individual modules for all hardware components and integrates them into a cohesive datapath.

The design is based on the classical MIPS architecture and is developed as part of Lab Sheet 6 from the course **Computer Architecture** at **BITS Pilani**.

## Objectives
- Model the MIPS single-cycle datapath in Verilog.
- Develop individual Verilog modules for:
  - Instruction Memory
  - Register File
  - ALU
  - Control Unit and ALU Control
  - Data Memory
  - Sign Extender
  - Shifter
  - Adders (for PC computation)
  - Multiplexers
- Integrate all modules in a top-level module: `SCDataPath`.
- Test the datapath using a `TestBench` for R-format instruction execution.

## Files
- `SCDataPath.v`: Main module that integrates all components.
- `InstructionMemory.v`: Module to read instructions.
- `RegisterFile.v`: Handles reading and writing to registers.
- `ALU.v`: Performs arithmetic and logic operations.
- `ControlUnit.v` and `ALUControl.v`: Generate control signals based on opcode and funct fields.
- `DataMemory.v`: (Prepared for lw/sw instructions)
- `SignExtender.v`, `Shifter.v`, `Adders.v`, `Mux.v`: Supporting components.
- `TestBench.v`: Benchmarks and verifies correct ALU output using sample instructions.

## TestBench Functionality
The testbench provides:
- Clock generation and reset logic.
- Instantiates the complete datapath.
- Monitors key outputs such as ALU result and PC value.
- Designed for simulation using tools like ModelSim, Xilinx Vivado, or Icarus Verilog.

## How to Run
1. Compile all Verilog modules including `SCDataPath.v` and `TestBench.v`.
2. Run the simulation.
3. Observe ALU output and PC updates for R-format instructions in the waveform or simulation log.

### Example Simulation Output
