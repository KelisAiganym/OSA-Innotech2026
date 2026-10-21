# Lab 0 — Inventory My Own Machine

**Week:** 1  
**Outcome:** CLO 1  
**Operating System:** Windows 10/11

## Inventory

| What | Value | Where I got it |
|---|---|---|
| CPU model | Intel Core i5-11400H @ 2.70 GHz | `Get-CimInstance Win32_Processor` |
| CPU core count | 6 | `Get-CimInstance Win32_Processor` |
| CPU thread count | 12 | `Get-CimInstance Win32_Processor` |
| Total installed RAM | 16 GB (15.73 GB reported by Windows) | `Get-CimInstance Win32_PhysicalMemory`; `Get-CimInstance Win32_ComputerSystem` |
| Installed memory modules | 1 detected module | `Get-CimInstance Win32_PhysicalMemory` |
| Memory speed | 3200 MT/s | `Get-CimInstance Win32_PhysicalMemory` |
| Memory manufacturer | Micron Technology | `Get-CimInstance Win32_PhysicalMemory` |
| Disk model | INTEL SSDPEKNU512GZ | `Get-PhysicalDisk` |
| Disk type | NVMe SSD | `Get-Disk` |
| Disk capacity | 476.94 GB | `Get-PhysicalDisk` |
| Free space on VM volume C: | 94.05 GB | `Get-Volume -DriveLetter C` |
| Firmware type | UEFI | `Get-ComputerInfo -Property BiosFirmwareType` |
| Firmware version | FX506HM.318 | `Get-CimInstance Win32_BIOS` |
| Firmware release date | 2025-06-17 | `Get-CimInstance Win32_BIOS` |
| Hardware virtualization supported | Yes | `Get-CimInstance Win32_Processor` |
| Hardware virtualization enabled | Yes | `Get-CimInstance Win32_Processor` |
| SLAT supported | Yes | `Get-CimInstance Win32_Processor` |

## What did not work

As this was my first time working with PowerShell and GitHub, I found several steps difficult at first. I needed extra attempts to understand how to run the commands correctly, save the command outputs as evidence files, and organize the files in the correct repository folders. I also needed to run an additional command to confirm the NVMe bus type. I learned how to correct these issues and organize my evidence properly

## Virtualization

Hardware virtualization is supported and enabled. VM monitor mode extensions and Second Level Address Translation (SLAT) are available. The system uses UEFI firmware.
