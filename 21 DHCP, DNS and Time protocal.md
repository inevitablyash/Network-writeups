# DHCP, DNS, IPv6, and Time Protocols Notes

> Beginner-friendly networking notes inspired by the teaching style of Professor Messer.

---

# DHCP (Dynamic Host Configuration Protocol)

DHCP automatically assigns IP configuration to devices on a network.

Instead of manually configuring:
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

DHCP does it automatically.

### Why DHCP is Important
Without DHCP:
- Every device must be configured manually
- Easy to make mistakes
- IP conflicts can happen

With DHCP:
- Faster
- Centralized management
- Easier scaling

### Common DHCP Ports
- UDP 67 → DHCP Server
- UDP 68 → DHCP Client

---

# BOOTP (Bootstrap Protocol)

BOOTP is an older protocol that came before DHCP.

It was mainly used for:
- Diskless workstations
- Automatically downloading boot files

### Difference Between BOOTP and DHCP

| BOOTP | DHCP |
|---|---|
| Static assignments | Dynamic assignments |
| Older protocol | Modern protocol |
| Limited features | Advanced configuration |

DHCP is basically an improved version of BOOTP.

---

# DORA Process

DORA is the 4-step DHCP communication process.

## 1. Discover
Client broadcasts:
> "Is there any DHCP server available?"

## 2. Offer
DHCP server replies:
> "I can give you this IP address."

## 3. Request
Client says:
> "I want to use that IP."

## 4. Acknowledge
Server confirms:
> "The IP is yours."

### Easy Memory Trick
DORA:
- Discover
- Offer
- Request
- Acknowledge

---

# DHCP Relay

A DHCP relay forwards DHCP requests between networks.

### Why Needed?
DHCP broadcasts normally do NOT cross routers.

If the DHCP server is on another network:
- Router acts as DHCP relay
- Forwards requests to server

### Example
- Client in VLAN 10
- DHCP server in VLAN 20
- Router relays DHCP packets

---

# Configuring DHCP

Basic DHCP configuration includes:

- IP range (scope/pool)
- Subnet mask
- Gateway
- DNS servers
- Lease time

### Example
```bash
192.168.1.100 - 192.168.1.200
```

---

# DHCP Scope Properties

A DHCP scope defines:
- Range of IP addresses
- Subnet mask
- Lease duration
- DNS settings
- Gateway

### Scope
A scope is the pool of addresses DHCP can assign.

---

# DHCP Assignment

DHCP can assign IP addresses in different ways.

## Dynamic Assignment
Temporary IP assignment.

## Automatic Assignment
Permanent assignment after first use.

## Manual Assignment
Admin manually maps MAC address to IP.

---

# Address Reservation

Reservation binds:
- A specific MAC address
- To a fixed IP address

### Why Use It?
Useful for:
- Printers
- Servers
- Cameras

Example:
```text
MAC → 192.168.1.50
```

---

# DHCP Lease

A lease is the amount of time a client can use an IP address.

### Example
- 8 hours
- 24 hours
- 7 days

When lease expires:
- Client renews IP

---

# IPv6

IPv6 is the next generation IP protocol.

### Why IPv6?
IPv4 addresses are running out.

### IPv6 Features
- 128-bit addresses
- Huge address space
- Better routing
- Built-in IPSec support

Example:
```text
2001:0db8:85a3::8a2e:0370:7334
```

---

# SLAAC (Stateless Address Autoconfiguration)

SLAAC allows devices to automatically generate IPv6 addresses.

### How It Works
Router advertises network information.
Client creates its own IPv6 address.

No DHCP server required.

---

# DAD (Duplicate Address Detection)

DAD checks whether an IPv6 address is already being used.

### Purpose
Prevents duplicate IPv6 addresses.

If duplicate found:
- Device does not use that address

---

# RS (Router Solicitation)

RS is sent by a client asking:
> "Any routers here?"

Used in IPv6 neighbor discovery.

---

# RA (Router Advertisement)

RA is sent by routers.

It tells clients:
- Network prefix
- Gateway information
- Whether SLAAC should be used

---

# DNS (Domain Name System)

DNS converts domain names into IP addresses.

### Example
```text
google.com → 142.250.x.x
```

Humans remember names.
Computers use IP addresses.

DNS acts like the internet's phonebook.

### Default Port
- UDP 53
- TCP 53

---

# gTLDs (Generic Top-Level Domains)

Common domain extensions.

Examples:
- .com
- .org
- .net
- .edu

---

