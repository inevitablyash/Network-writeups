# Networking Functions

Networking functions define how data is accessed, transmitted, secured, and optimized across a network.

---

## 1. Access to Important Data
- Networks allow users to access critical data from centralized or distributed systems  
- Ensures availability of resources across multiple devices  

---

## 2. Remote Access
- Enables users to access systems from different locations  
- Common in enterprise environments (e.g., remote work, cloud access)  

---

## 3. Traffic Management
- Controls the flow of data across the network  
- Prevents congestion and ensures efficient data transmission  

---

## 4. Protocol Support
- Networks rely on protocols to define communication rules  
- Examples:
  - TCP/IP  
  - HTTP/HTTPS  
  - FTP  
- Ensures interoperability between devices  

---

## 5. Content Delivery Network (CDN)
- Speeds up content delivery by using distributed servers  
- Stores (caches) copies of data closer to users  
- Reduces latency and improves performance  

---

## 6. Virtual Private Network (VPN)
- Provides secure communication over an insecure network (e.g., Internet)  
- Uses encryption and decryption to protect data  
- Requires client/server VPN devices or software  

---

## 7. Quality of Service (QoS)
- Prioritizes important traffic over less critical data  
- Ensures high performance for applications like video calls and gaming  

### Traffic Shaping
- Controls bandwidth usage  
- Sends data based on priority levels  

---

## 8. Time To Live (TTL)
- A value in IP packets that limits how long data can travel  
- Prevents packets from circulating endlessly  

### How TTL Works
- Each router reduces the TTL value by 1  
- When TTL reaches 0, the packet is discarded  

### Purpose
- Prevents **routing loops**  
- Helps clear unnecessary traffic from the network  

---

## 9. Routing Loops
- Occur when routers continuously pass packets between each other  
- Example:
  - Router A sends to Router B  
  - Router B sends back to Router A  
- TTL stops this loop by eventually dropping the packet  

---

## 10. Default TTL Values
- **Linux / macOS:** 64 hops  
- **Windows:** 128 hops  

---

## Summary

Networking functions ensure:
- Secure communication  
- Efficient data delivery  
- Controlled traffic flow  
- Prevention of network issues like loops  

They are essential for maintaining performance, reliability, and security in modern networks.
