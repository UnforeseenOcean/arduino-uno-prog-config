# Arduino Uno (ATMEGA328) fresh chip programming with TL866 programmer guide

Download the HEX file from https://diychris.com/index.php/2020/05/13/burning-the-arduino-bootloader-using-the-tl866-ii-plus/

If you want to use the `Xgecu` utility instead of `minipro`, here's how I did it.

This is basically a translation of Chris' guide to this specific utility.

First select ATMEGA328(P) from the list of chips.

Load the firmware image.

Set the fuse config according to the picture.

(Picture goes here and you're supposed to fix it, dummy)

Click PROG button. You can also click READ to dump the chip if you're duplicating the chip for mass manufacturing.

Click Program button to start. This is the part where you can weed out bad chips; If it tells you the pins near the middle are not being connected after moving the chip around then retrying, that means the chip is dead or bad and should be tossed.

You could attempt to ignore the warning and try burning the bootloader using other programmers (ICSP header), but since the middle few pins are power pins I don't think that's going to do anything good.
