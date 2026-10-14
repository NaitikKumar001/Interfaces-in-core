# SERV RISC-V Core

SERV is an open-source, ultra-small RISC-V CPU core designed to minimize hardware resource usage. It uses a **bit-serial architecture**, meaning it processes data one bit at a time across multiple clock cycles instead of using a conventional full-width datapath.

This approach makes SERV extremely compact, but arithmetic operations generally take more clock cycles, resulting in lower processing throughput.

## Properties

| Property | Description |
|---|---|
| Core Name | SERV |
| ISA | RV32I |
| Architecture | 32-bit RISC-V |
| Processing Style | Bit-serial |
| Main Goal | Minimize hardware resource usage |
| Performance | Low throughput compared with conventional 32-bit cores |
| Hardware Footprint | Extremely small |
| Typical Platform | FPGA |
| Main Trade-off | Lower execution speed in exchange for smaller hardware size |
| Source Code | Verilog |

# PicoRV32 RISC-V Core

PicoRV32 is an open-source, size-optimized RISC-V CPU core designed for FPGA-based systems and embedded applications. It executes 32-bit RISC-V instructions and provides a balance between small hardware size and practical processing performance.

It uses a conventional 32-bit datapath and supports different ISA configurations. Its interface variants allow it to connect with different system interconnects.

## Properties

| Property | Description |
|---|---|
| Core Name | PicoRV32 |
| ISA | RV32I, RV32E, RV32IC, RV32IM, RV32IMC (configurable) |
| Architecture | 32-bit RISC-V |
| Processing Style | Conventional 32-bit datapath |
| Main Goal | Small hardware footprint with practical performance |
| Performance | Moderate; depends on configuration and clock frequency |
| Hardware Footprint | Approximately 750–2,000 LUTs on Xilinx 7-Series FPGAs, depending on configuration |
| Typical Platform | FPGA and ASIC |
| Source Code | Verilog |
| License | ISC |

## PicoRV32 Variants

| Variant | Interface | Purpose |
|---|---|---|
| `picorv32` | Native memory interface | Simple memory access |
| `picorv32_axi` | AXI4-Lite master | Integration with AXI-based systems |
| `picorv32_wb` | Wishbone master | Integration with Wishbone-based systems |



# What type of Interconnect they use?
SERV and PICORV32_wb use 'WISHBONE' like simple communication protocol. Because SERV it self is very simple and low-bandwidth Core so Wishbone is perfect for it

# Wishbone Interconnect Protocol

## Overview

Wishbone is an open-source hardware interconnect protocol used to connect components such as processors, RAM, ROM, and peripherals. It defines common rules that allow different hardware components to communicate with each other.


## Important Signals

| Signal | Purpose |
|---|---|
| `ADR` | Specifies the address |
| `DAT_O` | Carries data from the master to the slave |
| `DAT_I` | Carries data from the slave to the master |
| `WE` | Selects a read or write operation |
| `CYC` | Indicates an active bus cycle |
| `STB` | Indicates an active transfer request |
| `ACK` | Indicates transfer completion |

## Where Is Wishbone Used?

- Connecting RISC-V processors to memory and peripherals.
- FPGA-based hardware designs.
- Open-source processor and SoC projects.
- Custom hardware systems.
- Connecting compatible hardware IP blocks.

 ## Key Properties

| Property | Description |
|---|---|
| Protocol Type | Open-source hardware interconnect |
| Main Purpose | Communication between hardware components |
| Communication Model | Master–Slave |
| Operations | Read and write |
| Timing | Supports synchronous and other defined interface options |
| Complexity | Relatively simple in basic configurations |
| Common Applications | FPGA designs, open-source CPUs, and SoCs |
