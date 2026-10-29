# Protection of Computer Networks and Systems

Lab work for *Protection of Computer Networks and Systems* (HSE University, 2025–2026), built in Cisco Packet Tracer.

The labs go from physical cabling and basic IOS commands to a redundant, secured enterprise network.

## Highlight: enterprise network redundancy and security

[`enterprise-network-redundancy-security`](./enterprise-network-redundancy-security) is the capstone lab. A main office with two routers connects to a remote branch through an ISP.

- **HSRP** gives the office a shared virtual gateway, so traffic fails over when one router goes down.
- **OSPF** handles dynamic routing between office, ISP and branch.
- **EtherChannel** bundles switch links for bandwidth and link redundancy.
- **NAT/PAT** translates internal addresses for internet access.
- **SSH and ACLs** restrict device management and filter traffic.

The folder contains the `.pkt` topology, the full device configuration and a write-up.

## All labs

| Folder | Topics |
|---|---|
| Root files | Network representation, logical vs. physical mode, IOS navigation basics (`.pka` + config files, `Report.pdf`) |
| [`Physical Layer & Seminar Labs`](./Physical%20Layer%20%26%20Seminar%20Labs) | Physical-layer connectivity and a multi-branch network topology (config + report) |
| [`Network Configuration and Connectivity Labs`](./Network%20Configuration%20and%20Connectivity%20Labs) | Initial switch configuration, wired and wireless LAN, IPv4 subnetting, basic connectivity (`Report.pdf`) |
| [`enterprise-network-redundancy-security`](./enterprise-network-redundancy-security) | HSRP, OSPF, EtherChannel, NAT/PAT, SSH, ACLs |

## How to open

Install [Cisco Packet Tracer](https://www.netacad.com/cisco-packet-tracer) (8.x) and open any `.pka` or `.pkt` file. Device configurations are also included as plain-text files.
