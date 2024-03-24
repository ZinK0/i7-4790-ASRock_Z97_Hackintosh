# i7 4790 + ASRock Z97 Extreme 6 (OpenCore)

## Introduce

> I been using this build over a year and everything is OK expect the sleep. If you want to try, just give a shot.

<div style="align: center">
<img src="https://github.com/ZinK0/i7-4790-ASRock_Z97_Hackintosh/blob/main/DEMO/Info.png">
</div>

## Lanuage

English (Current)

## Note

1. Strongly recommand you to re-create USBMap.kext for your own laptop with this [tool](https://github.com/corpnewt/USBMap).
2. If you change your hardware (like wireless), re-create the USBMap.kext as well.
3. It is strong recommanded that re-generate a serial number for your own laptop (needed to be check invaluable in apple.com) !
4. Do not turn on `Find my mac`!

<!-- ## Download

[![Download from https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh/releases](https://img.shields.io/badge/Download-v0.9.9.0-blue)](https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh/releases/tag/v0.9.9.0) -->

## Infomation

<details>
<summary><strong>Booter</strong></summary>
</br>
OpenCore  0.9.7
</details>

<details>
<summary><strong>MacOS Supported/Tested</strong></summary>
</br>
- Ventura 13.0 </br>
- Sonoma 14.0 (I am using)</br>
</details>

<details>
<summary><strong>My Hardware</strong></summary>
</br>

| Model     | Description                       |
| :-------- | :-------------------------------- |
| Processor | Intel Core i7-4790                |
| Graphics  | Integrated Intel HD Graphics 4600 |
| Memory    | 8GB 1866MHz DDR3 \* 2             |
| Display   | ViewSonic 27" 2K (2560x1440)      |
| Storage   | Sandisk 152GB M.2 SATA SSD        |
| Soundcard | Realtek ALC1150                   |

</details>

<details>
<summary><strong>Kexts Version</strong></summary>
</br>

| Kexts          | Version | Updated Way      |
| :------------- | :------ | :--------------- |
| Lilu           | 1.6.7   | Official Release |
| VirtualSMC     | 1.3.3   | Official Release |
| SMCProcessor   | 1.3.3   | Official Release |
| SMCSuperIO     | 1.3.3   | Official Release |
| WhateverGreen  | 1.6.7   | Official Release |
| IntelMausi     | 1.0.7   | Official Release |
| RealtekRTL8111 | 2.4.2   | Official Release |
| AppleALC       | 1.8.7   | Official Release |

</details>

## Status

<details>
<summary><strong>What's working</strong></summary>
</br>

- [x] Intel HD 4600 Graphics `incuding graphics acceleration`
- [x] All USB ports
- [x] All fn key work (You need to setting on bios first. Go to POST Behavior -> Fn Lock Options. Check Fn Lock and Lock mode disable/standard)
- [x] Speakers and headphones jack
- [x] External mic/Headphone mic jack(Working with [combojack](https://github.com/hackintosh-stuff/ComboJack))
- [x] Intel® I218V Gigabit Ethernet
- [x] Realtek RTL8111GR Gigabit Ethernet
- [x] App Store
- [x] iMessage and Facetime
- [x] DP and HDMI with digital audio passthrough

</details>

<details>
<summary><strong>What's not working</strong></summary>
</br>
- [x] Sleep ( wake continuous I don't want to give time to get the sleep :3 )
</details>

## Recommended Bios Setup

Enable:

1. `System Configuration` -> `Integrated NIC` -> `Enabled`

   But not tick the entry:

   - [ ] `Enable UEFI NetWork`

2. `System Configuration` -> `SATA Operation` -> `AHCI`

3. `System Configuration` -> `Thunderbolt Adapter Configuration` -> Enable all entries and select

   `Security level - No security`

Disable:

1. `Secure Boot` -> `Secure Boot Enable` -> `Disabled`
2. `Intel Software Guard Extension` -> `Intel SGX Enable` -> `Disabled`
3. `General ` -> `Advanced Boot Options` -> `Enable Legacy Option ROMs` -> `Disabled` (thanks @fdotcico)

<!-- ## IGPU 4K output Enabled

This part is credited from [Lorys89-DELL_LATITUDE_7280](https://github.com/Lorys89/DELL_LATITUDE_7280).

1. Open `config.plist` and delete `framebuffer-fbmem` and `framebuffer-stolenmem` in `DeviceProperties`, `PciRoot(0x0)/Pci(0x2,0x0)`

2. Restart and at the opencore boot GUI, choose the `modGRUBShell.efi`

3. For set DVMT PRE Allocated to 64 MB

`setup_var 0x795 0x2`

![DMT-PRE](https://raw.githubusercontent.com/Lorys89/DELL_LATITUDE_7280/main/Screenshot/DVMT-PRE.png)

4. For set DVMT Total GFX Mem to MAX

`setup_var 0x796 0x3`

![DMT-PRE](https://raw.githubusercontent.com/Lorys89/DELL_LATITUDE_7280/main/Screenshot/DVMT-TOT.png)

## For Intel Wireless and Bluetooth

Now, I add a config for Intel wireless card kexts. The method to use it is as below

- Delete the existing `config.plist`
- Change `config-intel-wireless-card.plist` into `config.plist`

## ComboJack Installation -->

Hackintosh combojack support for alc256/alc255 from https://github.com/hackintosh-stuff/ComboJack

Follow this step:

- Clone combojack repository
- Run ComboJack_Installer/install.sh in terminal and reboot
- Done. When you attach a headphone there will be a popup asking about headphone type.

## Credits

- [Lovey-XPP](https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh) for README Style.
- [Dortania](https://dortania.github.io/) for installation and other guides.
- All contributors for this EFI.
