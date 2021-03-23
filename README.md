# Xps-7590-BigSur
Hackintosh EFI for XPS 7590/Precision 5540

**MAKE SURE YOU PUT IN YOUR OWN SERIAL, MLB, ROM, ect**__. You can follow this guide: https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake-plus.html#platforminfo

BIOS settings:

Thunderbolt: Displayport and USB C only
Native Thunderbolt control-not bios assist


Working:

Everything (if you're willing to make changes). Using this repo exactly as it is, only Thunderbolt and SD card reader don't work. To fix thunderbolt, enable ssdt-tb3 then enable Thunderbolt in the BIOS. Keep the controller at Native, not Bios assist. Enabling Thunderbolt may take ~2 additional watts. I haven't done the testing to figure out.

For SD card reader, remap USB ports with this guide: https://dortania.github.io/OpenCore-Post-Install/usb/intel-mapping/intel.html to include the SD card reader **or** disable USBports.kext (may cause instability). Then enable the sinetek-rtsx kext in the config.plist. Reboot, then make sure the SD card is enabled in the BIOS. After that, you should be good to go.
