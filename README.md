# HYKU_Driver
Optional driver for HYKU Tablet that allows multi-monitor support

# What does it do?
This driver forces the HYKU Tablet to map to the entire virtual desktop instead of just the primary monitor to allow multi-monitor support.

# Do you need it?
If you:
- Have a multi-monitor setup
- Want to use the HYKU tablet for things other than osu!
- Find that the cursor is confined to your primary monitor when using the HYKU Tablet

This will allow you to use the tablet across your other monitors.

# Installation

1. Download moufiltr.zip from the [Releases](https://github.com/sssata/HYKU_Driver/releases) page.
2. Extract the zip to a new folder.
3.  [Disable Driver Signature Verification](https://www.howtogeek.com/167723/how-to-disable-driver-signature-verification-on-64-bit-windows-8.1-so-that-you-can-install-unsigned-drivers/)
4. Go to Control Panel\Hardware and Sound\Devices and Printers
5. Right click on HYKU Tablet and click Properties
6. Go to the Hardware tab and select HID Compliant Mouse
7. Click Properties and click Change Settings
8. Click the Drivers tab and click Update Driver
9. Click Browse my Computer for Drivers -> Let Me Pick From a List... -> Have Disk -> Browse to the folder that you extracted moufiltr.zip to -> Ok -> ... etc until driver is installed.
10. Done



# How does it work?

This driver is an upper filter driver for mouclass.sys. All MOUSE_INPUT_DATA packets with the MOUSE_MOVE_ABSOLUTE flag get their MOUSE_VIRTUAL_DESKTOP flag set.


# Original code
This is based on the moufiltr example from Windows Driver Samples.
https://github.com/microsoft/Windows-driver-samples/tree/master/input/moufiltr
