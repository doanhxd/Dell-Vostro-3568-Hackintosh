# Dell Vostro 3568 Hackintosh - OpenCore (Big Sur - 11.1)
**Note: I WILL NOT RESPONSIBLE IF YOU MESS UP YOUR COMPUTER USING THIS GUIDE!**

Intro
---

![About this Mac](https://github.com/doanhmaple/Dell-Vostro-3568-Hackintosh/blob/main/images/About_Mac.png)

This BIOS is actual only for Razer Blade 15 Advanced (2018)

| | Version |
| ---: | :--- |
| ``OpenCore`` | 0.6.4 (RELEASE) |
| ``Catalina`` | 10.15.7 (19H114) |
| - | - |
| ``Big Sur`` | 11.1 (20C69) |

## Disclaimer

This repository has no other purpose but sharing.
I want to share my hackintosh configuration for this particular laptop with the whole world.
This is not a step by step guide, rather a thing that can greatly help you on your way of turning this or similar laptop into a hackintosh.
Though you can just grab and use this if you have same or very similar laptop model, I greatly encourage you not do so, but instead read all the things I will mention below and get some knowledge.

## Hmmm...

* Please create [USBMap](https://github.com/corpnewt/USBMap) or `USBPort.kext` (Use Hackintool to do this) after install for best USB plug experience (uncheck SSDT-USBX-LAPTOP in config.plist or remove it when using USBMap/USBPort.kext)

* Create one-key cpufriend if you often use battery, power-plug always is not recommended for best performance 

Hardware
---

**Dell Vostro 3568 - Kaby Lake**

| | Specifications | macOS 10.15 Catalina & Big Sur compatibility |
| ---: | :--- | :--- |
| ``Chipset`` | Intel Kaby Lake | No issues |
| ``CPU`` | Intel Core i7-7500U Processor, 2 Cores / 4 Threads, 2.7Hz / 3.5GHz, 4MB Cache | No issues |
| ``Memory`` | 8GB dual-channel DDR4-2133MHz, up to 16GB | No issues |
| ``GPU`` | Intel HD Graphics 620 | No issues |
| ``dGPU`` | AMD Radeon HD 8550M/R5 M230 (2GB GDDR3 VRAM) | Not support. ACPI should be patched to disable dGPU |
| ``Storage`` | Samsung 860 EVO 250GB SATA-III | No issues |
| ``Screen`` | 15.6" Full HD 60Hz, 1920 x 1080 TN |  No issues |
| ``Webcam`` | Windows Hello built-in IR HD webcam (1MP / 720P) |  No issues. Windows Hello is not supported in macOS |
| ``Ethernet`` | RJ45 RTL8111 Realtek Ethernet | No issues |
| ``WiFi`` | Intel Wireless-AC 3165 | No issues, using [itlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) and [Heliport](https://github.com/OpenIntelWireless/HeliPort/releases) |
| ``Input & Output`` | USB 3.0 (USB-A) x3 | No issues |
| - | HDMI 1.4 | No issues |
| - | VGA | No issues |
| ``Soundboard`` | Realtek ALC256 (ALC3246) | No issues |
| ``Battery`` | 47WHr | About 3-5h after proper Power Management configuration. |
| ``Keyboard`` | - | No issues |
| ``Touchpad`` | Dell Touchpad | No issues. ACPI should be patched to enable gesture |
| ``Dimensions`` | 23.65mm x 260mm x 380mm | - |
| ``Weight`` | 2.29 kg | ACPI patches will not help with this. |
| ``Power`` | 60W power adapter | - |

## Gratitude

* [Dortania](https://dortania.github.io/) - for Vanilla guides
* [Acidanthera](https://github.com/acidanthera) - for OpenCore and lots of kexts
* [RehabMan](https://github.com/RehabMan) - for ACPI patching guides
* [Stonevil](https://github.com/stonevil) - for BIOS mod and hardware suggestions

### Where to begin

**Use Dortania's guide for doing config.plist and create USB Installer**

* [OpenCore Vanilla Laptop guide](https://dortania.github.io/OpenCore-Install-Guide)
and you must have some research then...