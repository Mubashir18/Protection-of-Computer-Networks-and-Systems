# Enterprise Network Architecture: High Availability & Security 🌐

This repository contains a complete **Cisco Packet Tracer** simulation of a resilient enterprise network. The project focuses on ensuring 99.9% uptime through redundancy protocols and securing the network infrastructure against unauthorized access.

---

## 🏗️ Topology Overview
The network connects a **Main Office** (High Availability Cluster) to a **Remote Branch** via an **ISP (Internet Service Provider)**.



### **Core Components:**
* **Main Office:** Dual-router setup (R2 & R3) for failover.
* **Core Switch:** SW1 managing internal VLANs and link aggregation.
* **ISP (R1):** Simulating the internet cloud and external routing.
* **Branch Office (R4):** Remote site connectivity via OSPF.

---

## 🛠️ Implemented Technologies & Features

### **1. High Availability (Redundancy)**
* **HSRP (Hot Standby Router Protocol):** Configured on R2 (Active) and R3 (Standby) to provide a Virtual Gateway IP (`192.168.32.2`). If the primary router fails, the standby takes over instantly.
* **EtherChannel (Link Aggregation):** Grouped multiple physical links between the routers and SW1 to increase bandwidth and provide link-level redundancy.

### **2. Routing & Connectivity**
* **Dynamic Routing (OSPF):** Area 0 implementation across all routers for automated route discovery.
* **NAT/PAT:** Network Address Translation configured on the edge to allow internal private IPs to access the internet.
* **Port Forwarding:** External access enabled for the internal Web/DNS server.

### **3. Security & Management**
* **SSH (Secure Shell):** Disabled Telnet and enabled SSH for secure remote management of all network devices.
* **Access Control Lists (ACLs):** Implemented to permit NAT traffic and restrict SSH access to authorized management IPs only.

### **4. Network Services**
* **DHCP:** Automated IP addressing for both Main Office and Branch users.
* **Internal DNS:** Local name resolution for the corporate web server.

---

## 📂 Project Structure
* `Network_Redundancy_Project.pkt` - The main Cisco Packet Tracer file.
* `Device_Configs/` - Folder containing the `.txt` running-configs for R1, R2, R3, R4, and SW1.
* `Screenshots/` - Visual proof of pings, traceroutes, and protocol states.

---

## 🧪 Verification Commands
To verify the setup in Packet Tracer, use the following:

| Feature | Command |
| :--- | :--- |
| **HSRP** | `show standby brief` |
| **EtherChannel** | `show etherchannel summary` |
| **Routing** | `show ip route` |
| **NAT** | `show ip nat translations` |
| **ACL** | `show access-lists` |



---

## 🚀 How to Use
1. Download and install **Cisco Packet Tracer**.
2. Clone this repository or download the `.pkt` file.
3. Open the file to explore the configurations and test failover by deleting the link to the Active router.

**Developed by:** [Your Name/GitHub Username]
