# Firewall Baseline

## Firewall Zones

### LAN Zone

Purpose:
- Trusted internal network

Configuration:
- Input: Accept
- Output: Accept
- Forward: Accept

### WAN Zone

Interfaces:
- WAN
- WAN6
- USB
- USBv6

Configuration:
- Input: Reject
- Output: Accept
- Forward: Reject
- NAT enabled

## Traffic Flow

LAN devices are allowed to forward traffic to WAN.

Example:

Device
→ LAN
→ Firewall
→ USB WAN
→ Internet

## Security Notes

Inbound WAN traffic is blocked by default unless explicitly allowed.

## Skills Practiced

- Firewall zones
- NAT concepts
- Network segmentation
- Traffic flow analysis
