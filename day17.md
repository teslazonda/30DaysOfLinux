# Day 17: Exploring Network Masking

## LPIC-1 Objective 109.1
<br></br>

## Notes

IP addresses have two parts. The first part with the first three decimal points is the Network address. The number following the final decimal point is the Host ID.

For example: `142.250.72.78` has a network of `142.250.72` and a Host of `78`.


### IPv6 Address Masking:

* 128-bits in length
  * Network is the first 64 bits
  * Host is the last 64 bits

The network half of a IPv6 address is sometimes called the _Routing_ , while the Host may be called the _Interface ID_ .

### IPv4 Address Masking (old):

Class A:

* Netmask `255.0.0.0`
  * Network in the first quad
  * Host in the last 3 quads
  * Example: <u>142.</u>250.72.78 (network underlined)

Class B:

* Netmask `255.255.0.0`
  * Network in the first 2 quads
  * Host in the last 2 quads
  * Example: <u>142.250.</u>72.78 (network underlined)


Class C:

* Netmask `255.255.255.0`
  * Network in the first 3 quads
  * Host in the last quad
  * Example: <u>142.250.72.</u>78 (network underlined)


### IPv4 Address Masking (modern via CIDR):

CIDR notation makes use of a / at the end of the IP address to denote the number of bits that are a part of the network. The remaining bits are part of the Host.
