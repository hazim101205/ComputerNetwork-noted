# Cisco Packet Tracer & Networking Labs 🌐

## Lab 01: Basic LAN Topology & Cisco IOS CLI Hardening

- **Tools Used:** Cisco Packet Tracer 🛠️
- **Devices:** 2 PCs (`192.168.1.0/24`), 1 Cisco 2960 Switch (`SW0`) 💻
- **Objective:** Configure Layer 3 IP addressing, verify ICMP reachability, and secure the switch CLI[cite: 8].

### Configuration Summary
1. **Physical Connections & STP:** Connected PCs to `Switch0` using Straight-Through cables and observed Spanning Tree Protocol (STP) transition to Forwarding state (green).
2. **IP Configuration & Ping:** Assigned static IPs (`192.168.1.1` & `192.168.1.2`) and confirmed 0% packet loss via `ping`[cite: 8].
3. **Cisco IOS Switch Hardening:**
   ```text
   Switch> enable
   Switch# configure terminal
   Switch(config)# hostname SW0
   SW0(config)# enable secret cisco123
   SW0(config)# exit
   SW0# copy running-config startup-config