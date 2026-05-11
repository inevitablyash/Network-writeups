# Network Topologies & Architecture

---

# Network Topologies

## Star Topology (Hub-and-Spoke)
- All devices connect to a central device  
- Central device is usually a switch or hub  

### Advantages
- Easy troubleshooting  
- Easy expansion  

### Disadvantages
- Central device failure affects the network  

---

## Mesh Topology
- Devices connect to multiple other devices  

### Advantages
- High redundancy  
- Reliable communication  

### Disadvantages
- Expensive and complex  

---

## Hybrid Topology
- Combination of multiple topologies  

### Example
- Star + Mesh  

---

## Spine and Leaf Topology
Common in modern data centers.

### Spine Layer
- High-speed backbone switches  

### Leaf Layer
- Connect servers and devices  

### Features
- Low latency  
- High scalability  
- Efficient traffic handling  

---

## Point-to-Point Topology
- Direct connection between two devices  

### Example
- Router-to-router connection  

---

# Network Architecture

---

# 3-Tier Architecture

A traditional enterprise network design divided into three layers.

## 1. Core Layer
- Backbone of the network  
- Provides high-speed transport between devices and networks  

### Functions
- Fast forwarding  
- High availability  

---

## 2. Distribution Layer
- Connects access layer to the core layer  

### Functions
- Routing  
- Policy enforcement  
- Traffic filtering  
- VLAN management  

---

## 3. Access Layer
- Closest layer to end devices  

### Connected Devices
- PCs  
- Printers  
- IP phones  
- Wireless access points  

### Functions
- Device access  
- Network connectivity  

---

# Collapsed Core (2-Tier Architecture)

- Combines:
  - Core Layer  
  - Distribution Layer  

### Structure
- Core/Distribution Layer  
- Access Layer  

### Benefits
- Lower cost  
- Simpler management  
- Common in small and medium networks  

---

# Traffic Flow

## East-to-West Traffic
- Traffic moving inside the same network or data center  

### Example
- Server-to-server communication  

---

## North-to-South Traffic
- Traffic entering or leaving the network  

### Example
- Internet access  

---

# Quick Summary

| Layer | Purpose |
|---|---|
| Core | High-speed backbone |
| Distribution | Routing and policy control |
| Access | End-device connectivity |

---

| Traffic Type | Description |
|---|---|
| East-to-West | Internal network traffic |
| North-to-South | External network traffic |
