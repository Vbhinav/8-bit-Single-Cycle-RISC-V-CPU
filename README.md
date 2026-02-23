# 8-bit Single-Cycle CPU with 16-bit Instruction Format (Logisim)

## CPU Datapath
![CPU Datapath](images/CPU.png)

## Overview
This project implements a **custom 8-bit single-cycle CPU** designed and built using **Logisim**, with a **16-bit wide instruction format**.  
The CPU was developed from first principles to explore **processor architecture, datapath design, control logic, and memory-mapped peripheral interfacing**.

A key highlight of the design is the use of **memory-mapped I/O**, where all input and output devices are accessed directly through the data memory address space, without dedicated I/O ports. The processor also implements a **custom 5-bit character encoding scheme** to support alphanumeric and punctuation display.

---

## Architecture
- **Data width:** 8-bit  
- **Instruction width:** 16-bit  
- **Execution model:** Single-cycle  
- **Design tool:** Logisim  

### Core Components
- Program Counter (PC)
- Instruction Memory
- Register File (8-bit registers)
- Arithmetic Logic Unit (ALU)
- Control Unit
- Data Memory (with built-in I/O devices)
- Display Interface Logic

All stages of instruction execution—fetch, decode, execute, memory access, and write-back—are completed within **a single clock cycle**.

---

## Instruction Format
The CPU uses a **16-bit instruction encoding** to allow expressive control while operating on an 8-bit datapath.

Typical instruction fields include:
- Opcode
- Register specifiers
- Immediate / control fields

Instruction decoding and control signal generation are implemented using combinational logic constructed from basic gates, multiplexers, and decoders within Logisim.

---

## Instruction Set
The processor supports a **custom RISC-style instruction set**, adapted for an 8-bit architecture.

### Instruction Categories
- Arithmetic and logical operations  
- Register-to-register instructions  
- Immediate-based instructions  
- Control flow instructions (branch and jump)  
- Load and store instructions  

All data transfers to external devices are performed using standard load and store instructions through memory-mapped addresses.

---

## Memory-Mapped I/O Design
This CPU **does not use dedicated I/O ports**. Instead, all input and output devices are implemented as **memory-mapped peripherals** within the data memory space.

### Design Characteristics
- Input devices and output displays are assigned fixed memory addresses
- Read/write operations to these addresses trigger device interaction
- No special I/O instructions are required
- I/O access is handled using standard load/store semantics

This design mirrors real-world processor architectures and demonstrates an understanding of **memory-mapped I/O, address decoding, and system-level integration**.

---

## Custom 5-bit Character Encoding
To support text output, the CPU implements a **custom 5-bit character code** designed specifically for this system.

### Features
- Encodes **all alphabetic characters**
- Supports **selected punctuation symbols**
- Optimized for compact storage and simple decoding
- Directly mapped to display hardware through memory-mapped addresses

Character data written to specific memory locations is decoded and rendered by the display logic, enabling character and numeric output without external controllers.

---

## Verification & Testing
- Step-by-step verification of instruction execution in Logisim  
- Observation of internal datapath signals including registers, ALU outputs, and control lines  
- Validation of correct display output using the custom character encoding  
- Incremental testing of memory-mapped I/O behavior  

The system was verified module-by-module before full CPU integration.

---

## Tools Used
- **Logisim**

---

## Key Learnings
- Designing an **8-bit processor with a wider instruction encoding**
- Implementing **memory-mapped I/O** without dedicated ports
- Creating a **custom character encoding scheme**
- Translating instruction semantics into hardware-level control logic
- Understanding timing and limitations of single-cycle architectures

---

## Future Improvements
- Multi-cycle or pipelined CPU design  
- Interrupt handling support  
- Expanded character set and punctuation support  
- Migration to Verilog HDL and FPGA implementation  

---

## Author
**Abhinav Krishna**  
Electronics and Communication Engineering Undergraduate  

