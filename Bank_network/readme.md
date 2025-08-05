# Bank Network Infrastructure

## Project Overview

This project is a simulation of a secure and efficient network infrastructure for a banking institution, created using Cisco Packet Tracer. The primary goal is to design and implement a network that ensures the confidentiality, integrity, and availability of sensitive financial data, while also providing reliable connectivity for various banking operations.

## Network Topology

The network is designed with a hierarchical model, consisting of a central headquarters (HQ) and two branch offices. This topology provides scalability, simplified management, and improved performance.

*(Optional: You can insert a screenshot of your Packet Tracer topology here.)*

## Features

* **VLAN Segmentation:** The network is segmented into multiple Virtual LANs (VLANs) to isolate different departments (e.g., Tellers, Loan Officers, Administration) and enhance security.
* **Inter-VLAN Routing:** A multi-layer switch at the HQ and routers at the branch offices are configured to enable communication between different VLANs.
* **Redundancy and High Availability:** The network design incorporates redundant links and protocols like EtherChannel to ensure high availability and minimize downtime.
* **Secure Remote Access:** A Virtual Private Network (VPN) is configured to provide secure remote access for employees working from home or traveling.
* **Access Control Lists (ACLs):** Standard and extended ACLs are implemented to filter traffic and enforce security policies, restricting unauthorized access to critical resources.
* **Dynamic Host Configuration Protocol (DHCP):** A DHCP server is configured to automatically assign IP addresses to client devices, simplifying network administration.
* **Network Address Translation (NAT):** NAT is configured on the edge router to translate private IP addresses to a public IP address, enabling secure internet access.

## Configuration

All device configurations, including routers, switches, and servers, are included in the Packet Tracer file (`Bank_network.pkt`).

## How to Use

To explore the project, you will need to have Cisco Packet Tracer installed.

1.  **Download:** Download the `Bank_network.pkt` file.
2.  **Open:** Open the file in Cisco Packet Tracer.
3.  **Simulate:** You can then interact with the network, test connectivity using `ping`, and view device configurations.

## Contributor

- [Your Name]

Feel free to connect with me on [LinkedIn] https://www.linkedin.com/in/jamsithrilwan/.