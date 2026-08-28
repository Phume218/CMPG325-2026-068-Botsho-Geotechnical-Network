# CMPG325-2026-068 — Botsho Geotechnical Engineers Network

## Project Overview

This repository contains the design, implementation, testing and documentation for the CMPG325 Computer Networks project assigned to Botsho Geotechnical Engineers in Potchefstroom.

The network will be designed and implemented using Cisco Packet Tracer.

## Project Information

| Item | Details |
|---|---|
| Project ID | CMPG325-2026-068 |
| Client ID | CLI-068 |
| Organisation | Botsho Geotechnical Engineers |
| Location | Potchefstroom |
| Industry | Engineering |
| Addressing Block | 172.30.42.0/23 |
| Networking Challenge | DHCP — Scoped Multi-VLAN Address Assignment |
| Design Constraint | Critical file/print/application services must remain available during business hours |
| Change Request | CR8 — Shared printer zone for two departments |
| Simulation Tool | Cisco Packet Tracer |

## Milestone 1 — Client Design Review

Milestone 1 focuses on the initial network design and includes:

- Client requirements
- Physical topology
- Logical topology
- IP addressing plan
- Initial GitHub repository

## Proposed Network Design

The network currently contains four VLANs:

| VLAN | Name         | Purpose                             |
|---:|----------------|-------------------------------------|
| 10 | ENGINEERING    | Engineering departmental users      |
| 20 | ADMINISTRATION | Administration departmental users   |
| 30 | SHARED-PRINTER | Shared printer zone required by CR8 |
| 40 | SERVERS        | Critical file/application services  |

Engineering and Administration are design assumptions used for the Packet Tracer simulation because the client brief requires two departments but does not specify their names.

## IP Addressing Summary

| VLAN | Network | Gateway |
|---:|---|---|
| 10 | 172.30.42.0/26 | 172.30.42.1 |
| 20 | 172.30.42.64/26 | 172.30.42.65 |
| 30 | 172.30.42.128/28 | 172.30.42.129 |
| 40 | 172.30.42.144/28 | 172.30.42.145 |

### Infrastructure Addresses

Shared Printer:

172.30.42.130/28

Server:

172.30.42.146/28

## DHCP Design

Two DHCP scopes will be implemented.

### Engineering

Network: 172.30.42.0/26  
Gateway: 172.30.42.1  
DHCP range: 172.30.42.10–172.30.42.62

### Administration

Network: 172.30.42.64/26  
Gateway: 172.30.42.65  
DHCP range: 172.30.42.70–172.30.42.126

## CR8 — Shared Printer Zone

A dedicated Shared-Printer VLAN will allow both Engineering and Administration users to access a common network printer through inter-VLAN routing.

The printer will use the static address:

172.30.42.130/28

## Repository Structure

The repository will progressively contain:

Milestone-1/  
Packet-Tracer/  
Evidence/  
Troubleshooting/  
Reflection/

Evidence from the implementation and testing phases will be added as the project develops.

## Current Project Status

Milestone 1: Client Design Review

Current activities include network requirements analysis, topology design, IP addressing and preparation for Cisco Packet Tracer implementation.
Initial repository setup and README
