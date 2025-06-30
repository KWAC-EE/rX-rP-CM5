# rX-rP-CM5
Radxa-rPi CM5 Compatibility Layer

The Radxa and RaspberryPi CM5s have much in common, but the pinout between them differs.

Physically, the Radxa CM5 is more compatible with CM4 carriers than it is for those built for the rPiCM5. For that reason, i designed an adapter to transpose the USB3 lanes from the auxilary mezzanine connector on the Radxa to the corresponding pinout on the RaspberryPi variant.

I haven't had much luck getting the RadxaCm5 in my posession working, and now i have phsyically damaged it, so I can't confirm its function.

MUX chipsets are meant to swap the USB2 lanes between acting as a Host for USB peripherals, and acting as Mass Storage for eMMC flashing.
