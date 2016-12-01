# Koruza Expander board RPi

New Koruza expander board will connect the Raspberry Pi A+ to the new Koruza router board. The purpose is to have all necessary connectors and PCB form to fit into the Koruza unit case and connect all the boards.

**Features:**
* Koruza router connector
  * GPIO
  * I2C (from SFP)
  * USB (for ethernet emulation)
  * Power +5 V, +6/9/12 V (for stepper motors) 
* Raspberry Pi A+ connector
  * Power for Raspberry Pi A+
  * UART to Koruza move driver
  * USB to Koruza router
  * GPIO for IR receiver and transmitter 
* Koruza move driver connector
  * Power for Koruza move driver (onboard regulator for MCU)
  * UART for communication
  * GPIO pin for reset (firmware upgrade)
* IR link connector
  * GPIO for transmitter
  * GPIO for receiver

### Version 1.0
This version is currently active and used with https://github.com/IRNAS/Universal-Stepper-Driver-Rpi board. The following modifications are required to attach Raspberry Pi A+ or Zero to this shield:
 * Cut 12V trace on shield not to connect 5V pins on Raspberry Pi header
 * Solder an USB header on Raspberry and on expander and connect with a cable

### Version 1.1
Koruza units with WiTi board are ready for further development, testing, and assembly, so the new version of the board for Raspberry Pi A+ need to be made for them. All connectors mentioned above are necessary, but also power regulators for converting 24 V PoE input to 12 V for Koruza driver, Koruza router and everything else.
This board should be in shape of the previous version of Kouza expander board to fit in the current Koruza case with the current router and other electronics.

### Version 2.0
This version will have only connectors mentioned above, and not the power regulator for PoE because that part will be on the separate board, the Koruza power board.
The thing to watch out for is in this version is heat dissipation. Because idea is to put Koruza driver and Koruza expander board above the router board. Koruza router has CPU that heats up, and now the Koruza driver also has the CPU that will heat, so they should not be above each other nor the boards should block the space in front of the MCU chips.

  
