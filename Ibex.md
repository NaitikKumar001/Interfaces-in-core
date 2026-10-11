## What is Ibex?

Ibex is a small, open-source, 32-bit RISC-V CPU core developed and maintained by lowRISC.

It is an actual hardware implementation of the RISC-V Instruction Set Architecture (ISA).

The Ibex core is designed to support the standard **RV32I (40 base integer instructions)** or **RV32E (16 base instructions)** instruction sets, expandable to **over 100 instructions** depending on the enabled extensions.

# Existence of Interface in Ibex.

Ibex already has built-in interfaces, such as instruction memory, data memory, interrupt, and debug interfaces.


However, it does not include standard GPIO, UART, SPI, or I²C peripheral controllers inside the CPU core.
When designing a SoC using Ibex, we add the required peripheral controllers and connect them to the core through a suitable interconnect or adapter.

In simple words:
Ibex provides basic interfaces to communicate with memory and other system components. The SoC designer adds the additional interfaces and peripherals required for the application.

# SOC design with different Interfaces 

# Temperature monitoring SoC
  
