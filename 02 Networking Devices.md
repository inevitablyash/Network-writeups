# Networking Devices (Professor Messer - Network+)

Modern networks use multiple devices working together to connect systems, manage traffic, and provide security. 0

---

## 1. Router
- Connects different networks together
- Works at **Layer 3 (Network Layer)**
- Uses IP addresses to route traffic
- Determines the best path for data using routing tables

---

## 2. Switch
- Connects devices within the same network
- Works at **Layer 2 (Data Link Layer)**
- Uses MAC addresses to forward data
- Sends data only to the intended device (efficient)

---

## 3. Hub
- Basic networking device
- Works at **Layer 1 (Physical Layer)**
- Broadcasts data to all connected devices
- No intelligence → outdated and inefficient

---

## 4. Access Point (AP)
- Provides wireless connectivity (Wi-Fi)
- Connects wireless devices to a wired network
- Acts as a bridge between wireless and wired networks

---

## 5. Firewall
- Security device
- Filters incoming and outgoing traffic
- Uses rules to allow or block traffic
- Can operate at multiple OSI layers

---

## 6. Modem
- Converts digital signals to analog and vice versa
- Used for internet connectivity via ISP
- Example: DSL, Cable modem

---

## 7. Bridge
- Connects two network segments
- Works at **Layer 2**
- Filters traffic based on MAC addresses
- Reduces network congestion

---

## 8. Repeater
- Regenerates and amplifies signals
- Works at **Layer 1**
- Used to extend network distance

---

## 9. Gateway
- Connects networks using different protocols
- Acts as a translator between systems
- Operates at multiple layers (often Layer 7)

---

## 10. Load Balancer
- Distributes network traffic across multiple servers
- Improves performance and reliability
- Prevents server overload

---

## 11. Proxy Server
- Acts as an intermediary between client and internet
- Provides:
  - Security
  - Caching
  - Anonymity

---

## 12. IDS / IPS
### IDS (Intrusion Detection System)
- Monitors traffic
- Detects suspicious activity
- Sends alerts

### IPS (Intrusion Prevention System)
- Detects and actively blocks threats

---

## 13. VPN Concentrator
- Manages multiple VPN connections
- Provides secure remote access

---

## Quick Summary Table

| Device | Layer | Function |
|--------|------|---------|
| Router | L3 | Connect networks, routing |
| Switch | L2 | Connect devices, MAC-based forwarding |
| Hub | L1 | Broadcast data |
| Access Point | L2 | Wireless connectivity |
| Firewall | Multi | Security filtering |
| Modem | L1 | Signal conversion |
| Bridge | L2 | Segment networks |
| Repeater | L1 | Signal boosting |
| Gateway | Multi | Protocol translation |
| Load Balancer | L4/L7 | Traffic distribution |
| Proxy | L7 | Intermediary, caching |
| IDS/IPS | Multi | Threat detection/prevention |

---

## Key Idea

Networking devices operate at different OSI layers, each performing a specific role:
- Lower layers → physical transmission
- Middle layers → data handling and routing
- Upper layers → application and security services

These devices work together to ensure efficient, secure, and reliable communication across networks.
