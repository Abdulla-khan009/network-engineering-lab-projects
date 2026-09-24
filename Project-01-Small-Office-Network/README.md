
# Project 01 — Small Office Enterprise Network

A hands-on **small office enterprise network simulation** designed and implemented using **Cisco Packet Tracer**.

The project demonstrates practical skills in network design, VLAN segmentation, switching, routing, DHCP, NAT/PAT, ACL-based security, simulated Internet connectivity, and network troubleshooting.

---

## 📌 Project Overview

The objective of this project was to design and configure a small company's network where different departments are separated using VLANs while still allowing controlled communication between internal networks and the Internet.

The network includes:

* Multiple departmental VLANs
* Inter-VLAN routing
* DHCP services
* NAT/PAT
* Guest network isolation
* Access control using extended ACLs
* Switch management
* STP and PortFast
* Basic port security
* Simulated ISP and Internet connectivity
* End-to-end connectivity testing

---

## 🏗️ Network Topology

### Network Architecture

```text
                         Simulated Internet
                                │
                         Internet Router
                                │
                           ISP Router
                                │
                                │
                              R1
                       Company Router
                                │
                         802.1Q Trunk
                                │
                              SW1
                         Main Switch
                         /         \
                  802.1Q Trunk      Servers
                     │
                    SW2
                Access Switch
                /    |    \
              PCs   PCs   Guest PCs
```

The topology uses **Router-on-a-Stick** to provide inter-VLAN routing through a single router interface with multiple 802.1Q subinterfaces.

---

## 🖥️ Devices Used

| Device          | Quantity | Purpose                            |
| --------------- | -------: | ---------------------------------- |
| Cisco Router    |        1 | Inter-VLAN routing, DHCP, NAT, ACL |
| Cisco Switch    |        2 | VLANs, trunking, STP               |
| ISP Router      |        1 | Simulated ISP                      |
| Internet Router |        1 | Simulated Internet routing         |
| Server          |       1+ | Simulated Internet/server services |
| PCs             | Multiple | Department and guest clients       |

---

## 🌐 VLAN & IP Addressing Plan

| VLAN | Department | Network | Gat
