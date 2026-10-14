#  Smartwatch SoC

Purpose: Read health and motion sensors, update the display, detect button presses, and communicate with debugging equipment.
```
Internal architecture
```
```
           Low-power CPU
                |
      AHB or AXI-Lite interconnect
                |
         APB bridge (optional)

I²C controller.         SPI Controller 

GPIO Controller.        UART Controller
```
# How each interface works

```I²C``` — sensor communication
The CPU configures the I²C controller through internal registers. The controller reads heart-rate or motion data from a compatible sensor over SDA and SCL. The CPU then processes the reading.

```SPI``` — display communication
The CPU or display driver sends pixel data and commands through an SPI controller. Clock, data, and chip-select signals coordinate the transfer. SPI can be useful when a display needs more data throughput than a simple sensor does.

```GPIO ```— buttons and status signals
A button can be connected to a GPIO configured as an input. Pressing it changes the input level, which software can detect. A GPIO configured as an output can switch an LED or another compatible digital signal.

```UART``` — debugging
The UART controller sends serial text to a compatible external serial adapter or debug module through TX and RX. This helps developers inspect readings and troubleshoot the smartwatch firmware.
Internal protocols: AHB or AXI-Lite can serve as the main interconnect, with APB for simple peripheral registers if the architecture includes an APB bridge. AXI-Lite is a simpler AXI variant suited to single-transfer register accesses. 


# Why multiple interfaces?
Each interface has a different job: I²C reads sensor data, SPI sends display data, GPIO detects simple digital events, and UART provides a debugging path. The exact combination depends on the selected components.
