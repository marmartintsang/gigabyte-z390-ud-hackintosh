# [SUCCESS] Gigabyte Z390-UD Vanilla Hackintosh Installation

## Part List
| Component     | Model         | 
| ------------- |:-------------:| 
| CPU           | Intel® Core™ i7-8700 Processor | 
| Motherboard      | Gigabyte Z390 UD      |   
| Video Card | ZOTAC GeForce® GTX 1080 Ti AMP Edition      | 
| Ram | ADATA Premier, 8GB, DDR4, 2666MHz x 2 |
| Storage | Western Digital 240GB Green M.2 2280 Internal Solid State Drive Model WDS240G1G0B  |
| Wifi | BCM94360 PCI-E |
| Bluetooth | BCM94360 USB |

## Targeted OS
#### macOS High Sierra
It is a pity that Nvidia display card is currently not supported in macOS Mojave and above ;( The second thing I would like to mention is that GeForce® RTX 20 series is not supported by Nvidia also. (No drivers for RTX 20 series for macOS). Thus, my build will use GTX 1080 and 10.13 for the best performance.

## PreRequisites
- [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/)
- [Clover's Install Package](http://mackie100projects.altervista.org/download-clover-configurator/)

## Installation Walkthrough
1. Get `macOS High Sierra (10.13.6)`
2. Building the USB Installer followed by [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/building-the-usb-installer)
3. Install `Clover EFI bootloader` to USB Installer followed by [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup)
4. Copy `FakeSMC.kext (All kexts)`, `IntelMausiEthernet.kext`, `USBInjectAll.kext`, `AppleALC.kext`, `Lilu.kext`, `WhateverGreen.kext` and `AirportBrcmFixup.kext` to `/Volumes/EFI/EFI/CLOVER/kexts/Other`
5. Edit Config.Plist by `Clover Configurator`, the settings can be found here [Coffee Lake Config](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-per-hardware/coffee-lake)
6. Configure Bios
    - Load Optimized Default Settings
    - Peripherals → USB Configuration → XHCI Hand-off : Enabled
    - Peripherals → Super IO Configuration → Serial Port: Disabled
    - Chipset → DVMT Pre-Allocated: 96M
    - Chipset → DVMT Total Gfx Mem: 256M
7. Install macOS
8. Create EFI partition for Hackintosh
    - locate SSD & USB's disk no. by `diskutil list`
    - Create EFI partition for Hackintosh `sudo mkdir /Volumes/efidisk`
    - `sudo mount -t msdos /dev/disk{number} /Volumes/efidisk`
    - Mount USB's EFI partition `sudo mkdir /Volumes/efiusb`
    - `sudo mount -t msdos /dev/disk{number} /Volumes/efiusb`
    - Copy clover settings from USB `cp -R /Volumes/efiusb/* /Volumes/efidisk`
9. Install nvidia web driver

## References
- [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/)
- [z390 aorus master i99900k gtx1070ti high sierra](https://www.reddit.com/r/hackintosh/comments/a4obvs/z390_aorus_master_i99900k_gtx1070ti_high_sierra/)
- [Hackintosh Mojave Installation Guide for Gigabyte Z390 Aorus Master](https://github.com/cmer/gigabyte-z390-aorus-master-hackintosh)
- [Building a GTX 1080 Ti-powered Hackintosh: Installing macOS Sierra step-by-step [Video]](https://9to5mac.com/2017/04/28/building-a-gtx-1080-ti-powered-hackintosh-installing-macos-sierra-step-by-step-video/)
