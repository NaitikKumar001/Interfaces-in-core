#  soinc BOOM (Berkeley Out-of-Order Machine)

## Key Properties

| Property | Description |
|---|---|
| Full Name | Berkeley Out-of-Order Machine |
| Type | Processor Core |
| ISA | RISC-V |
| Architecture | 64-bit (RV64) |
| Execution | Out-of-Order Execution |
| Design Language | Chisel |
| Integration | Can be integrated into an SoC using the Rocket Chip framework |
| Main Purpose | Research, education, and high-performance processor design |

## Applications

- Computer Architecture Research
- RISC-V Processor Development
- System-on-Chip (SoC) Design
- Studying Advanced Processor Execution Techniques

- # Rocket Chip and Rocket Core

# Rocket chip

### Key Properties

| Property | Description |
|---|---|
| Type | SoC Generator Framework |
| ISA Support | RISC-V-based systems |
| Hardware Description | Chisel |
| Programming Language | Scala |
| Interconnect | TileLink |
| Main Purpose | Generate and integrate SoC hardware designs |
| Core Support | Rocket Core, BOOM, and other compatible cores |

### Applications

- RISC-V SoC development
- Processor integration
- Hardware architecture research
- FPGA and chip design experiments

# Rocket Core 

### Key Properties

| Property | Description |
|---|---|
| Type | Processor Core Generator |
| ISA | RISC-V |
| Execution | In-order |
| Pipeline | 5-stage pipeline |
| Hardware Description | Chisel |
| Integration | Rocket Chip framework |
| Interconnect | TileLink |
| Main Purpose | Execute RISC-V instructions |
| Configuration | Supports configurable processor and cache parameters |

| Core / Processor | ISA | Interconnect | Bus Protocol |
|---|---|---|---|
| Rocket Core | RISC-V | TileLink | TileLink |
| Microchip Mi-V | RV32IMA | AHB | AHB |
| Microchip Mi-V | RV32IMA | AXI | AXI |

# TileLink Interconnect Protocol


TileLink is an open-source interconnect protocol used to connect processor cores, caches, memory, and peripherals in a System-on-Chip (SoC).

It is commonly used in RISC-V-based systems, including Rocket Chip. It allows different hardware components to communicate by sending requests and receiving responses.

## Where Is TileLink Used?

TileLink is commonly used in RISC-V SoC designs, particularly those built using the Rocket Chip ecosystem.


## Key Properties

| Property | Description |
|---|---|
| Protocol Type | Hardware interconnect protocol |
| Main Purpose | Connect processor cores, memory, caches, and peripherals |
| Common Ecosystem | RISC-V and Rocket Chip |
| Communication | Request and response channels |
| Open Source | Open specifications and implementations are available |
| Cache Coherence | Supported by TileLink-C |
| Variants | TileLink-UL, TileLink-UH, and TileLink-C |
| Typical Use | On-chip communication in SoCs |
