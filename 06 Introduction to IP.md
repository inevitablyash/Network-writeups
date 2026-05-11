# Internet Protocol (IP) – Overview

The Internet Protocol (IP) is the core protocol responsible for moving data across networks. It ensures that data is addressed correctly and delivered to the right destination.

---

## Data Transfer Analogy

A simple way to understand networking:

- **Highway** → Physical or wireless network  
- **Truck (IP)** → Carries data across networks  
- **Boxes (TCP/UDP)** → Package and organize data  

---

## Encapsulation

Before data is sent, it is wrapped in layers:

1. **Application Data** → Original data  
2. **TCP/UDP Header** → Adds transport information  
3. **IP Header** → Adds source and destination IP addresses  
4. **Ethernet Frame** → Adds MAC addresses and final delivery structure  

---

## Transport Layer Protocols

### TCP (Transmission Control Protocol)
- Connection-oriented  
- Reliable data transfer  
- Uses:
  - Acknowledgments  
  - Packet sequencing  
  - Flow control  

---

### UDP (User Datagram Protocol)
- Connectionless  
- Faster but less reliable  
- No acknowledgments or session setup  
- Ideal for:
  - Streaming  
  - Real-time communication  

---

## Addressing and Ports

### IP Address
- Identifies the destination device on a network  

### Port Numbers
- Identify specific applications/services on a device  
- Example:
  - Port 80 → Web (HTTP)  
  - Port 143 → Email (IMAP)  

---

## Port Types

### Non-Ephemeral Ports (0–1023)
- Well-known ports  
- Used by standard services  

### Ephemeral Ports (1024–65535)
- Temporary ports  
- Assigned to clients during sessions  

---

## Summary

- IP handles addressing and delivery  
- TCP ensures reliability  
- UDP provides speed  
- Ports ensure data reaches the correct application  
- Encapsulation enables structured data transmission across networks
