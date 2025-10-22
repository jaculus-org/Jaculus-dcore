# Troubleshooting

Some problems that may occur when using Jaculus and how to fix them.


## Command stuck on "Connected" and not doing anything

This means that the device does not respond to the communication. This can be caused by several things:

- The firmware is halted or otherwise not responding
- The device is stuck in a boot loop
- The device does not have Jaculus firmware installed
- Jaculus-tools version is incompatible with the device firmware

To fix this, try the following:

- Check that you are connecting to the correct port
- Reset the device by pressing the reset (EN) button
- Unplug and reconnect the device
- Flash the Jaculus firmware again ([Getting started](getting-started.md))
- Update Jaculus-tools and device firmware to the latest version


## Command "flash" stuck on one file

This can be caused by several things:

- The device crashed while uploading the file
- The filesystem on the device is corrupted

To fix this, try the following:

- Reset the device by pressing the reset (EN) button
- Unplug and reconnect the device
- Flash the Jaculus firmware again ([Getting started](getting-started.md))


## Cannot flash firmware

If the firmware flashing fails, try the following:

- Try resetting the device to the bootloader mode manually by holding the BOOT button while pressing the reset (EN) button, then releasing the BOOT button after a second
- Make sure you have the correct drivers installed for your device (likely CP210x or CH340)
- Try using a different USB cable or USB port
