# **Hackintosh EFI HP Pavilion 14-V205TX**

Hackintosh **macOS Big Sur 11.7.6** | **HP Pavilion 14-V205TX**

---

**Download EFI**

- via Terminal : \$ `git clone https://github.com/fahrulariza/HP-Pavilion-14-V205TX.git` or [Click Here](https://github.com/fahrulariza/HP-Pavilion-14-V205TX/archive/refs/heads/master.zip)

---

**Specification  :**

- **Processor :** [Intel Core i5-5200U @ 2.20GHz 3 MB cache, 2 cores](https://www.intel.co.id/content/www/id/id/products/sku/85212/intel-core-i55200u-processor-3m-cache-up-to-2-70-ghz/specifications.html)
- **Motherboard  :** Hewlett-Packard 2295 (Socket BGA1168)
- **iGPU :** [Intel® HD Graphics 5500](https://ark.intel.com/content/www/id/id/ark/products/graphics/86210/intel-hd-graphics-5500.html)
- **dGPU :** [Nvidia GeForce 840M (Optimus)](https://www.nvidia.com/en-us/geforce/gaming-laptops/geforce-840m/)
- **Memory :** 8GB 2x4GB DDR3L PC3-12800 / 1600Mhz
- **Storage :** 1x [ADATA SU650 SSD 240GB](https://www.adata.com/us/specification/503) (Windows 10) + 1x  Candy 2,5" [SATA SDD VENOMRX 1TB](https://venomrxs.com/ssd/super-ssd-sata/) (macOS)
- **Ethernet :** 1x [Qualcomm Atheros AR9485WB-EG Network Adapter 72 MB Ethernet](https://www.ath-drivers.eu/download-driver-for-Atheros-chipset-with-id-61-and-Windows10-64bit.html)
- **Wi-Fi :** [RealTek RTL8101/2/3 Family Fast Ethernet NIC](https://www.realtek.com/en/component/zoo/category/network-interface-controllers-10-100-1000m-gigabit-ethernet-pci-express-software)
- **Bluetooth :** [Atheros AR3012 version 4.0](https://www.ath-drivers.eu/download-driver-for-Atheros-chipset-with-id-77-and-Windows10-64bit.html)
- **Camera :** [Chicony Electronics HP Truevision HD Webcam](https://id.webcamtests.com/reviews/17777)
- **USB :** [Intel Broadwell Chipset](https://ark.intel.com/content/www/id/id/ark/products/codename/38530/products-formerly-broadwell.html)
- **Touchpad :** [ALPS Pointing-device](https://osxlatitude.com/forums/topic/8285-refined-alps-touchpad-driver/)
- **External Ports :** 1x SDCard Reader + 2x USB 3.0 + 1 USB 2.0 + 1x HDMI + 1x RJ45
- **Audio Codec :** [Realtek Audio ALC290](https://witcomputers.com/product/alc-290-realtek-audio-chip-ics/) (3,4,10,15,25)
- **Display Size and Model :** 14” LG Philips diagonal HD WLED-backlit
- **Monitor Resolution :** HD 1366 x 768
- **Boot Mode :** UEFI GPT
- **BIOS Manufacturer :** Insyde Software version F.57
- **SMbios :** MacBookAir7,2
- **OS Version :** [macOS Big Sur 11.7](https://www.olarila.com/topic/6278-olarila-vanilla-images-macos-installer/)
- **Bootloader :** [OpenCore 0.9.1](https://github.com/acidanthera/OpenCorePkg/releases)

---

**What's Working **

- QE/CI of Intel HD Graphics 5500 (1536MB) | **ig-platform-id** : 06002616 + SMBIOS MBP12,1 ([Lilu](https://github.com/acidanthera/Lilu/releases), [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases))
- CPU Power Management (SSDT-PLUG)
- Restart, Sleep and Shutdown
- [Internal Speaker, Headphone and Internal Microphone](https://www.tonymacx86.com/threads/solved-intel-hd-graphics-520-realtek-alc290-codec-alc3241-rtl8101e-hp-laptop.210923/page-6) | with layout-id 3,4,10,15,25 ([AppleALC](https://github.com/acidanthera/applealc/releases), [Lilu](https://github.com/acidanthera/Lilu/releases), SSDT-IRQFix)
- Touchpad with Gestures
- Brightness | (SSDT-PNLF)
- FN + Brightness Button Up/Down | (SSDT-PNLF)
- Ethernet | ([RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases))
- Wi-Fi | (AirPortAtheros40, [HS80211Family](https://www.insanelymac.com/forum/files/file/1008-io80211family-modif/))
- Bluetooth | (Turn on in Windows setting, then restart and boot to macOS)
- HDMI Out (Video)
- HDMI Audio (Video)
- Battery Indicator | ([VirtualSMC](https://github.com/acidanthera/virtualsmc/releases), SMCBatteryManager)
- All USB Port (USB 3.0, USB 2.0, Jack Audio)
- iMessage + facetime | (Use Real Serial Number of MacBook Pro (Sync with SMBIOS))
- Webcam
- SD Card Reader
- Etc..

---

**Not Working :**

- dGPU : Nvidia GeForce 840M (disable from SSDT)
- AirDrop ??? not tested

---

**BIOS Configuration**

|                  Bios Config                  |  Setting   |
| :-------------------------------------------: | :--------: |
|            Security -> Secure Boot            |  Disabled  |
|             Intel Virtualization              |  Enabled   |
|                     VT-d                      |  Enabled   |
| Graphics Configuration -> DVMT Pre-Allocation |    64M     |
|    USB Configuration -> XHCI Pre-Boot Mode    | Smart Auto |
|                   SATA Mode                   |    AHCI    |
|              Boot -> Launch CSM               |  Disabled  |

---

**Tutorial**

[OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
if you used this my EFI please Generate New SMbios

---

**Special Thanks and Credits to :**

[Apple](https://www.apple.com) | [OpenCore](https://github.com/acidanthera/OpenCorePkg) | [corpnewt](https://github.com/corpnewt/gibMacOS) | [doesprintfwork](https://github.com/doesprintfwork/MakeInstallmacOS) | [Acidanthera](https://github.com/acidanthera) | [RehabMan](https://github.com/RehabMan/Laptop-DSDT-Patch) | [Mieze](https://github.com/Mieze/RTL8111_driver_for_OS_X) | [InsanelyMac](https://www.insanelymac.com/forum) | [Andres ZeroCross](https://github.com/andreszerocross) | Other Developers.

---
