# OSI Model (Open Systems Interconnection)

## Mnemonic
**All People Seem To Need Data Processing**

Each word represents a layer in the OSI model:
1. Application  
2. Presentation  
3. Session  
4. Transport  
5. Network  
6. Data Link  
7. Physical  

---

## Layer 1 — Physical Layer
- Handles transmission of raw bits (0s and 1s)
- Includes:
  - Signaling
  - Cabling
  - Connectors

---

## Layer 2 — Data Link Layer
- Basic network communication layer
- Uses Data Link Control protocols
- Responsible for switching
- Works with MAC addresses (Media Access Control)
- MAC address = unique identifier of a network interface card (NIC)

---

## Layer 3 — Network Layer
- Responsible for routing
- Uses Internet Protocol (IP)
- Handles packet forwarding between networks
- Performs fragmentation of packets

---

## Layer 4 — Transport Layer
- Ensures reliable data delivery
- Acts like a "post office" (handling parcels and letters)
- Protocols:
  - TCP (Transmission Control Protocol)
  - UDP (User Datagram Protocol)

---

## Layer 5 — Session Layer
- Manages communication sessions
- Controls:
  - Session start
  - Session maintenance
  - Session termination

---

## Layer 6 — Presentation Layer
- Responsible for data formatting and encryption
- Handles:
  - Character encoding
  - Data translation
  - Encryption (e.g., TLS)

---

## Layer 7 — Application Layer
- Closest to the end user
- Provides network services to applications
- Examples:
  - HTTP / HTTPS
  - Databases
  - Web browsers

---

## Example: How a Web Request Works

1. **Application Layer (Layer 7)**  
   The browser creates an HTTP request using HTTPS.

2. **Presentation Layer (Layer 6)**  
   The request is encrypted using TLS.

3. **Session Layer (Layer 5)**  
   A session is established and maintained with the server.

4. **Transport Layer (Layer 4)**  
   - Data is divided into segments  
   - Uses TCP for reliable delivery  
   - Source and destination ports are assigned (e.g., 52341 → 443)

5. **Network Layer (Layer 3)**  
   - Segments are converted into packets  
   - IP addresses are added (source and destination)  
   - Routing determines the best path across networks

6. **Data Link Layer (Layer 2)**  
   - Packets are framed into Ethernet frames  
   - MAC addresses are added  
   - Switches forward frames to the correct device

7. **Physical Layer (Layer 1)**  
   - Data is transmitted as electrical signals or radio waves  

---

## Reverse Process (On Server Side)

- Physical receives signals  
- Data Link removes frame  
- Network removes IP header  
- Transport reassembles segments  
- Session validates connection  
- Presentation decrypts data  
- Application processes the request  

---

## Summary

The OSI model standardizes how data travels from one system to another by dividing the process into 7 layers, each with a specific role.
