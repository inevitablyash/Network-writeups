# IPv4 Addressing & Subnetting

---

# Binary Math

Computers use binary (0s and 1s) for communication.

## Binary Place Values

| Binary | Decimal |
|---|---|
| 128 | 128 |
| 64 | 64 |
| 32 | 32 |
| 16 | 16 |
| 8 | 8 |
| 4 | 4 |
| 2 | 2 |
| 1 | 1 |

### Example
`11000000 = 192`

---

# IPv4 Addressing

- IPv4 uses 32-bit addresses  
- Written in dotted decimal format  

### Example
`192.168.1.1`

---

# Loopback Address

- Used to test the local system/network stack  

### Range
`127.0.0.0/8`

### Common Address
`127.0.0.1`

---

# Reserved Addresses

Certain IPv4 ranges are reserved for special purposes.

## Private Address Ranges
| Range | Class |
|---|---|
| 10.0.0.0 – 10.255.255.255 | A |
| 172.16.0.0 – 172.31.255.255 | B |
| 192.168.0.0 – 192.168.255.255 | C |

---

# VIP — Virtual IP Address

- Shared IP address used by multiple devices  
- Common in:
  - Load balancing  
  - High availability systems  

---

# DHCP — Dynamic Host Configuration Protocol

Automatically assigns:
- IP addresses  
- Subnet masks  
- Default gateways  
- DNS servers  

---

# Classful Subnetting

Older addressing method based on classes.

| Class | Range | Default Mask |
|---|---|---|
| A | 1–126 | 255.0.0.0 |
| B | 128–191 | 255.255.0.0 |
| C | 192–223 | 255.255.255.0 |

---

# Components of a Subnet

## Network Address
- Identifies the network itself  
- First address in the subnet  

---

## First Usable Address
- First assignable IP address for hosts  

---

## Broadcast Address
- Last address in the subnet  
- Used to send traffic to all devices in the subnet  

---

# IPv4 Subnet Mask

Separates:
- Network portion  
- Host portion  

### Example
`255.255.255.0 = /24`

---

# Classless Subnetting (CIDR)

CIDR = Classless Inter-Domain Routing

- Uses prefix length instead of address classes  

### Example
`192.168.1.0/24`

### Benefits
- Efficient IP usage  
- Flexible subnetting  

---

# Calculating IPv4 Subnets

Subnetting divides a network into smaller networks.

## Used For
- Better organization  
- Security  
- Efficient IP allocation  

---

# VLSM — Variable Length Subnet Mask

- Different subnet masks within the same network  
- Allows efficient address allocation  

### Example
- Large subnet for servers  
- Smaller subnet for printers  

---

# Magic Number Subnetting

Fast method for finding subnet ranges.

## Formula
`256 - subnet mask value`

### Example
Mask: `255.255.255.192`

`256 - 192 = 64`

Subnet increments:
- 0
- 64
- 128
- 192

---

# Seven Second Subnetting

Quick subnetting method used for exams and troubleshooting.

## Focus Areas
- Subnet ranges  
- Broadcast addresses  
- Usable hosts  
- CIDR notation  

---

# Quick Notes

- `/24` = 255.255.255.0  
- `/16` = 255.255.0.0  
- `/8` = 255.0.0.0  

- Network address = first address  
- Broadcast address = last address  
- Hosts exist between them
