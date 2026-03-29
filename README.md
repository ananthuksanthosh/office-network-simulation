🏢 Enterprise Office Network Simulation (GNS3)

📌 Overview

This project demonstrates the design and implementation of an enterprise office network using GNS3.
It is built using a core–edge architecture and integrates key networking concepts such as routing, NAT, DHCP, and firewall security using Access Control Lists (ACLs).

The objective is to simulate a secure and scalable office environment with controlled access between internal departments and external users.

---

🏗️ Network Architecture

The network consists of the following components:

- Core Router (CORE-RTR): Handles internal routing and enforces firewall policies
- Edge Router (EDGE-RTR): Provides internet connectivity using NAT
- Core Switch (CORE-SW): Connects internal office devices
- Office Network: HR, IT, and Finance departments
- Admin Network: Secure subnet with restricted access
- Customer Network: DHCP-enabled external network

---

🌐 IP Addressing Scheme

Network| Subnet| Description
Core ↔ Edge| 10.0.0.0/24| Router-to-router communication
Office Network| 192.168.10.0/24| HR, IT, Finance
Admin Network| 192.168.20.0/24| Secure admin systems
Customer Network| 192.168.50.0/24| DHCP-based users

---

⚙️ Features Implemented

- Static IP addressing for internal office systems
- DHCP configuration for customer network
- NAT for internet connectivity
- Static routing between routers
- Firewall implementation using extended ACL
- Network segmentation for improved security

---

🔐 Security Implementation

An extended ACL is configured on the core router to enforce access control:

- Admin network has full access to all networks
- Office and customer networks cannot access the admin network
- ACL rules are applied on multiple interfaces to ensure complete protection

---

🔄 Data Flow

Office Users:
PC → Switch → Core Router → Edge Router → Internet

Customer Users:
Device → Switch → Edge Router → Internet

Admin Users:
Admin can access all internal and external networks

---

🚀 How to Run

1. Install GNS3 and Oracle VM VirtualBox
2. Download the project file from the link below
3. Import the project into GNS3
4. Start all devices
5. Open VPCS terminals
6. Test connectivity using ping commands

---

⭐ Highlights

- Designed a multi-network enterprise topology
- Implemented firewall security using ACL
- Configured DHCP for dynamic IP allocation
- Enabled internet access using NAT
- Applied network segmentation for access control

---

🧪 Verification

Screenshots demonstrating key functionalities are available in the "screenshots/" folder:

- "topology.png" → Network topology
- "network-working.png" → Internal communication
- "firewall-block-test.png" → Firewall blocking IT → Admin
- "firewall-block-hr.png" → Firewall blocking HR → Admin
- "firewall-allow-test.png" → Admin access to all networks
- "dhcp-auto-assignment.png" → DHCP IP allocation
- "internet-access-NAT.png" → Internet connectivity

---

🧠 Design Decisions

- Admin network is separated to enhance security
- DHCP is used for customer network to simplify configuration
- NAT is implemented on edge router for internet access
- Firewall is applied on core router to protect internal resources

---

💼 Skills Demonstrated

- Network Design and Topology Planning
- IP Addressing and Subnetting
- Static Routing
- NAT Configuration
- DHCP Configuration
- Firewall Implementation (ACL)
- Network Security Fundamentals

---

🔮 Future Improvements

- Implement VLAN segmentation for departments
- Use OSPF for dynamic routing
- Add VPN for secure remote access
- Enhance firewall with port-based filtering

---

🧰 Tools & Technologies

- Cisco 7200 Router (IOS)
- GNS3 Network Simulator
- Oracle VM VirtualBox

---

📂 Project File

https://drive.google.com/file/d/1mlkhLAarYJyHyTNzjELdpsSS7sZZXd11/view?usp=sharing

---

🏢 Real-World Use Case

This project simulates a small enterprise environment where:

- Employees communicate across departments
- Administrative systems are protected from unauthorized access
- Customer network is isolated from internal resources
- Internet access is controlled through an edge router

---

🎯 Learning Outcomes

- Understanding enterprise network architecture
- Practical implementation of routing and NAT
- Configuration of DHCP services
- Application of firewall security using ACL
- Importance of network segmentation

---

🎓 Conclusion

This project demonstrates how a secure and scalable enterprise network can be designed using industry-standard networking concepts.
It integrates routing, NAT, DHCP, and access control mechanisms to achieve both connectivity and security.

---

👨‍💻 Author

Ananthu K Santhosh
Bachelor of Computer Applications (BCA)
Marian College Kuttikkanam

---
