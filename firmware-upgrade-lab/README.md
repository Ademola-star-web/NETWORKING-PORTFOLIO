# Cisco Firmware Upgrade Lab

## Overview
This project documents a lab-based demonstration of performing **firmware upgrades** on Cisco devices using **SolarWinds Network Configuration Manager (NCM)**. The process includes upgrade planning, execution, verification, and rollback strategy.

## Objectives
- Upgrade Cisco device firmware to the latest stable release.
- Use SolarWinds NCM for automation and centralized management.
- Document a rollback plan to ensure safe recovery in case of failure.

## Tools & Technologies
- Cisco IOS routers and switches
- SolarWinds Network Configuration Manager (NCM)
- TFTP server for image transfer
- Windows Server for SolarWinds deployment

## Upgrade Process
1. **Preparation**
   - Backup current running configuration.
   - Download the correct firmware image from Cisco.
   - Verify the image integrity using MD5 checksum.

2. **Upload Firmware**
   - Transfer the firmware image to the device via TFTP:
     ```txt
     copy tftp: flash:
     ```
   - Set the new boot variable:
     ```txt
     boot system flash:<new_image.bin>
     ```

3. **Apply Changes**
   - Save configuration:
     ```txt
     write memory
     ```
   - Reload the device:
     ```txt
     reload
     ```

4. **Verification**
   - Confirm firmware version with:
     ```txt
     show version
     ```
   - Test network services and connectivity.

## Rollback Plan
- If the device fails to boot or experiences performance issues:
  1. Boot from the old firmware image.
  2. Restore the backup configuration.
  3. Test and confirm normal operation.

## Skills Demonstrated
- Cisco IOS firmware management
- SolarWinds NCM automation
- Change control and rollback strategy
- Configuration backup and recovery
