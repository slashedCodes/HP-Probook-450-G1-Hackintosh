![image](https://github.com/slashedCodes/HP-Probook-450-G1-Hackintosh/assets/76942911/687a2279-abdd-41b8-8a3b-472c2c0861aa)

# HP Probook 450 G1 Hackintosh

This repo contains the EFI Folder for [OpenCore 1.0.0](https://github.com/acidanthera/OpenCorePkg/releases/tag/1.0.0) for the [HP Probook 450 G1](https://support.hp.com/vn-en/document/c03963187).

I tested this with big sur, feel free to experiment on your own. <br>
If you've found that this EFI folder works with Catalina or Monterey for example, please fork this repository and pull request your corresponding fixes into the EFI folder and mention the version of MacOS that you've found this to work on.

# IMPORTANT!!!!!!!!!!!!
After MacOS is installed, still follow the [Post-Install Guide](https://dortania.github.io/OpenCore-Post-Install/). <br>
Specifically follow the [Booting without USB Guide](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html), otherwise you won't be able to boot without the USB.

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

| PURPOSE          | KEXT                                                                                                                                          | VERSION                                                                      |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Required         | [VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases)                                                                              | [1.3.2](https://github.com/acidanthera/VirtualSMC/releases/tag/1.3.2)        |
| Required         | [Lilu](https://github.com/acidanthera/Lilu/releases)                                                                                          | [1.6.7](https://github.com/acidanthera/Lilu/releases/tag/1.6.7)              |
| Graphics         | [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)                                                                        | [1.6.6](https://github.com/acidanthera/WhateverGreen/releases/tag/1.6.6)     |
| Audio            | [AppleALC](https://github.com/acidanthera/AppleALC/releases)                                                                                  | [1.9.0](https://github.com/acidanthera/AppleALC/releases/tag/1.9.0)          |
| Ethernet         | [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases)                                                                   | [2.4.2](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases/tag/2.4.2) |
| Input            | [VoodooPS2](https://github.com/acidanthera/VoodooPS2/releases)                                                                                | [2.3.5](https://github.com/acidanthera/VoodooPS2/releases/tag/2.3.5)         |
| Battery Readouts | [ECEnabler](https://github.com/1Revenger1/ECEnabler/releases)                                                                                 | [1.0.4](https://github.com/1Revenger1/ECEnabler/releases/tag/1.0.4)          |
| Brightness Keys  | [BrightnessKeys](https://github.com/acidanthera/BrightnessKeys/releases)                                                                      | [1.0.3](https://github.com/acidanthera/BrightnessKeys/releases/tag/1.0.3)    |

# Side notes
 - OpenCore has the RELEASE binaries, and [OpenCanopy is installed](https://dortania.github.io/OpenCore-Post-Install/cosmetic/gui.html) (GUI for OS picker). When booting up, hit space on the GUI picker and wait a few minutes to select the USB recovery.
 - [SSDT's](https://dortania.github.io/Getting-Started-With-ACPI/) were compiled using [SSDTTime](https://github.com/corpnewt/SSDTTime) on Windows 10.
 - Every time MacOS reboots during recovery/setup, boot into the usb and pick the first option (which is the macos partition).

# Issues
 - CMOS Reset bullshit. I aint fixing that
 - Wifi doesn't work - no driver.
