# VLANs, Trunking & Switch Configuration

---

# VLAN — Virtual Local Area Network

A VLAN separates devices into different logical networks within the same physical switch.

## Benefits
- Improves security  
- Reduces broadcast traffic  
- Better network organization  

---

# Trunking

Trunk links carry traffic for multiple VLANs between switches.

## Features
- Uses VLAN tagging  
- Common protocol:
  - IEEE 802.1Q  

---

# Interface Configuration

Interfaces are network ports configured for communication.

## Common Configurations
- IP addressing  
- VLAN assignment  
- Speed and duplex settings  

---

# Basic Interface Settings

## Example Configurations
- Enable/disable interface  
- Assign VLAN  
- Configure IP address  
- Set interface description  

---

# Speed & Duplex

## Speed
Defines transmission speed.

### Examples
- 100 Mbps  
- 1 Gbps  
- 10 Gbps  

---

## Duplex

Controls communication direction.

### Half Duplex
- Send or receive at one time  

### Full Duplex
- Send and receive simultaneously  

---

# IP Address Management (IPAM)

Used to organize and manage IP addresses.

## Functions
- IP allocation  
- Address tracking  
- Preventing conflicts  

---

# Link Aggregation

Combines multiple physical links into one logical connection.

## Benefits
- Increased bandwidth  
- Redundancy  
- Improved reliability  

## Example Protocol
- LACP (Link Aggregation Control Protocol)  

---

# MTU — Maximum Transmission Unit

Maximum size of a packet/frame transmitted over a network.

## Standard Ethernet MTU
`1500 bytes`

## Jumbo Frames
- Larger MTU for high-performance networks  

---

# STP — Spanning Tree Protocol

Prevents switching loops in Layer 2 networks.

## Purpose
- Avoids broadcast storms  
- Creates loop-free topology  

---

# STP States

## Blocking
- Prevents loops  
- Does not forward frames  

---

## Listening
- Processes BPDU information  
- Does not forward data yet  

---

## Learning
- Learns MAC addresses  
- Still does not forward user traffic  

---

## Forwarding
- Fully operational state  
- Sends and receives frames  

---

## Disabled
- Interface is administratively down or inactive  

---

# Quick Notes

- VLANs separate networks logically  
- Trunks carry multiple VLANs  
- Full duplex allows simultaneous communication  
- Link aggregation combines bandwidth  
- MTU controls packet size  
- STP prevents Layer 2 loops
