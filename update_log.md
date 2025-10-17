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