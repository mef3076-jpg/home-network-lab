# Network Baseline

## Current Network Layout

Router:
- Hiveton H5000M
- ImmortalWrt 24.10

Modem:
- RM551
- Connection mode: ECM
- Interface: usb0

## WAN Configuration

Interface:
- usb0

IPv4:
- Address assigned through DHCP
- Router receives address from modem

Default Gateway:
- Provided by cellular modem

## LAN Configuration

Interface:
- br-lan

Router IP:
- 192.168.88.1/24

LAN Services:
- DHCP server enabled
- DNS service provided by dnsmasq

## IPv6 Status

WAN:
- IPv6 address assigned successfully

LAN:
- Global IPv6 prefix assigned

Current goal:
- Verify IPv6 address assignment to client devices

## DNS Baseline

Current DNS service:
- dnsmasq

DNS flow:

Client devices
→ Router dnsmasq
→ Upstream DNS provided by modem

## DHCP Configuration Notes

IPv4:
- DHCP server enabled on LAN

IPv6:
- Router Advertisements enabled
- DHCPv6 currently disabled
- SLAAC enabled

## Skills Practiced

- Network documentation
- IP addressing
- DHCP troubleshooting
- IPv6 configuration
- DNS analysis

- ## DHCP Verification

Verified connected LAN clients using the DHCP lease table.

Current clients:
- OnePlus-12
- Blackstar

IPv4 DHCP:
- Working
- Addresses assigned from 192.168.88.0/24 network

IPv6:
- Requires separate verification because SLAAC is being used instead of DHCPv6
-
- ## IPv6 Client Verification

### Test

Command:. ## IPv6 Client Verification

### Test

Command:
### Results

Verified IPv6 connectivity after router rebuild.

Confirmed:
- WAN IPv6 address assigned
- LAN IPv6 prefix assigned
- Client devices receiving IPv6 addresses
- Router advertisements successfully reaching LAN clients

IPv6 configuration:
- DHCPv6: Disabled
- Router Advertisement: Enabled
- SLAAC: Enabled

### Skills Practiced

- IPv6 troubleshooting
- Neighbor discovery
- Router advertisement concepts
- LAN/WAN IPv6 verification
