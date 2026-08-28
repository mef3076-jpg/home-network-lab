# Home Network Lab

## Overview

Built a personal home networking lab using an OpenWrt-based router to develop hands-on experience with network administration, DNS management, IPv6 troubleshooting, Linux systems, and network monitoring.

This lab uses a cellular internet connection and a custom router configuration to practice real-world IT tasks including network configuration, troubleshooting, security filtering, and system monitoring.

---

## Goals

- Build hands-on networking experience in a real environment
- Learn router administration and troubleshooting
- Understand IPv4, IPv6, DNS, DHCP, and routing concepts
- Improve network security and visibility
- Practice documenting technical problems and solutions

---

## Hardware

**Router**
- Hiveton H5000M

**Cellular Modem**
- Quectel RM551

**Lab System**
- Development board

**Network**
- Ethernet LAN
- WiFi clients

---

## Software

- ImmortalWrt 24.10
- AdGuard Home
- Linux shell
- UCI configuration system
- BusyBox utilities

---

# Projects

## DNS Filtering and Network Security

### Objective
Create network-wide DNS filtering to reduce unwanted advertisements and improve security.

### Completed Work
- Installed and configured AdGuard Home
- Integrated DNS filtering into the home network
- Tested DNS resolution and troubleshooting
- Reviewed router DNS configuration

### Skills Demonstrated
- DNS troubleshooting
- Linux service management
- Network security fundamentals
- Router configuration


---

## Cellular Signal Monitoring Dashboard

### Objective
Create a way to monitor cellular modem performance and network information.

### Completed Work
- Used router system information through UBUS
- Created scripts to collect modem statistics
- Built a dashboard displaying:
  - Signal strength
  - Signal quality
  - Network mode
  - Serving band
  - Temperature
  - Voltage information

### Skills Demonstrated
- Linux scripting
- Network monitoring
- Data collection
- Troubleshooting


---

# Troubleshooting Cases

## IPv6 Address Assignment Issues

**Problem:**  
Some devices were not consistently receiving IPv6 addresses.

**Investigation:**
- Reviewed IPv6 interface settings
- Checked DHCPv6 and router advertisement behavior
- Tested IPv6 connectivity

**Status:**  
Continuing investigation.


---

## Network Performance Changes During Device Sleep

**Problem:**  
Network performance changes when the final LAN device enters sleep mode.

**Investigation:**
- Monitoring router behavior
- Reviewing network interfaces
- Checking modem behavior

**Status:**  
Continuing investigation.


---

## Skills Learned

- IPv4 and IPv6 networking
- DNS troubleshooting
- DHCP/DHCPv6 concepts
- Router administration
- Linux command line
- Shell scripting
- Network monitoring
- Technical documentation

---

## Screenshots

Screenshots and additional documentation will be added as the project develops.
