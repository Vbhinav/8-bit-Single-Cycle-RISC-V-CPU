# 8-bit Single-Cycle RISC-V–Inspired CPU with Custom Display Interface

## Overview
This project implements a **custom 8-bit single-cycle CPU** designed and developed in **Verilog HDL**, using a **16-bit wide instruction format**.  
The processor was built from scratch with a focus on **instruction execution flow, control logic, and peripheral interfacing**, and was extended to communicate with **custom character and numeric display modules using self-designed communication protocols**.

The project emphasizes **low-level digital system design**, including datapath construction, control signal generation, and timing-aware interfacing with external hardware.

---

## Architecture
- **Data width:** 8-bit  
- **Instruction width:** 16-bit  
- **Execution model:** Single-cycle  
- **Design language:** Verilog HDL  
- **Target platform:** FPGA (tested using Intel Quartus Prime)

### Core Components
- Program Counter (PC)
- Instruction Memory
- Register File (8-bit registers)
- Arithmetic Logic Unit (ALU)
- Control Unit
- Data Memory
- Custom I/O Interface Controller

The CPU follows a **single-cycle datapath**, where instruction fetch, decode, execute, memory access, and write-back are completed within one clock cycle.

---

## Instruction Set
The processor supports a **custom RISC-V–inspired instruction set**, adapted for:
- **8-bit data operations**
- **16-bit instruction encoding**

### Instruction Categories
- Arithmetic and logical operations  
- Register-to-register instructions  
- Immediate-based instructions  
- Control flow instructions (branches / jumps)  
- Load and store instructions  

Instruction decoding and control signal generation are implemented using combinational logic derived from opcode and function fields within the 16-bit instruction word.

---

## Custom Display Interface
A key feature of this project is the design of **custom communication protocols** to interface the CPU with:
- A character display module  
- A numeric display module  

### Design Highlights
- Proprietary protocol designed to meet timing and resource constraints  
- Dedicated control logic for data framing and synchronization  
- Clear separation between CPU core logic and peripheral interface logic  

This approach avoids reliance on standard protocols and demonstrates **protocol-level design, synchronization, and timing analysis**.

---

## Verification & Debugging
- Functional verification performed through **simulation** and FPGA testing  
- Internal signals monitored using **SignalTap Logic Analyzer**  
- Incremental module-level testing before full system integration  

Special attention was given to:
- Correct instruction execution  
- Control signal timing  
- Reliable communication with external display peripherals  

---

## Tools Used
- **Verilog HDL**
- **Intel Quartus Prime**
- **SignalTap Logic Analyzer**
- ModelSim (for simulation)

---

## Key Learnings
- Designing an **8-bit processor datapath** with a wider instruction encoding  
- Translating instruction-level behavior into hardware control signals  
- Designing and debugging **custom hardware communication protocols**  
- Understanding timing, synchronization, and system-level integration on FPGA  

---

## Future Improvements
- Pipelined version of the CPU  
- Interrupt support  
- Expansion of the instruction set  
- Standardized peripheral bus interface  

---

## Author
**Abhinav Krishna**  
Electronics and Communication Engineering Undergraduate  

Interests:  
- Digital Electronics & FPGA Design  
- Processor Architecture  
- Embedded Systems  
- Hardware-Aware Cybersecurity