# ccTLDs (Country Code Top-Level Domains)

Country-specific domains.

Examples:
- .in → India
- .uk → United Kingdom
- .jp → Japan

---

# Primary and Secondary DNS

## Primary DNS
Main DNS server.

## Secondary DNS
Backup DNS server.

Used for:
- Redundancy
- Fault tolerance

---

# FQDN (Fully Qualified Domain Name)

Complete domain name including hostname.

Example:
```text
server1.example.com
```

Breakdown:
- server1 → Hostname
- example → Domain
- com → TLD

---

# Local Name Resolution

Resolving names inside local network.

Methods:
- Hosts file
- DNS
- mDNS
- NetBIOS

---

# Lookup

DNS lookup means finding:
- IP from domain name
OR
- Domain name from IP

---

# Authoritative DNS Server

An authoritative server contains official DNS records.

It gives:
- Final answer
- Not cached response

---

# Recursive DNS Query

Client asks DNS server:
> "Find the answer for me."

Recursive resolver:
- Contacts other DNS servers
- Returns final result

---

# DNSSEC (DNS Security Extensions)

DNSSEC adds authentication to DNS.

### Purpose
Prevents:
- DNS spoofing
- DNS cache poisoning

Uses:
- Digital signatures

---

# DoT (DNS over TLS)

Encrypts DNS traffic using TLS.

### Port
- TCP 853

### Benefit
Protects DNS privacy.

---

# DoH (DNS over HTTPS)

DNS requests sent through HTTPS.

### Benefits
- Encrypted
- Harder to monitor
- Uses HTTPS traffic

---

# DNS Records

DNS records store information about domains.

---

# RR (Resource Record)

General term for DNS entries.

Every DNS record is a resource record.

---

# SOA (Start of Authority)

Contains important information about DNS zone.

Includes:
- Primary DNS server
- Admin email
- Serial number
- Refresh timers

---

# AAAA Record

Maps:
- Domain name
- To IPv6 address

Example:
```text
example.com → 2001:db8::1
```

---

# CNAME Record

Canonical Name record.

Creates alias for another domain.

Example:
```text
www.example.com → example.com
```

---

# MX Record

Mail Exchange record.

Specifies mail server for a domain.

Example:
```text
example.com → mail.example.com
```

---

# TXT Record

Stores text information in DNS.

Commonly used for:
- Verification
- Security policies

---

# DKIM (DomainKeys Identified Mail)

Email authentication method.

Adds digital signature to email.

### Purpose
Prevents:
- Email spoofing
- Fake emails

Uses TXT records in DNS.

---

# NS Record

Name Server record.

Specifies authoritative DNS servers for domain.

Example:
```text
ns1.example.com
```

---

# PTR Record

PTR record performs reverse DNS lookup.

Maps:
- IP address
- To domain name

### Reverse of AAAA/A Record

Example:
```text
192.168.1.10 → server.example.com
```

---

# NTP (Network Time Protocol)

Synchronizes time across devices.

### Why Important?
Accurate time needed for:
- Logs
- Authentication
- Security
- Kerberos
- Certificates

### Port
- UDP 123

---

# NTP Server

Provides accurate time to clients.

Usually syncs from:
- Atomic clocks
- GPS
- Internet time sources

---

# NTP Client

Receives time updates from NTP server.

Adjusts local clock automatically.

---

# NTP Client/Server Mode

Some devices:
- Receive time from upstream server
- Provide time to downstream devices

Acts as:
- Client and server simultaneously

---

# PTP (Precision Time Protocol)

Provides extremely accurate time synchronization.

More accurate than NTP.

### Common Uses
- Financial systems
- Telecom
- Industrial automation

### IEEE Standard
```text
IEEE 1588
```

---

# Quick Comparison Table

| Protocol | Purpose |
|---|---|
| DHCP | Assign IP addresses |
| DNS | Resolve names to IPs |
| NTP | Synchronize time |
| PTP | High-precision time sync |
| SLAAC | Auto IPv6 configuration |
| DNSSEC | Secure DNS responses |
| DoT | Encrypted DNS with TLS |
| DoH | Encrypted DNS over HTTPS |

---

# Easy Exam Tips

## DHCP
Remember:
```text
DORA
```

## DNS
Remember:
```text
Phonebook of the Internet
```

## IPv6
Remember:
```text
128-bit addressing
```

## NTP
Remember:
```text
UDP 123
```

## DNS Ports
Remember:
```text
TCP/UDP 53
```

## DoT
Remember:
```text
TCP 853
```

---
