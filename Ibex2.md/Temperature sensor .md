# Temperature monitoring SoC

Purpose: Measure room temperature and humidity and send the readings to the CPU.
Internal architecture

         Ibex RISC-V CPU
                | 
    APB or simple internal bus
                |
         I²C Controller
                |
          BME280 Sensor


This is an illustrative architecture, not a mandatory Ibex configuration.

# How the interfaces work

```External interface ```—
# I²C

— The CPU asks the I²C controller to read a sensor register.

— The controller sends a START condition, the sensor address, and a read/write bit over SDA, with SCL providing the clock.

— The sensor acknowledges the address and returns the requested data.

—The controller reports the received data to the CPU.

—The BME280 supports both I²C and SPI. I²C is a convenient choice here because it uses two signal wires and allows compatible devices to share the bus using addresses. 

—Internal protocol — APB or a simple bus
The CPU uses the internal bus to access the controller's registers—for example, to set the sensor address, start a transfer, and read the result. APB is suitable for this type of low-bandwidth register access. 

# Why not AXI?
A small temperature-monitoring system may not need AXI's more complex, high-performance data-transfer features. A simple bus or APB may be sufficient.
