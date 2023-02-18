# Day 18: Discerning Network Address Standards

## LPIC-1 Objective 109.1
<br></br>

## Notes

NAT (Network Address Translation) - converts private to public IP address and vice versa on IPv4 connections.

## IPv4 Private Addresses

* Only for local networks

* Not allowed for public IP address use

* Private IP addresses ranges:
  * `10.0.0.0` to `10.255.255.255`
  * `172.16.0.0` to `172.31.255.255`
  * `192.168.0.0` to `192.168.255.255`

## IPv6 Private Addresses

Called _site-local_ instead of private.

Site-local IP addresses start with:
* fec
* fed
* fee
* fef

**Site-Local addressing is DEPRECATED:** USE a unique IPv6 address instead.

## Link-local Addresses (IPv4)

Packets with these IP addresses are kept on the local network, and are not routed publicly.

IPv4 includes private address ranges and APIPA (Automatic Private IP Adressing) addresses.

* Assigned APIPA address if:
  * Dynamic Host Configuration Protocol (DHCP) system fails or other IP assigning method fails

* **APIPA address range:** `169.254.0.0` to `169.254.255.255`


## Link-local Addresses (IPv6)

* Always assigned this address along with routable IP address

* Often use MAC address to create this address.

* Addresses start with `fe80:0000:0000:0000:0000`
  * `fe80::` (shortened)
