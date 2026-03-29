🏢 Enterprise Office Network Simulation (GNS3)

📌 Overview

This project simulates a real-world enterprise office network using GNS3.
It follows a core–edge architecture to provide secure communication, controlled access, and internet connectivity.

The implementation demonstrates key networking concepts such as routing, NAT, DHCP, and firewall security using ACLs.

---

🏗️ Network Architecture

The network is divided into multiple logical segments:

- Core Router (CORE-RTR): Handles internal routing and firewall policies
- Edge Router (EDGE-RTR): Provides internet access using NAT
- Core Switch (CORE-SW): Connects office devices
- Office Network: HR, IT, Finance departments
- Admin Network: Protected subnet with restricted access
- Customer Network: DHCP-enabled network for external users

---

🌐 IP Addressing Scheme

Network| Subnet| Description
Core ↔ Edge| 10.0.0.0/24| Router communication
Office Network| 192.168.10.0/24| HR, IT, FIN users
Admin Network| 192.168.20.0/24| Secure admin devices
Customer Network| 192.168.50.0/24| Guest access

---

⚙️ Features Implemented

- Static IP configuration for office devices
- DHCP configuration for customer network
- Network Address Translation (NAT) for internet access
- Static routing between networks
- Firewall implementation using extended ACL
- Network segmentation for security

---

🔐 Security Implementation

An extended Access Control List (ACL) is configured on the core router:

- Admin network has full access to all networks
- Office and customer networks cannot access the admin network
- Firewall rules are applied on multiple interfaces

---

🔄 Data Flow

- Office Users:
  PC → Switch → Core Router → Edge Router → Internet

- Customer Users:
  Device → Access Point → Switch → Edge Router → Internet

- Admin Access:
  Admin can communicate with all networks

---

🧪 Testing & Verification

Blocked Access (Unauthorized → Admin)

"Firewall Block Test" (screenshots/firewall-block-test.png)

---

Allowed Access (Admin → All Networks)

"Firewall Allow Test" (screenshots/firewall-allow-test.png)

---

Internet Connectivity (NAT)

"Internet Test" (screenshots/internet-working.png)

---

DHCP Allocation (Customer Network)

"DHCP Test" (screenshots/dhcp-customer.png)

---

🧰 Tools & Technologies

- Cisco 7200 Router (IOS)
- GNS3 Network Simulator
- Oracle VM VirtualBox

---

📂 Project File

The full GNS3 project file is available via Google Drive:

https://drive.google.com/file/d/1mlkhLAarYJyHyTNzjELdpsSS7sZZXd11/view?usp=sharing

Reference link also available in:
"project-files/project-link.txt"

---

🎯 Learning Outcomes

- Understanding of enterprise network design
- Implementation of routing and NAT
- Configuration of DHCP services
- Application of ACL-based firewall security
- Network segmentation concepts

---

🎓 Conclusion

This project demonstrates the design and implementation of a secure enterprise network using industry-standard networking concepts, integrating routing, NAT, DHCP, and access control mechanisms.

---

👨‍💻 Author

Ananthu K Santhosh\n
Bachelor of Computer Applications (BCA)\n
Marian College Kuttikkanam

---
