🏢 Enterprise Office Network Simulation (GNS3)

A hands-on enterprise network simulation built using GNS3 and Cisco 7200 routers, designed to replicate a real-world office network environment.
This project demonstrates key networking concepts including routing, NAT, DHCP, network segmentation, and firewall implementation using ACLs.

---

📌 Project Overview

This project simulates a small enterprise infrastructure consisting of multiple internal departments and an external customer network.
The primary goal is to ensure:

- Secure communication between internal networks
- Controlled access to sensitive systems
- Reliable internet connectivity using NAT
- Efficient IP management using DHCP

The design follows a simplified core-edge architecture, commonly used in real enterprise networks.

---

🏗️ Network Architecture

The network is structured into different layers and functional components:

- Core Router (CORE-RTR)
  Handles internal routing between subnets and enforces firewall policies using ACLs

- Edge Router (EDGE-RTR)
  Acts as the gateway to external networks and provides internet access using NAT

- Core Switch (CORE-SW)
  Connects all internal office devices and enables LAN communication

- Office Network
  Includes departmental systems such as:
  
  - HR
  - IT
  - Finance

- Admin Network
  A highly secure subnet with restricted inbound access

- Customer Network
  A dynamic network where devices receive IP addresses using DHCP

---

🌐 IP Addressing Scheme

The network is divided into logical subnets for scalability and security.

| Network            | Subnet              | Description                         |
|------------------|--------------------|-------------------------------------|
| Core ↔ Edge Link | 10.0.0.0/24        | Router-to-router communication      |
| Office Network   | 192.168.10.0/24    | HR, IT, Finance departments         |
| Admin Network    | 192.168.20.0/24    | Secure admin systems                |
| Customer Network | 192.168.50.0/24    | DHCP-based external users           |

🚪 Default Gateways

- Office Network → 192.168.10.1
- Admin Network → 192.168.20.1
- Customer Network → 192.168.50.1

---

⚙️ Features Implemented

This project includes several core networking features:

- Static IP Addressing
  Used for office and admin devices to ensure consistent connectivity

- DHCP Configuration
  Automatically assigns IP addresses to customer devices

- NAT (Network Address Translation)
  Enables internal devices to access external networks (Internet simulation)

- Static Routing
  Configured between routers for inter-network communication

- Firewall using Extended ACL
  Controls traffic flow and enforces security policies

- Network Segmentation
  Separates networks to improve performance and security

---

🔐 Security (Firewall Implementation)

Firewall functionality is implemented using extended Access Control Lists (ACLs) on the Core Router (Cisco 7200).

🔒 Security Rules

- Admin network has full access to all networks
- Office and customer networks are restricted from accessing admin network
- Unauthorized traffic is blocked at the router level
- ACLs are applied on interfaces to control inbound traffic

This ensures that sensitive systems remain protected while maintaining necessary communication.

---

🧪 Verification & Testing

The network was tested to validate connectivity, security, and functionality.

✅ Internal Communication

All office devices successfully communicate with each other
Example: HR → IT → FIN

Screenshot: "network-working.png"

---

🚫 Firewall Block (Unauthorized Access)

Attempts to access the admin network from other networks are blocked
Displays: “Communication administratively prohibited”

Screenshots:

- "firewall-block-test.png"
- "firewall-block-hr.png"

---

✅ Firewall Allow (Admin Access)

Admin network can access all other networks without restriction

Screenshot: "firewall-allow-test.png"

---

🌍 Internet Access (NAT)

Internal devices can access external IP (e.g., 8.8.8.8) using NAT

Screenshot: "internet-access-NAT.png"

---

📡 DHCP Verification

Customer devices receive IP addresses dynamically

Screenshot: "dhcp-auto-assignment.png"

---

📁 Project Structure

enterprise-office-network-gns3/
│
├── configs/         # Router configuration files
├── project-file/    # GNS3 project download link
├── screenshots/     # Output verification images
└── README.md

---

🔗 GNS3 Project File

Due to size limitations, the project is hosted externally.

👉 Download here:
https://drive.google.com/file/d/1mlkhLAarYJyHyTNzjELdpsSS7sZZXd11/view?usp=sharing

---

🚀 How to Run the Project

1. Install GNS3 and VirtualBox
2. Import Cisco 7200 router image
3. Download the project file
4. Open it in GNS3
5. Start all devices
6. Verify connectivity using ping commands

---

🛠️ Technologies Used

- GNS3 (Network Simulation Tool)
- Cisco 7200 Router (Core, Edge, Firewall roles)
- VPCS (Virtual PC Simulator)
- VirtualBox

---

🎯 Learning Outcomes

Through this project, the following skills were developed:

- Enterprise network design fundamentals
- Routing and NAT configuration
- Firewall implementation using ACL
- DHCP setup and troubleshooting
- Network segmentation and security practices

---

👨‍💻 Author

Ananthu K Santhosh
BCA Student | Aspiring Full Stack Developer & Cybersecurity Enthusiast

---

⭐ Conclusion

This project demonstrates a practical implementation of an enterprise network with secure communication, controlled access, and internet connectivity.
It reflects hands-on experience with real-world networking concepts using GNS3 and Cisco devices.
