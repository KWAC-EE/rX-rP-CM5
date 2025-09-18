## rX-rP-CM5 ##
**Radxa-rPi CM5 Compatibility Layer**
<img width="1277" height="817" alt="image" src="https://github.com/user-attachments/assets/e7e88d8d-1e01-4521-aa2e-1cee008cc56a" />

The Radxa and RaspberryPi CM5s have much in common, but the pinout between them differs. Functionally, the Radxa's RK3588 outperforms Broadcom's BCM2712 in most benchmarks (at least those i'm interested in):
[Benchmarks seen here](https://gadgetversus.com/processor/rockchip-rk3588s-vs-broadcom-bcm2712/)

Native GPU video encode and decode makes the Radxa far more ideal to use as the core of a media server, and local AI acceleration should allow a more energy efficient means of driving my smarthome devices without needing to ping a distal server.

Physically, the Radxa CM5 is more compatible with rPi CM4 carriers than it is with those built for the rPiCM5.
The CM4 wasn't received as enthusatically by developers as the CM5, so more custom carriers are being built to take advantage of the added USB3 functionality.
For that reason, i designed an adapter to transpose the USB3 lanes from the auxilary mezzanine connector on the Radxa to the corresponding pinout on the RaspberryPi variant.

As of 09/18/2025, I haven't been able to perform a flash on a functional Radxa CM5 to test my present design. The single unit i had bought was damaged in a way I am unable to repair, so I havent been able to test this design en vivo. Updates will be included as testing becomes possible.

# Project design files
PCBAs are designed in Altium 22 & 25. This is a paid software platform for professionals, and viewer licenses can be requested from the developers.

Design references can also be found as PDFs for those who wish to rebuild segments of the design themselves.

# PCBA exports/ Manufacturer files
Designs have been exported as Gerbers with Pick&Place & BOM files such that they may be fully assembled by prototypers such as JLC-PCB, PCB-Way and the like.
Simply upload the zipped project export folder for the PCB, then the internal XLXS/CSV component-level assembly.

# License
Copyright Kurt Widhalm/@KWAC-EE 2025
This source describes Open Hardware and is licensed under the CERN-OHL-P v2

You may redistribute and modify this documentation and make products using it under the terms of the CERN-OHL-P v2 (https:/cern.ch/cern-ohl). This documentation is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE. Please see the CERN-OHL-P v2 for applicable conditions
