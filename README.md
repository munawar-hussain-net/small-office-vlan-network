# Small Office VLAN Network

A hands-on Cisco Packet Tracer lab simulating a small office network with separate Sales and IT departments.

## 🎯 Objective

Build a small office network where:

- Sales and IT are separated using VLANs
- Both departments can communicate with each other
- Both departments can access a shared server
- Inter-VLAN routing is provided using Router-on-a-Stick

## 🖥️ Network Topology

![Network Topology](topology.png)

## 🔧 Technologies Used

- Cisco Packet Tracer
- VLANs
- 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- IPv4
- Static IP Addressing

## 🌐 IP Addressing

| Device | VLAN | IP Address | Gateway |
|---|---:|---|---|
| PC1 | 10 - Sales | 192.168.10.11/24 | 192.168.10.1 |
| PC2 | 10 - Sales | 192.168.10.12/24 | 192.168.10.1 |
| PC3 | 20 - IT | 192.168.20.11/24 | 192.168.20.1 |
| PC4 | 20 - IT | 192.168.20.12/24 | 192.168.20.1 |
| Server | 30 - Server | 192.168.30.10/24 | 192.168.30.1 |

## 🔀 VLAN Configuration

| VLAN | Name | Network |
|---:|---|---|
| 10 | Sales | 192.168.10.0/24 |
| 20 | IT | 192.168.20.0/24 |
| 30 | Server | 192.168.30.0/24 |

## 🚦 Router-on-a-Stick

The switch-to-router connection is configured as an 802.1Q trunk.

Router subinterfaces:

- G0/0.10 → 192.168.10.1
- G0/0.20 → 192.168.20.1
- G0/0.30 → 192.168.30.1

## 🧪 Connectivity Testing

- [ ] PC1 → PC2
- [] PC1 → PC3
- [] PC1 → PC4
- [] PC1 → Server
- [] PC1 → Router
- [] PC3 → Server

## 📚 What I Learned

- How to create and configure VLANs
- How to assign switch ports to VLANs
- How 802.1Q trunking works
- How Router-on-a-Stick provides inter-VLAN routing
- How to configure static IPv4 addresses
- How to test connectivity using ping
- How to troubleshoot basic network connectivity

## 📁 Project Files

- `small-office-vlan-network.pkt` — Cisco Packet Tracer topology
- `topology.png` — Network topology screenshot
