# 1. Introduction.

VexRiscv is an open-source, 32-bit RISC-V processor implementation written using SpinalHDL. It is designed to be FPGA-friendly and highly configurable.

Unlike a fixed processor design, VexRiscv uses a plugin-based architecture. This allows developers to add, remove, or modify features such as multiplication, division, caches, debugging, and pipeline hazard handling.

# Interconnect and Bus Interfaces

VexRiscv supports multiple interface options, depending on the selected configuration and integration.

| Interface | Main Purpose | Typical Use |
|---|---|---|
| Wishbone | Connects the processor to memory and other hardware components | Small FPGA-based SoCs |
| AXI4 | Supports memory transactions and communication with other system components | Higher-performance FPGA systems |
| Avalon | Connects processor interfaces to compatible memory and peripherals | FPGA systems using Intel FPGA tools |
