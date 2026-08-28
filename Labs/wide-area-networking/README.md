# Wide Area Networking & Dynamic Routing Lab

## Overview

This Cisco Packet Tracer project demonstrates the configuration and
testing of Wide Area Network (WAN) connectivity and dynamic routing.

The project consists of two networking labs:

1. DSL WAN connectivity and network services
2. Dynamic routing using RIPv2

The labs demonstrate how devices on separate networks can communicate
through WAN infrastructure and how routers dynamically learn routes
between multiple LANs.

## Technologies and Concepts

- Cisco Packet Tracer
- Wide Area Networks (WAN)
- DSL
- DHCP
- DNS
- HTTP
- IPv4
- RIPv2
- Dynamic Routing
- Routing Tables
- ARP
- Network Troubleshooting
- ICMP / Ping

---

## Part 1 – DSL WAN

### Objective

The objective of this lab was to create a WAN using DSL connections
and configure network services that could be accessed across the WAN.

### Network Components

The topology included:

- Two PCs
- Two switches
- Two DSL modems
- PT-Cloud
- Server

### Server Services

The server was configured to provide:

- DHCP
- DNS
- HTTP

DHCP automatically provided addressing information to network clients.

DNS provided name resolution for the web server.

HTTP provided a webpage that could be accessed by clients across the
WAN.

### Testing

Connectivity was verified using ICMP ping tests.

DNS functionality was tested by resolving the configured hostname.

Finally, a web browser was used to access the HTTP server across the
WAN.

---

## Part 2 – RIPv2 Dynamic Routing

### Objective

The objective of this lab was to enable communication between
multiple LANs using dynamic routing.

RIPv2 was configured on multiple Cisco routers so that each router
could advertise its directly connected networks and dynamically learn
remote routes.

### Example Configuration

```text
router rip
version 2
network <directly-connected-network>
