# Universal WLED board with ethernet switch

This projects aims to deliver a hardware platform to drive smart LEDs like WS2812, SK6812 and similar.
It can operate from the LED strips supply voltage (5-24V) and provides a webinterface over WiFi or Ethernet.
The integrated ethernet switch enables an ethernet daisy chain.
Each LED output is individually fused to allow for thiner wires and high current powersupplies.
Some smart LEDs have trouble reading 3.3V data signals with a high supply voltage. This board contains a 5V output driver to avoide data corruption.

![](images/pcb_v2.jpg)
![3D Rendering of the board](images/3drender.png)

## Features
* WLED compatible
* Input Voltage 5-24V
* Integrated Ethernet switch for daisy chaining
* 6 LED outputs with 5V signal level
* 5A per output, 16A total
* Every output fused individually
* Output using 2.54mm pins or AKZ500 screw terminals
* 2 fan connectors with PWM
* Connector for DS18B12 temperature sensors
* Connector for I2S microphones (shared with LED output 4/5)
* LEDs can be disabled with jumpers
* Reverse protection diode, will short-circuit the supply if reversed
* Board size 110 x 80mm

## Building it
PCB manufacturing data (gerber), schematic and (mostly) mouser BOM are available in directory "hardware/releases/". PCB was manufactured by JLCPCB including stencil, but hand soldering is an option (L1 needs hot air soldering).
Solder thick wires (1.5 - 2.5mm2) on the exposed traces on the bottom to allow high output currents.

![](images/ksz8863.jpg)

## Cost
BOM costs are around 45€ + Board + Stencil

## License
This hardware is licensed under CERN open hardware license [CERN-OHL-W](license.txt)

## Software
Compatible with my fork of WLED, available [here](https://github.com/Bauteiltoeter/WLED2/tree/cyberlamp).
