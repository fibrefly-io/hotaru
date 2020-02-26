fibrefly.io "hotaru" debug board
================================

This is a utility board for the fibrefly.io project.  It provides 2 JTAG/SWD
ports on an FT4232H, one of which is on an USB-C plug specific to the project.
(Debug accessory mode is used on the target board to enable SWD.)

*This board is not production proven yet.  The first prototype batch has just
been ordered.*

The USB-C JTAG/SWD interface is probably not useful for other projects.
However, the following features are generally useful:

- properly buffered JTAG port, should work at 1.2V - 3.3V
  - 20-pin 2.54mm ARM (old) standard pinout
  - 10-pin 1.27mm "Cortex debug" pinout
- two properly buffered serial ports with CTS/RTS flow control, should work
  at 0.9V-3.3V
- USB-C port controller with STM32 MCU to control it via USB to I2C to Type-C
  (e.g. to debug full-featured USB-C implementations)

There is no firmware yet for the STM32 MCU.

Designed with Horizon EDA [https://github.com/horizon-eda/horizon]
