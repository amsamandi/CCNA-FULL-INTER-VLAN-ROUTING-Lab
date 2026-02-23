Full Inter-VLAN Routing Network

## Overview

This lab demonstrates full Inter-VLAN Routing in a multi-VLAN enterprise network using Router-on-a-Stick. Devices in different VLANs communicate through a router using 802.1Q trunking.

Built and tested using Cisco Packet Tracer.

---

## Network Design

VLANs configured:

| VLAN | Name  | Network         | Gateway      |
| ---- | ----- | --------------- | ------------ |
| 10   | SALES | 192.168.10.0/24 | 192.168.10.1 |
| 20   | HR    | 192.168.20.0/24 | 192.168.20.1 |
| 30   | IT    | 192.168.30.0/24 | 192.168.30.1 |

Switch connected to router using trunk link.

---

## Key Configuration

Router subinterfaces:

interface g0/0.10

encapsulation dot1Q 10

ip address 192.168.10.1 255.255.255.0

interface g0/0.20

encapsulation dot1Q 20

ip address 192.168.20.1 255.255.255.0

interface g0/0.30
encapsulation dot1Q 30
ip address 192.168.30.1 255.255.255.0

Switch trunk:

interface fa0/24
switchport mode trunk

## Verification

Commands used:

* show vlan brief
* show interfaces trunk
* show ip route

Connectivity tested using ping between VLANs. All VLANs successfully communicate.

---

## Skills Demonstrated

* VLAN configuration
* 802.1Q trunking
* Inter-VLAN Routing
* Router-on-a-Stick
* Enterprise network segmentation
* Troubleshooting and verification

---

## Lab File

CCNA LAB 6 – Full Inter-VLAN Routing Network (.pkt)

---

## Author

Amir Samandi
CCNA Certified
