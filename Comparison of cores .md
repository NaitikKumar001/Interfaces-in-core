## 1. Complete RISC-V Core Comparison

| RISC-V Core | Why It Was Designed / Main Purpose | Architecture & Performance | Best-Suited Application Fields | Main Trade-off |
|---|---|---|---|---|
| Shakti | A processor family designed for different application requirements | Depends on the processor class; performance varies by implementation | Embedded systems, controllers, and higher-performance systems | The appropriate processor class must be selected |
| SERV | To achieve an extremely small hardware footprint | Bit-serial architecture; low throughput | Tiny IoT controllers, area-constrained FPGA designs, and education | Extremely small area but slow execution |
| PicoRV32 | To provide a simple and compact RISC-V implementation | Small, multi-cycle processor | Small FPGA projects, simple SoCs, and control applications | Low resource usage but lower throughput than advanced cores |
| Ibex | To provide a small, practical embedded processor with configurable features | RV32, typically a 2-stage in-order pipeline | Embedded controllers, secure devices, and microcontrollers | Good area-performance balance but not designed as a high-end application core |
| Vega | The exact design purpose depends on the specific Vega implementation | Specifications and performance require identification of the exact project | Depends on the intended Vega core | Cannot be compared accurately until the exact implementation is identified |
| CV32E40P | To provide embedded compute performance with support for DSP-oriented workloads | RV32, 4-stage in-order pipeline | IoT, embedded signal processing, and real-time control | More hardware complexity than minimal cores |
| Rocket Core | To provide a configurable general-purpose RISC-V processor for SoCs and research | Typically a 5-stage in-order pipeline; configurations vary | Linux-capable SoCs, research, FPGA prototypes, and general-purpose computing | More complex than minimal embedded cores |
| SweRV EH1 | To provide high instruction throughput for embedded workloads | RV32, 9-stage, dual-issue, in-order pipeline | Networking, storage controllers, and embedded computing | Higher area and design complexity |
| VexRiscv | To provide a highly configurable processor for FPGA and SoC development | Configurable pipeline, plugins, and extensions | FPGA prototyping, custom SoCs, and processor experiments | Performance, area, and features depend on configuration |
| SonicBOOM | To explore high-performance general-purpose CPU architecture | Superscalar, out-of-order execution | Advanced CPU research, high-performance prototypes, and demanding compute workloads | High hardware complexity, area, power, and verification requirements |
