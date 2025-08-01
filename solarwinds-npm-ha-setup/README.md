# SolarWinds Orion NPM High Availability Setup

## Overview
This project documents the configuration of a **High Availability (HA)** deployment for **SolarWinds Orion Network Performance Monitor (NPM)** with an additional polling engine to ensure redundancy and uninterrupted network monitoring.

## Objectives
- Maintain continuous monitoring during server outages.
- Improve device polling efficiency.
- Minimize downtime for critical network monitoring services.

## Tools & Technologies
- **SolarWinds Orion NPM, NCM, NTA**
- **Windows Server 2019**
- **SNMP v3** (AES256 encryption, SHA authentication)
- Virtualization: VMware ESXi / Hyper-V (for lab environment)

## Steps Taken
1. **Installed Primary Orion Server** – Configured with SNMP v3 credentials for all monitored devices.
2. **Deployed Secondary Polling Engine** – Installed on a separate server to share polling load.
3. **Configured HA Pool** – Enabled and paired both servers in the SolarWinds HA settings.
4. **Tested Failover** – Simulated a primary server outage and verified seamless transition.
5. **Monitored Performance** – Used NPM dashboards to confirm polling distribution and uptime.

## Configuration Notes
- Primary Server: OrionNPM01 – 192.168.10.100
- Secondary Server: OrionNPM02 – 192.168.10.101
- Polling Interval: 120 seconds
- SNMP Credentials: v3 with encryption and authentication

## Screenshots
> *(Add your own SolarWinds HA dashboard and failover test screenshots here)*

## Skills Demonstrated
- SolarWinds Orion Suite configuration (NPM, NCM, NTA)
- High Availability design & implementation
- SNMP-based network monitoring
- Failover testing & verification
- IT documentation best practices
