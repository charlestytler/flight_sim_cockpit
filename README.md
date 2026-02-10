# Arduino Flight Panels

Repository for Arduino software for flight simulation panels that provide input/output for Buttons/Switches/Encoders/LEDs.

## Hardware

![Physical Cockpit](./images/physical_cockpit.jpg)
(Partially) assembled cockpit.

### CAD Models

![CAD Model Rendering of Physical Cockpit](./images/Physical_cockpit_CAD_Model_render.png)
[Link to Fusion 360 Web Viewer](https://a360.co/4bIpcXp)

### PCBs

Current version of PCBs using:
 - Arduino Micro Pro (Atmel ATmega32U4)
    - Central processor for all I/O
    - Emulates a USB HID Joystick device
    - Communicates over Serial to PC middleware
    - Likely will upgrade to RP2040 Pico boards in next revision
 - PCF8575 I2C Expanders
    - Provides 16 digital I/O pins per board
    - Inputs used for Switches, Outputs used for indication LEDs
 - CD74HC4067 Multiplexers
    - Provides 16 to 1 analog input multiplexing
    - Used for reading analog potentiometers
 - RP2040 Raspberry Pi Pico (external of PCB)
    - Used for reading rotary encoders
    - Uses PIO to provide parallel handling of encoder interrupts
 - Screw Terminal breakouts

![PCB Layout](./images/PCB_FlightSimIOBreakoutBoard.png)
![PCB with Soldered Components](./images/PCB_physical_image.jpg)

### Cockpit Layout

![Cockpit Layout](./images/Cockpit_layout.png)
