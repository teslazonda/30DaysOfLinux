# Day 22: Network Configuration Manager

## LPIC-1 Objective 109.2
<br></br>

## Notes

Modern Network Interface Cards (NIC) have the following naming conventions:

* Typical port configuration is _tyL_
  * Where _ty_ is:
    * **en** = Ethernet
    * **wl** = Wireless LAN
    * **ww** = Wireless WAN

  * Where _L_ is the location (port and slot) on the PCI bus:
    * **p0s8** = Port 0, slot 8 on the PCI bus

### Commands

To show a short list of network interfaces on your device use: `ip -br addr show`

Show the system's routing table: `ip route`
