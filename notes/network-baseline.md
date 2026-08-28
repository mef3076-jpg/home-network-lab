I# Network Baseline

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

## AdGuard Preparation

Checks completed:

- AdGuard Home not installed
- Router configuration backup created
- Storage verified

Storage:
- Overlay available space: ~7GB

Status:
Ready for AdGuard Home installation

## AdGuard Installation

Installed:
- AdGuard Home 0.107.57-r1

Binary:
- /usr/bin/AdGuardHome

Status:
- Installed
- Not enabled yet

Reason:
- DNS port 53 currently owned by dnsmasq

Next:
- Reconfigure dnsmasq for DHCP only
- Configure AdGuard Home as DNS server

## AdGuard Home Service Started

Status:
- Installed
- Enabled
- Running

Verification:
- AdGuard Home listening on TCP port 3000

Current DNS:
- dnsmasq still owns port 53

Next:
- Configure AdGuard
- Migrate DNS service
- Test client DNS filtering## AdGuard Home Configuration

Status:
- Installed
- Running

Web Interface:
- Port: 8080

DNS Service:
- Port: 5353 (temporary)

Current DNS ownership:
- dnsmasq: port 53
- AdGuard Home: port 5353

Upstream DNS:
- Quad9 DNS over HTTPS

Current migration plan:
1. Verify AdGuard works
2. Move DNS from dnsmasq to AdGuard
3. Test client devices
4. Add filtering list

## DNS Testing

Installed:
- bind-dig DNS troubleshooting tools

Verification:

Command:
dig @127.0.0.1 -p 5353 google.com

Result:
- AdGuard Home responded successfully
- Upstream DNS resolution working
- Quad9 DoH upstream configured

Current state:
- dnsmasq handles client DNS
- AdGuard running on port 5353
- ## DNS Migration - Phase 1 Complete

Changed dnsmasq forwarding:

Before:
Client → dnsmasq → modem DNS

After:
Client → dnsmasq → AdGuard Home → Quad9 DoH

Configuration:
dnsmasq upstream:
127.0.0.1#5353

Verification:
- DNS resolution successful
- AdGuard Home responding
- No client DHCP changes required

Next:
- Verify client queries appear in AdGuard
- Add blocklists
- Test DNS filtering
