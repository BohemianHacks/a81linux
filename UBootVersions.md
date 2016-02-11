# Introduction #

There appear to be a number of versions of U-Boot floating about, some of which work properly, and some of which don't.

# Details #

The versions supplied by Witstech all appear to be based on U-Boot 2008.10, but from an unknown repository.  the standard U-Boot repo doesn't have  Omap3 support for that version.  These only appear to be able to boot specific kernels, although this may be a kernel issue rather than a u-boot issue.  The symptoms of a failed boot are that the boot stops at "Loading Kernel..." on the serial port.

With a certain amount of care, you can use witstech's Android u-boot to fire up linux on the SDCard.  the main thing you need to do is edit U-Boot.bin **before flashing** to have a bootdelay parameter other than 0, which will allow you to interrupt booting using a serial link.

http://code.google.com/p/beagleboard/downloads/detail?name=u-boot_revc_v3.bin&can=2&q is reported to work as well, but possibly requires a kernel configured for beagleboard.

U-Boot 20010.06 builds, and with some configuration will boot linux (at least the same versions 2008.10 will, and possibly others).  However, it doesn't initialise the LCD or backlight, which is "somewhat annoying", as it leaves you with a system you can only interact with over serial.  I'm working on that, in that I'm trying to incorporate the techniques used by the ITBOK utility (this seems to be what witstech have done with their 2008.10 version, going by the debug messages they left in) and the values used by witstech (disassemble, disassemble).