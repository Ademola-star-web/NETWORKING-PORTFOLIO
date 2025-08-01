# Cisco NetFlow Configuration & Integration with SolarWinds NTA

## Overview
This project demonstrates how to configure **NetFlow v9** on Cisco routers and integrate it with **SolarWinds NetFlow Traffic Analyzer (NTA)** to capture, analyze, and visualize network traffic.

## Objectives
- Enable NetFlow for real-time traffic visibility.
- Export NetFlow data to SolarWinds NTA for analysis.
- Create dashboards for bandwidth usage, top talkers, and application traffic.

## Tools & Technologies
- Cisco IOS-based routers and switches
- NetFlow v9
- SolarWinds NetFlow Traffic Analyzer (NTA)
- SNMP v2/v3 for device monitoring

## Configuration Steps
1. **Enable NetFlow Export**
   ```txt
   ip flow-export destination 192.168.10.50 2055
   ip flow-export version 9
   ip flow-cache timeout active 1
   ip flow-cache timeout inactive 15
