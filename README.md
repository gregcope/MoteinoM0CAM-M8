# MoteinoM0CAM-M8
A [Moteino M0](https://lowpowerlab.com/guide/moteino/moteinom0/) [Breakout board](https://lowpowerlab.com/guide/moteino/m0-sensor-shields/) for a uBlox [CAM-M8Q](https://www.u-blox.com/en/product/cam-m8-series) GNSS module.  This module has an integrated GNSS chip antenna.  The board also containers an MCP 1711 Low DropOut regulator to power the module.  The battery backup (V_BCKP) is constantly powered by the Moteino M0 3.3v.

A green LED is connected to the TIMEPULSE output (1 pulse per second, synchronized at rising edge, pulse length 100 ms) as a visual fix indicator.

The LDO Enable pin (to power the main module down), TIMEPULSE and LNA Enable are connected to Moteino pins.

# Setup
* git clone https://github.com/u-blox/CadSoft-Eagle-Library and copy the ubloxLib.lbr to ~/Documents/eagle/libraries so that you have the CAM-M8Q part.

# BOM
* [CAM-M8Q - UK Link](https://www.tme.eu/gb/details/cam-m8q/gnss-gps-glonass-beidou-modules/u-blox)
* [Microchip Tech MCP1711T-33I/OT](https://lcsc.com/product-detail/Others_Microchip-Tech_MCP1711T-33I-OT_Microchip-Tech-MCP1711T-33I-OT_C79527.html)
* [0603 100nF SMD Capacitors](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Walsin-Tech-Corp-0603B104J250CT_C237171.html)
* [0603 4.7uF SMD Capacitor](https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Walsin-Tech-Corp-0603N4R7C500CT_C314302.html)
* [0603 220 Ohm SMD Resistors](https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount_Uniroyal-Elec-0603WAJ0221T5E_C1226.html)
* [0603 Green SMD LED](https://lcsc.com/product-detail/Light-Emitting-Diodes-LED_0603-green_C205443.html)

Design Notes
* Search the [CAM-M8 Hardware Integration Manual](https://www.u-blox.com/sites/default/files/CAM-M8-FW3_HardwareIntegrationManual_%28UBX-15030063%29.pdf) for the following referances
* 220R Resitors on RXD and TXD as recommended here; 'To avoid interference by improperly shielded lines, it is recommended to use resistors' and section 2.2 'Minimal Design'
* 4.7uF from Section 2.2 'Minimal Design'
* The Regulator needs to supply 71mA max on CAM-8 startup (see 4.3 Indicative power requirements from the data sheet)
* Search the [MCP1711 Datasheet](https://datasheet.lcsc.com/szlcsc/Microchip-Tech-MCP1711T-33I-OT_C79527.pdf) for the following referances
* The MCP1711 was chosen as it has an enable pin and low quiescent curent draw
* The 0.1uF input and output capacitor see 'For most applications, 0.1 µF of capacitance will ensure stable operation of the LDO circuit. If the output capacitor is used, the input capacitor should have a capacitance value equa' is from section 3.1 Unregulated Input Voltage(Vin)

# Other Resources
* Easyeda board: https://easyeda.com/granbobbi22/MAX-M8Q-Minimal-Breakout
* Watterott board: https://github.com/watterott/CAM-M8Q-Breakout/blob/master/hardware/CAM-M8Q-Breakout_v11.pdf
* CAM-M8u-blox M8 Data Sheet : https://www.u-blox.com/sites/default/files/CAM-M8-FW3_DataSheet_%28UBX-15031574%29.pdf
* CAM-M8 Hardware Integration Manual : https://www.u-blox.com/sites/default/files/CAM-M8-FW3_HardwareIntegrationManual_%28UBX-15030063%29.pdf
* MCP1711 Datasheet: https://datasheet.lcsc.com/szlcsc/Microchip-Tech-MCP1711T-33I-OT_C79527.pdf

# Schematic / Board
![Schematic](/MoteinoM0CAM-M8-sch.png)
![Board](/MoteinoM0CAM-M8-brd.png)
