# MoteinoM0CAM-M8
A [Moteino M0](https://lowpowerlab.com/guide/moteino/moteinom0/) [Breakout board](https://lowpowerlab.com/guide/moteino/m0-sensor-shields/) for a uBlox [CAM-M8Q](https://www.u-blox.com/en/product/cam-m8-series) GNSS module.  This module has an integrated GNSS chip antenna.  The board also containers an MCP 1711 Low DropOut regulator to power the module.  The battery backup (V_BCKP) is constantly powered by the Moteino M0 3.3v.

A green LED is connected to the TIMEPULSE output (1 pulse per second, synchronized at rising edge, pulse length 100 ms) as a visual fix indicator.

The LDO Enable pin (to power the main module down), TIMEPULSE and LNA Enable are connected to Moteino pins.

# Setup
* git clone https://github.com/u-blox/CadSoft-Eagle-Library and copy the ubloxLib.lbr to ~/Documents/eagle/libraries so that you have the CAM-M8Q part.

# BOM
* [CAM-M8Q - UK Link](https://www.tme.eu/gb/details/cam-m8q/gnss-gps-glonass-beidou-modules/u-blox)
* MCP 1711 LDO
* 0603 100nF SMD Capacitors
* 0603 4.7uF SMD Capacitor
* 0603 220 Ohm SMD Resistors
* 0603 Green SMD LED

# Other Resources
* Easyeda board: https://easyeda.com/granbobbi22/MAX-M8Q-Minimal-Breakout
* Watterott board: https://github.com/watterott/CAM-M8Q-Breakout/blob/master/hardware/CAM-M8Q-Breakout_v11.pdf
* CAM-M8 Hardware Integration Manual : https://www.u-blox.com/sites/default/files/CAM-M8-FW3_HardwareIntegrationManual_%28UBX-15030063%29.pdf

# Schematic / Board
![Schematic](/MoteinoM0CAM-M8-sch.png)
![Board](/MoteinoM0CAM-M8-brd.png)
