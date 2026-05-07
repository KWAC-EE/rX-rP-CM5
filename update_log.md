*10/16/2025*
Samples of X2 arrived, as did a fresh CM5 from Radxa.
As hoped, the USB-C port allows the device to be programmed independently.
There are a few bugs in the transposition, at least in the carrier I design to pair with this.
The primary USB3 lane from the auxilary port is transposed to the USB3-1 channel pads of the Raspberry pi CM5 carrier, and downstream devices fully enumerate and function.
The USB-C channel, however, doesn't appear to be behaving correctly, at least not on my current OS & hardware.
Similarly, the USB2 lane that is transposed to the OTG pads doesn't appear to initialize the downstream hub.
I'll continue testing by using a real CM5 IO board from raspberry pi soon.

**<11:30pm>**
ok, I know what I did now. flipped the polarity between the otg & USB-C d+/- nets. dislexia strikes again...

you know what they say: third rev's the charm. dammit....

*11/17/2025*
X3 samples are in. USB2 and USB3-1 channels work as intended, and the onboard USB-C(2.0) port allows flashing of the module; USB3-0, which is derived from the Type-C on header J3, will not enumerate connected devices through OTG/Host mode. May be from I2C port controller, still debugging

*2/20/2026*
X4 design is done. giving up on using the OTG port to drive a separate USB3 channel, and instead decided to split the known working USB3 channel with a hub. Will this reduce overall bandwidth? Yes, but for my application, i doubt it will be noticable.
I'll order samples when i place another order for other parts.

*3/27/2026*
Shouldn't have given up on X3 so quickly... Did a bit more experimenting. Lo and Behold, i needed to depop the FUSB chip completely, enter the Radxa OS configuration utility and manually set the OTG port to use only Host mode, and Tah-dah, it works exactly as intended. which is good, because there seems to be some interference caused by the hub on the X4 version that prevents the flashing utility from conntecting to the Emmc. So if you were planning on using any version of this design, i recommend starting from X3, removing the FUSB U1 component, and configuring it within the device tree.

*5/7/2026*
I just widdled it down for rev X5 to make use of what I learned from working on X3. Mechanically, the addition of the USB-C port was a hinderance; it got in the way of a few hardware enclosures, so i wasn't cleanly able to test compatibility with some custom carriers.
Electrically, i think the MUX config will function better so I can flash the EEprom of the SoM without the extra connector. Furthermore, i needed to add pull-ups for the VBus-enable pin so the current regulator on the Pi Cm5 IO board would turn on without bodging at start-up.
IDk when i'll be able to order samples. I really want to deploy one of these units so i can set up my Arm64 Nas, but the expense is hard to justify without additional parts to order with it.
