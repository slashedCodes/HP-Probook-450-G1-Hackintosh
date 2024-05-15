# HP Probook 450 G1 Hackintosh

This repo contains the EFI Folder for OpenCore 1.0.0 for the [HP Probook 450 G1](https://support.hp.com/vn-en/document/c03963187).

I tested this with big sur, feel free to experiment on your own. <br>
If you've found that this EFI folder works with Catalina or Monterey for example, please fork this repository and pull request your corresponding fixes into the EFI folder and mention the version of MacOS that you've found this to work on.

# The Hardware

| PART               | MODEL                              | COMMENT                      |
|--------------------|------------------------------------|------------------------------|
| CPU                | Intel i5 4200M                     | Haswell                      |
| DGPU               | Radeon HD 8750M                    | Disable this in BIOS         |
| IGPU               | Intel Graphics 4600                | Supported up to MacOS 12.6.x |
| CHIPSET            | Mobile Intel HM87 Express          |                              |
| KEYBOARD           | PS/2                               |                              |
| TOUCHPAD           | PS/2 Synaptics                     |                              |
| AUDIO              | IDT92HD91                          | AppleAHC ID 13               |
| NETWORK CONTROLLER | Realtek PCIE GBE Family Controller |                              |
| WI-FI CARD         | Qualcomm Atheros QCA9565           |                              |

# Kexts Used

| PURPOSE          | KEXT                                                                                                                                          |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Required         | [VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases)                                                                              |
| Required         | [Lilu](https://github.com/acidanthera/Lilu/releases)                                                                                          |
| Graphics         | [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)                                                                        |
| Audio            | [AppleALC](https://github.com/acidanthera/AppleALC/releases)                                                                                  |
| Ethernet         | [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases)                                                                   |
| Wifi             | [High Sierra's IO80211Family](https://github.com/khronokernel/IO80211-Patches/blob/main/10.13.6-High-Sierra-Kexts/IO80211HighSierra.kext.zip) |
| Input            | [VoodooPS2](https://github.com/acidanthera/VoodooPS2/releases)                                                                                |
| Battery Readouts | [ECEnabler](https://github.com/1Revenger1/ECEnabler/releases)                                                                                 |
| Brightness Keys  | [BrightnessKeys](https://github.com/acidanthera/BrightnessKeys/releases)                                                                      |

# Issues
 - CMOS Reset bullshit. I aint fixing that