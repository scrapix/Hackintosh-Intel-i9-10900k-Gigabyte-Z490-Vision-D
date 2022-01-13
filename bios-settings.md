# My BIOS-settings

Some BIOS-settings are recommended for the Z490 platform in general, and some BIOS-settings depend on wether you use the iMac20,2 or the iMacPro1,1 config.

## Disable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#disable):
- Legacy USB Mode (very important. Always boot to OC in UEFI mode. So when you press F12 to select the boot devices, the OC one needs to start with UEFI. E.g. "UEFI: SanDisk")
- Fast Boot
- Secure Boot
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Intel SGX (Software Guard Extension)
- Intel Platform Trust
- CFG Lock (requires a newer BIOS version F5 (This must be off, if you can't find the option then enable both AppleCpuPmCfgLock and AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

## Enable 
(reference: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#enable):
- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 10
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI

## Thunderbolt
- GPIO Force Power: Enabled
- Security: No security

## iMac20,2-specific settings:
- Internal Graphics: Enabled
- DVMT Pre-Allocated: 64MB or 128MB (for QHD+/UHD)
- DVMT Total Gfx Mem: 256M

## iMacPro1,1-specific settings:
- Internal Graphics: Disabled

## My BIOS settings for BIOS f20b with iMac20,2:

I recommend to not just copy and paste my OC settings for the 10850k. Instead, try CPU Clock Ratio set to Auto and then apply a fixed voltage of 1.3V. This way your 10900k/10850k stay cooler than stock, where the Auto Voltage sometimes goes to 1.4V and higher.

Also, always try XMP-off and CPU @ stock settings before you post about stability issues here on github ;)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2705.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2706.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2707.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2708.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2709.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2710.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2711.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2712.jpeg)

![My BIOS settings for f20b with iMac20,2](BIOS-settings/IMG_2713.jpeg)

# Z490 Vision D Configuraiton
## Tweaker
- CPU Upgrade
- CPU Base Clock
- PCIe/DMI/PEG Clock Frequency
- Enhanced Multi-Core Ratio
- Ring Ratio
- IGP Ratio
- AVX offset
- Adcanced CPU Settings
  - CPU Over Temoerature Protection
  - FCLK Frequency for Early Power On
  - Hyper-Threading Technolgy
  - No. of CPU Cores Enabled
  - # VT-d == DISABLE (can be enabled if you set DisableIoMapper to YES)
  - Intel(R) Speed Shift Technology
  - CPU Thermal Monitor
  - Ring to Core offset (Down Bin)
  - CPU EIST Function
  - Race To Halt (RTH)
  - Energy Efficient Turbo
  - Voltage Optimization
  - Intel (R) Turbi Boost Technology
  - Intel (R) Turbo Boost Max Technology 3.0
  - CPU Flex Ratio Override
  - CPU Flex Ratio Settings
  - Frequency Clipping TVB
  - Voltage reduction initiated TVB

  - Active Ratios
  - Per Core HT Disable Setting
  - C-States Control
  - Turbo Power Limits
  - Turbo Per Core Limit Control
  

- Extreme Memory Priflie (X.M.P.)
- System Memory Multiplier
- Memory Ref Clock
- Memory Odd Ratio (100/133 or 200/266)
- Advanced Memory Settings
  - Memory Multiplier Tweaker
  - Channel Interleaving
  - Rank Interleaving
  - Memory Boot Mode
  - Realtime Memory Timing
  - Memory Enhancement Settings
  - Memory Channel Detection Message
  - SPD Info
  - Memory Channels Timing

- Vcore Voltage Mode
- CPU Vcore
- Dynamic Vcore(DVID)
- BCLK Adaptive Voltage
- CPU Graphics Voltage (VAXG)
- DRAM Voltage (CH A/B)
- CPU VCCIO
- CPU System Agent Voltage
- VCC Substained
- VCCPLL
- VCCPLL OC
- VCCVTT
- PCH Core
- Advanced Voltage Settings

## Settings
Platform Power
- Platform Power Management 
- ErP
- Soft-Off bbyb PWR-BTTN
- Resume by Alarm
- Power Loading
- PC6 Render Standby
- AC BACK

IO Ports
- Internal Graphics
- Aperture Size
- PCIE Bifurcation Support
- Support Rocket Lake M2. Slot
- USB 3.0 DAC-UP 2
- OnBoard LAN Controller
- Audio Controller
- Above 4G Decoding
- PCH LAN Controller
- Wake on LAN Enable
- IOAPIC 24-119 Entries
- Thunderbolt(TM) Configuration
- USB Configuration
- Network Stack Configuration
- NVMe Configuration
- SATA And RST Configuration
- EZ RAID

## Miscellaneous
- LEDs in System Power On State
- Leds in Sleep, Hibernation and Soft Off States
- Onboard DB Port LED
- Intel Platform Trust Technology (PTT)
- Software Guard Extensions (SGX)
- 3DMark01 Enhancement
- CPU PCIe Link Speed
- Trusted Computing
  - Security Device Support
  - Active PCR banks
  - Acailable PCR banks
  - SHA-1 PCR BANK
  - SHA256 PCR Bank

  - Pending operation
  - Platform Hierarchy
  - Storage Hierarchy
  - Endorsement Hierarchy
  - TPM2.0 UEFI Spec Version
  - Physical Presence Spec Version
  - TPM 20 Interface Type
  - Device Select
  - Disable Block Sid

PC Health Status
Smart Fan 5


## Boot
Bootup Numlock State
# CFG Lock == Disabled
Security Option
Full Screen LOGO Show

Boot Option Priorities

Fast Boot
Mouse Speed
Windows 10 Features
CSM Support
Administratior Password
User Password
Secure Boot
# - Secure Boot Enable == Disable
- Secure Boot Mode

Preferred Operation Mode


