# VoodooSMBusOCGuide
A guide for OC users to configure VoodooSMBus.

Tested with Opencore 1.0.7 (04/15/2026).

## Disclaimer

I didn't make the VoodooSMBus kext, I just spent some days to set it up the VoodooSMBus in my Thinkpad E14 Gen 1 (i5-10210u). So this is just a guide to configure like I did.

## How to

1. Install the **[VoodooPS2 kext](https://github.com/acidanthera/VoodooPS2)** from Acidanthera in your EFI/OC/Kexts
2. Add the four kernel patches from original VoodooSMBus ([link to patches converted to OC]())
3. Install the **[VoodooSMBus](https://github.com/VoodooSMBus/VoodooSMBus)** in your EFI/OC/Kexts
4. Remember to OC Snapshot the config.plist with **[ProperTree](https://github.com/corpnewt/propertree)**
5. Restart and see if it's working

## Validating

Open **[IORegisterExplorer](https://github.com/khronokernel/IORegistryClone/blob/master/ioreg-302.zip)** and see if the SBUS/SMBU has mouse/trackpoint things inside like photo below:

If not appears you need to open the info.plist inside VoodooSMBus and add the PCI id of your SMBus Device. I did use the Hackintool to find the device id and vendor id:

Combine device id with vendor id respectively with `0x` prefix, like this:

Reboots and see if it appears in IOReg.

## If any of this not working

Back to **[VoodooSMBus](https://github.com/VoodooSMBus/VoodooSMBus)** repository and check for the guide and search in issues for some solution. I'm not an expert (unfortunately).
