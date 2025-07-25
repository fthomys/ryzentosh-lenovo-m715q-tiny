## OpenCore EFI Config for AMD Ryzen Hackintosh 


[![macOS version](https://img.shields.io/badge/macOS-15.5-informational.svg)](https://www.apple.com/macos)
[![OpenCore version](https://img.shields.io/badge/OpenCore-0.6.3-informational.svg)](https://github.com/acidanthera/OpenCorePkg)


## Specification


| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 5 3200GE @ 3.2GHz |
| Motherboard | Lenovo M715q Tiny |
| RAM | 8GB SK Hynix |
| GPU | AMD Radeon RX Vega 11 |
| WiFi & Bluetooth | Currently None |
| Disk (NVMe) | Crucial 512GB |

**macOS version**: 15.5 Sonoma

**OpenCore version**: 0.6.3  

## What is working:

- Everything besides what is mentioned below

## What is not working:

- Partially-working virtualization (only VirtualBox)
- Wifi and Bluetooth (no hardware installed)
- Sleep
- Google Chrome (somehow it freezes the OS)


## How to use
  1. Make your installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
  2. Clone the repository and paste "BOOT" and "OC" directories into your's install drive "EFI" folder
  3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **MacMini**.
  4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
  5. Boot!  


**IMPORTANT NOTES:**

- If you want iMessage and FaceTime to work, fill in YOUR unique info in PlatformInfo.


**Guides/Support**

 - [Apple](https://apple.com) for macOS
 - [AMD-OSX Developers](https://github.com/AMD-OSX) for kernel patches for AMD CPUs
 - [Acidanthera](https://github.com/acidanthera) for OpenCore and most of used kexts
 - [Mieze](https://github.com/Mieze) for RealtekRTL8111 kext
 - [Dortania](https://github.com/dortania) for OpenCore configuration guides
 - [AMD-OSX Community](https://amd-osx.com) for support while making my Hackintosh


Have Fun!
