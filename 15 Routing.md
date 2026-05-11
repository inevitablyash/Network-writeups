# Routing & Network Address Translation

Routing is the process of forwarding packets between networks using routers.

---

# Static Routing

- Routes are manually configured by administrators  
- Does not automatically adapt to network changes  

## Advantages
- Simple  
- Predictable  
- Low resource usage  

## Disadvantages
- Not scalable  
- Manual updates required  

---

# Dynamic Routing

- Routers automatically learn and update routes  
- Uses routing protocols to exchange information  

## Advantages
- Automatic route updates  
- Better scalability  

## Disadvantages
- More CPU and memory usage  

---

# EIGRP — Enhanced Interior Gateway Routing Protocol

- Cisco proprietary routing protocol  
- Hybrid routing protocol  

## Features
- Fast convergence  
- Efficient routing updates  
- Uses metrics like bandwidth and delay  

---

# OSPF — Open Shortest Path First

- Link-state routing protocol  
- Open standard protocol  

## Features
- Uses shortest path calculation  
- Fast convergence  
- Common in enterprise networks  

---

# BGP — Border Gateway Protocol

- Exterior Gateway Protocol (EGP)  
- Used between autonomous systems on the Internet  

## Features
- Controls internet routing  
- Highly scalable  
- Policy-based routing  

---

# Three-Tier Routing Protocol Design

A common enterprise routing structure.

## Core Layer
- High-speed backbone routing  

---

## Distribution Layer
- Routing policies and traffic control  

---

## Access Layer
- End-device connectivity  

---

# Routing Table

A table stored on routers containing route information.

## Includes
- Destination network  
- Next hop  
- Interface  
- Metric  

---

# Prefix Length

Indicates how many bits belong to the network portion of an IP address.

## Example
`192.168.1.0/24`

- `/24` = 24 network bits  

---

# Administrative Distance (AD)

Measures the trustworthiness of a routing source.

## Lower Value = More Trusted

| Route Type | AD |
|---|---|
| Connected | 0 |
| Static | 1 |
| EIGRP | 90 |
| OSPF | 110 |
| RIP | 120 |

---

# Metrics

Used by routing protocols to determine the best path.

## Examples
- Bandwidth  
- Delay  
- Hop count  
- Cost  

---

# FHRP — First Hop Redundancy Protocol

Provides gateway redundancy.

## Purpose
- Prevents single point of failure for default gateways  

## Examples
- HSRP  
- VRRP  
- GLBP  

---

# NAT — Network Address Translation

Translates private IP addresses into public IP addresses.

## Purpose
- Conserves public IP addresses  
- Hides internal networks  

---

# Private IP Addresses

Used inside local networks and not routable on the internet.

| Class | Range |
|---|---|
| A | 10.0.0.0 – 10.255.255.255 |
| B | 172.16.0.0 – 172.31.255.255 |
| C | 192.168.0.0 – 192.168.255.255 |

---

# Public IP Addresses

- Globally unique  
- Routable on the internet  
- Assigned by ISPs or registries  

---

# NAT Process Example

```text
Private Device → Router (NAT) → Internet

192.168.1.10
        ↓
Translated to Public IP
        ↓
203.0.113.5
