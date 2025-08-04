# Small Office Network Simulation

This repository contains a Cisco Packet Tracer (`.pkt`) file that simulates a basic network infrastructure for a small office. The goal of this project is to create a functional and secure network that segments traffic between different departments and provides reliable internet connectivity.

---

## 🚀 Network Topology

The network consists of the following devices:

* **1 x Router:** Responsible for inter-VLAN routing and connecting to the internet (simulated ISP).
* **2 x Switches:** Provide network access for end devices and handle traffic segmentation using VLANs.
* **1 x Server:** Hosts an internal web application (HTTP).
* **End Devices:** Several PCs distributed across different departments.

*(Optional: You can take a screenshot of your Packet Tracer topology and add it here for a quick visual reference. To do this, upload the image to your GitHub repo and link it like this: `![Topology Screenshot](topology.png)`)*

---

## 📋 Features & Configuration

This network simulation includes the following configurations:

### VLAN Configuration
To segment traffic and improve security, the following VLANs have been configured:
* **VLAN 10:** Sales (`192.168.10.0/24`)
* **VLAN 20:** Engineering (`192.168.20.0/24`)
* **VLAN 99:** Management (`192.168.99.0/24`)
* **VLAN 100:** Server Farm (`192.168.100.0/24`)

### Routing
* **Router on a Stick:** The router is configured to route traffic between all VLANs.
* **DHCP Server:** The router acts as a DHCP server, dynamically assigning IP addresses to end devices in each VLAN.
* **Default Route:** A static default route is configured to simulate a connection to an ISP for internet access.

### Switch Configuration
* **Trunking:** The link between the two switches and the link from the main switch to the router are configured as `802.1Q` trunks to carry traffic for all VLANs.
* **Access Ports:** Switchports connected to end devices are configured as access ports and assigned to their respective VLANs.
* **Port Security:** Basic port security can be enabled on access ports to restrict access to known MAC addresses. _(Mention if you have configured this)_.

### Security
* **Standard Access Control Lists (ACLs):** (Optional) ACLs can be implemented to restrict inter-VLAN communication, for example, preventing the Sales department from accessing resources in the Engineering VLAN.
* **SSH Access:** Secure Shell (SSH) is configured for secure remote management of the router and switches. Telnet has been disabled.
* **Password Encryption:** All passwords on network devices are encrypted using the `service password-encryption` command.

---

## 💻 How to Use

1.  **Download the `.pkt` file** from this repository.
2.  **Open the file** using **Cisco Packet Tracer** (Version 8.2 or later is recommended).
3.  **Explore the topology** and inspect the running configurations on the router, switches, and other devices.

### Verification Tests
You can perform the following tests to verify network functionality:

* **Ping between PCs in the same VLAN:** Should be successful.
* **Ping between PCs in different VLANs:** Should be successful (traffic is routed by the router).
* **Ping the Server:** All devices should be able to ping the server at `192.168.100.10`.
* **Access the Web Server:** Open the web browser on any PC and navigate to `http://192.168.100.10`. You should see the default web page.
* **DHCP:** Check if PCs are receiving IP addresses correctly from their respective DHCP pools.

---
*This project serves as a practical exercise in fundamental networking concepts including VLANs, inter-VLAN routing, DHCP, and basic security practices.*