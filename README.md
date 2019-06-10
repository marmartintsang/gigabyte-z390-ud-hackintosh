# Gigabyte Z390-UD Hackintosh Installation

## Part List
| Component     | Model         | 
| ------------- |:-------------:| 
| CPU           | Intel® Core™ i7-8700 Processor | 
| Motherboard      | Gigabyte Z390 UD      |   
| Video Card | ZOTAC GeForce® GTX 1080 Ti AMP Edition      | 
| Ram | ADATA Premier, 8GB, DDR4, 2666MHz x 2 |

## PreRequisites
- [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/)
- [Clover's Install Package](http://mackie100projects.altervista.org/download-clover-configurator/)

## Installation Walkthrough
1. Get `MacOS High Sierra (< 10.13.6)`. ([Huihut](https://blog.huihut.com/2018/10/13/GIGABYTE_Z370_HD3P_i7-8700K_GTX1080_Install_Hackintosh_HighSierra10.13.6/)) has mentioned that there is a bug when using `10.13.6` image.)
2. Building the USB Installer followed by [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/building-the-usb-installer)
3. Install `Clover EFI bootloader` to USB Installer followed by [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup)
4. Copy `VirtualSMC.kext` and `IntelMausiEthernet.kext` to `/Volumes/EFI/EFI/CLOVER/kexts/Other`


## References
- [Vanilla](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/)
- [z390 aorus master i99900k gtx1070ti high sierra](https://www.reddit.com/r/hackintosh/comments/a4obvs/z390_aorus_master_i99900k_gtx1070ti_high_sierra/)
- [Hackintosh Mojave Installation Guide for Gigabyte Z390 Aorus Master](https://github.com/cmer/gigabyte-z390-aorus-master-hackintosh)
- [技嘉Z370 HD3P + i7-8700K + GTX1080 装黑苹果 High Sierra 10.13.6](https://blog.huihut.com/2018/10/13/GIGABYTE_Z370_HD3P_i7-8700K_GTX1080_Install_Hackintosh_HighSierra10.13.6/)
- [Building a GTX 1080 Ti-powered Hackintosh: Installing macOS Sierra step-by-step [Video]](https://9to5mac.com/2017/04/28/building-a-gtx-1080-ti-powered-hackintosh-installing-macos-sierra-step-by-step-video/)
