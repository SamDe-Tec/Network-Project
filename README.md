# TechNova LTD. Network Configuration in Cisco Packet Tracer

This project demonstrates the design, configuration, and testing of a departmental network for **TechNova LTD.** using Cisco Packet Tracer. It includes IP addressing through DHCP, router and switch configuration, connectivity testing, and Access Control Lists (ACLs) to restrict specific traffic while maintaining access to server services.

## Table of Contents

- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author

## Project Overview

The purpose of this project was to design and implement a functional network infrastructure for TechNova LTD., supporting three departments: **IT, Sales, and HR**.

The project focused on:

- Designing a departmental network topology.
- Configuring network devices and router interfaces.
- Assigning IP addresses to devices using DHCP.
- Setting default gateways and a static DNS server.
- Testing connectivity between departments using `ping`.
- Implementing ACLs to restrict ping traffic from Sales to IT while preserving access to server services and allowing other traffic.

## Network Topology

The network was designed in Cisco Packet Tracer to connect three departments through a central router and three access switches.

### Network Devices

- **1 Cisco 2911 Router** – Provides routing and applies traffic filtering rules.
- **3 Cisco 2960 Switches** – Connect devices within the IT, Sales, and HR departments.
- **6 PCs** – Two computers assigned to each department.
- **1 Server** – Located in the IT department to provide server services.
- **Copper straight-through cables** – Used to connect network devices.

### IP Addressing and Departments

The project documentation identifies the following departmental networks:

| Department | Network Address   | Devices            |
| ---------- | ----------------- | ------------------ |
| IT         | `192.168.10.0/24` | 2 PCs and 1 server |
| Sales      | `192.168.20.0/24` | 2 PCs              |
| HR         | `192.168.30.0/24` | 2 PCs              |

- **IP addressing:** Devices receive IP addresses through DHCP.
- **Default gateways:** Configured for the respective departments.
- **DNS:** A static DNS server is configured.
- **Network connectivity:** Departmental devices are connected through switches and the router.
  

## Tools and Technologies

- **Cisco Packet Tracer** – Network design, device configuration, and simulation.
- **Cisco 2911 Router** – Routing and ACL implementation.
- **Cisco 2960 Switches** – Departmental network connectivity.
- **Dynamic Host Configuration Protocol (DHCP)** – Automatic IP address assignment.
- **Access Control Lists (ACLs)** – Traffic filtering and access restrictions.
- **Internet Control Message Protocol (ICMP)** – Connectivity testing using `ping`.
- **HTTP** – Testing access to server services.
- **Domain Name System (DNS)** – Name resolution support through a configured static DNS server.
- **Copper straight-through cables** – Physical connections in the simulated topology.

## Configuration Steps

1. **Design the network topology**

   Created the TechNova LTD. network in Cisco Packet Tracer with one Cisco 2911 router, three Cisco 2960 switches, six PCs, and one server.
2. **Connect the network devices**

   Connected the PCs and server to their departmental switches and connected the switches to the router using copper straight-through cables.
3. **Configure IP addressing**

   Configured DHCP to assign IP addresses to the network devices and set the appropriate default gateway for each department.
4. **Configure router interfaces**

   Configured the router interfaces to support connectivity between the departmental networks.
5. **Configure DNS**

   Set a static DNS server address in the network configuration.
6. **Test initial network connectivity**

   Used `ping` to test communication between devices in the IT, Sales, and HR departments before implementing access restrictions.
7. **Configure the Access Control List**

   Applied an ACL on the router to prevent the Sales network (`192.168.20.0/24`) from pinging the IT network (`192.168.10.0/24`), while allowing access to server services and permitting other traffic.

   The intended policy was to restrict ICMP echo traffic from Sales to IT without blocking all communication between the two networks.
8. **Verify the ACL configuration**

   Run a ping test from a Sales PC to an IT PC. The test returned a destination host unreachable result, indicating that the intended restriction was taking effect.
9. **Test server service access**

   Tested HTTP access from the Sales department to verify that the ACL restriction did not prevent access to the relevant server services.

## Results and Findings

The project successfully demonstrated departmental network design, IP configuration, connectivity testing, and router-based traffic filtering.

### Key Results

- **Network topology:** Successfully created a network containing three departments, a router, three switches, six PCs, and one server.
- **IP configuration:** Configured DHCP for automatic IP address assignment and set departmental default gateways.
- **Initial connectivity:** Successfully tested communication between departmental devices before applying restrictions, including a successful ping from an HR PC to an IT PC.
- **Access control:** Applied an ACL intended to block ping traffic from Sales to IT.
- **ACL verification:** A ping test from Sales to IT returned a destination host unreachable result.
- **Server access:** Performed an HTTP access test to assess whether Sales could still access server services.

### Key Findings

- Basic connectivity testing helps confirm that the network is operational before security restrictions are introduced.
- ACLs can be used to enforce departmental communication policies at the router.
- ICMP restrictions can be implemented separately from permitted application traffic, provided the ACL rules are configured appropriately.
- Testing both restricted traffic and permitted services is important for validating network access-control policies.

**Conclusion:** The TechNova LTD. project demonstrates the practical application of network topology design, DHCP, routing, connectivity troubleshooting, and ACL-based traffic control in Cisco Packet Tracer.

## Author

**Samuel Letsu**

- **Project:** Project Work 2 – TechNova LTD. Network in Cisco Packet Tracer
- **Location:** Preston, United Kingdom
- **GitHub:** Add your GitHub profile URL here.
- **Email:** Add your professional email address here.
