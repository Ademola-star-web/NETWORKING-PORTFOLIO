# Onboarding Devices in SolarWinds NPM

## Overview
This project demonstrates the process of adding network devices into **SolarWinds Network Performance Monitor (NPM)** for proactive monitoring. It covers both **single node onboarding** and **network discovery** methods.

## Prerequisites
- SNMP enabled on network devices (v2c or v3).
- SNMP credentials configured in SolarWinds.
- ICMP (ping) allowed from the Orion server.
- Device firewall rules permitting SNMP/WMI traffic.

## Steps
### Method 1 – Add Single Node
1. Navigate to **Settings → Manage Nodes → Add Node**.
2. Enter device IP/hostname and SNMP credentials.
3. Test connection and select monitored interfaces.
4. Save and verify device status.

### Method 2 – Network Discovery
1. Go to **Settings → Network Discovery → Add New Discovery**.
2. Enter IP range or subnet to scan.
3. Add SNMP/WMI credentials.
4. Review discovered devices and import into NPM.

## Example SNMP Config (Cisco IOS)
```txt
snmp-server community NOCstring RO
snmp-server location DataCenter
snmp-server contact noc@example.com
