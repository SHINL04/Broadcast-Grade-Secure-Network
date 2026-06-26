 Broadcast-Grade Secure Network
## Overview

This project simulates a broadcast media organization's enterprise network using Cisco Packet Tracer. The network is designed to demonstrate VLAN segmentation, inter-VLAN communication, dynamic routing with OSPF, Router-on-a-Stick architecture, and secure connectivity between a Headquarters (HQ) site and a Remote Office.

The project was built as part of a networking portfolio to demonstrate practical skills in network design, routing, switching, troubleshooting, and enterprise network implementation.

## Network Architecture

### Headquarters (HQ)

The HQ site contains:

* Core Switch
* HQ Router
* Multiple VLANs representing departments:

  * VLAN 10 – NEWS
  * VLAN 20 – SPORTS
  * VLAN 30 – EDITING
  * VLAN 40 – IT
  * VLAN 50 – MEDIA

### Remote Office

The Remote Office contains:

* Remote Router
* Remote Laptop
* Dedicated Remote Office subnet

### WAN Link

A point-to-point connection connects HQ and the Remote Office.

* HQ Router: 10.0.0.1/30
* Remote Router: 10.0.0.2/30

Dynamic routing is provided through OSPF Area 0.

---

## Technologies Implemented

* Cisco Packet Tracer
* VLAN Segmentation
* IEEE 802.1Q Trunking
* Router-on-a-Stick (ROAS)
* OSPF Dynamic Routing
* IPv4 Addressing
* Inter-VLAN Routing
* Enterprise Network Design
* Network Troubleshooting

---

## IP Addressing Plan

| Network         | Purpose       | Gateway      |
| --------------- | ------------- | ------------ |
| 192.168.10.0/24 | NEWS          | 192.168.10.1 |
| 192.168.20.0/24 | SPORTS        | 192.168.20.1 |
| 192.168.30.0/24 | EDITING       | 192.168.30.1 |
| 192.168.40.0/24 | IT            | 192.168.40.1 |
| 192.168.50.0/24 | MEDIA         | 192.168.50.1 |
| 192.168.60.0/24 | Remote Office | 192.168.60.1 |
| 10.0.0.0/30     | HQ–Remote WAN | N/A          |

---

## Key Features

### VLAN Segmentation

Separate VLANs were created to isolate departments and reduce broadcast traffic.

### Router-on-a-Stick

A single physical router interface uses multiple 802.1Q subinterfaces to provide inter-VLAN routing.

### OSPF Dynamic Routing

OSPF Area 0 dynamically exchanges routes between the HQ and Remote Office routers.

### End-to-End Connectivity

The Remote Office laptop successfully communicates with the Media Server located in VLAN 50 at HQ.

---

## Validation Tests

The following tests were successfully completed:

* OSPF Neighbor Adjacency = FULL
* VLAN Connectivity Verified
* Trunk Link Operational
* Inter-VLAN Routing Functional
* HQ-to-Remote Routing Functional
* Laptop-to-Media Server Connectivity Verified
* End-to-End ICMP Testing Successful

Example:

Remote Laptop (192.168.60.10)

↓

Remote Router (192.168.60.1)

↓

OSPF WAN Link (10.0.0.0/30)

↓

HQ Router

↓

Core Switch

↓

Media Server (192.168.50.10)

Result: Successful Connectivity

---

## Project Screenshots

### Network Topology

![Topology](screenshots/01-network-topology.png)

### VLAN Configuration

![VLAN](screenshots/02-vlan-configuration.png)

### Trunk Configuration

![Trunk](screenshots/03-trunk-configuration.png)

### Router-on-a-Stick

![ROAS](screenshots/04-router-on-a-stick.png)

### OSPF Neighbor Relationship

![OSPF Neighbor](screenshots/05-ospf-neighbor.png)

### Routing Table

![Routing Table](screenshots/06-routing-table.png)

### OSPF Configuration

![OSPF Config](screenshots/07-ospf-config.png)

### End-to-End Connectivity Test

![Ping Test](screenshots/08-end-to-end-ping.png)

### Media Server Configuration

![Server](screenshots/09-server-config.png)

### Remote Laptop Configuration

![Laptop](screenshots/10-laptop-config.png)

---

## Lessons Learned

During this project I gained practical experience with:

* VLAN deployment and management
* 802.1Q trunk configuration
* Router-on-a-Stick implementation
* OSPF configuration and troubleshooting
* Enterprise network troubleshooting methodology
* Route propagation and verification
* End-to-end connectivity testing

---

## Author

Shafi Islam Nabil

Aspiring Network Administrator | Network Engineering Student | Cisco Packet Tracer Enthusiast
