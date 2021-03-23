# Xps-7590-BigSur
Hackintosh EFI for XPS 7590/Precision 5540. OC 6.5. Follow this guide (https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html) to set up your own EFI. I couldn't upload the EFI, OC, or one of the BOOT folders because I don't know how to use Github.

****MAKE SURE YOU PUT IN YOUR OWN SERIAL, MLB, ROM, ect****. You can follow this guide: https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake-plus.html#platforminfo

BIOS settings:

This: https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake-plus.html#intel-bios-settings
Plus-
Thunderbolt: Displayport and USB C only
Native Thunderbolt control-not bios assist


Working:

Everything minus fingerprint reader (if you're willing to make changes). Using this repo exactly as it is, only Thunderbolt and SD card reader don't work. To fix thunderbolt, enable ssdt-tb3 then enable Thunderbolt in the BIOS. Keep the controller at Native, not Bios assist. Enabling Thunderbolt may take ~2 additional watts. I haven't done the testing to figure out.

For SD card reader, remap USB ports with this guide: https://dortania.github.io/OpenCore-Post-Install/usb/intel-mapping/intel.html to include the SD card reader **or** disable USBports.kext (may cause instability). Then enable the sinetek-rtsx kext in the config.plist. Reboot, then make sure the SD card is enabled in the BIOS. After that, you should be good to go.


Initial credits (I'll improve if people actually start seeing this repo):

@xxxzc
https://github.com/xxxzc/xps15-9570-macos

@jaromeyor
