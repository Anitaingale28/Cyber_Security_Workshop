# Day 2: Networking Fundamentals for Cyber Security

> **Masterclass Module:** Cyber Security Fundamentals   
> **Level:** Beginner  
> **Prerequisites:** Day 1 — Introduction to Cyber Security  
> **Learning outcome:** By the end of this module, learners will understand networks, the Internet, network devices, addressing, protocol models, common services, wireless security, and major network-based attacks.

<!-- Dev Note: This module is intentionally broad. Teach concepts first, then return to attack techniques in later labs. Avoid demonstrating attacks against networks or devices without explicit written authorization. -->

## 1. What Is a Network?

### 1.1 Definition

A **computer network** is a collection of two or more computing devices connected to exchange data, share resources, and communicate using agreed rules called **protocols**.

### 1.2 Key Components

| Component | Definition | Example |
|---|---|---|
| **Node** | Any device connected to a network | Laptop, phone, server, printer |
| **Link** | Physical or wireless connection between devices | Ethernet cable, Wi-Fi |
| **Protocol** | A set of rules for communication | TCP, HTTP, DNS |
| **Server** | A system that provides services | Web server, mail server |
| **Client** | A system that requests services | Browser, email app |
| **Bandwidth** | Maximum data-transfer capacity | 100 Mbps connection |

### 1.3 Simple Network Diagram

```text
   Laptop          Phone
      |               |
      +-------+-------+
              |
          Switch/Router
              |
          Internet
              |
          Web Server
```

<!-- Dev Note: Use a classroom analogy: a network is like students communicating in a shared language. Devices are students, cables/Wi-Fi are the classroom, and protocols are grammar rules. -->

## 2. What Is the Internet?

### 2.1 Definition

The **Internet** is a global network of interconnected networks that communicate using the TCP/IP protocol suite.

The Internet is not a single organization or single cable. It is a worldwide system of ISPs, data centers, routers, undersea cables, wireless networks, and connected devices.

### 2.2 Internet vs Network

| Feature | Network | Internet |
|---|---|---|
| **Scope** | Local or limited area | Global |
| **Ownership** | Often owned by a home, school, or organization | Made of many interconnected networks |
| **Example** | College Wi-Fi | Websites, email, cloud platforms |
| **Protocol** | May use TCP/IP or other protocols | Primarily TCP/IP |

## 3. History: ARPANET to the Internet

### 3.1 ARPANET

**ARPANET** was an early packet-switching network developed for the U.S. Advanced Research Projects Agency. It demonstrated that computers could communicate by dividing data into packets and sending them across multiple routes.

### 3.2 Evolution

```text
ARPANET
   |
   v
TCP/IP adopted as a common communication standard
   |
   v
Universities, research networks, and organizations connect
   |
   v
World Wide Web makes the Internet widely usable
   |
   v
Modern Internet: cloud, mobile, IoT, and global services
```

### 3.3 Why This Matters for Security

As networks became interconnected, security became essential. A vulnerability in one connected system can potentially affect users, organizations, and services across the Internet.

<!-- Dev Note: Explain packet switching with a simple example: a file is divided into parcels, each parcel may take a different route, and the receiver reassembles them. -->

## 4. Types of Networks

| Network Type | Full Form | Coverage | Example |
|---|---|---|---|
| **PAN** | Personal Area Network | A few meters | Bluetooth headset connected to a phone |
| **LAN** | Local Area Network | Home, office, campus | College computer lab |
| **MAN** | Metropolitan Area Network | City or large campus | City-wide government network |
| **WAN** | Wide Area Network | Large geographic area | Internet, bank branch network |
| **VPN** | Virtual Private Network | Secure tunnel over a public network | Employee securely accessing office resources |

### 4.1 VPN Concept

A **Virtual Private Network (VPN)** creates an encrypted tunnel between a user’s device and a VPN server, helping protect traffic from local network observers.

```text
User Device
     |
Encrypted VPN tunnel
     |
VPN Server
     |
Destination Website
```

> **Important:** A VPN improves privacy and can protect traffic on untrusted networks, but it does not make a user anonymous or protect against every threat.

## 5. Network Devices

| Device | Definition | Main Function |
|---|---|---|
| **NIC** | Network Interface Card | Connects a device to a network; has a MAC address |
| **Hub** | Basic Layer 1 device | Broadcasts data to all connected ports |
| **Switch** | Layer 2 device | Forwards frames using MAC addresses |
| **Router** | Layer 3 device | Routes packets between networks using IP addresses |
| **Modem** | Modulator-demodulator | Converts signals between digital devices and ISP media |
| **Repeater** | Signal booster | Regenerates weak signals |
| **Bridge** | Connects network segments | Filters traffic using MAC addresses |
| **Access Point** | Wireless connectivity device | Allows Wi-Fi devices to join a wired network |
| **Firewall** | Security control | Filters traffic based on defined rules |

### Switch vs Router

```text
+------------------+          +------------------+
|      SWITCH      |          |      ROUTER      |
+------------------+          +------------------+
| Works with MAC   |          | Works with IP    |
| addresses        |          | addresses        |
| Connects devices |          | Connects         |
| in one network   |          | different        |
|                  |          | networks         |
+------------------+          +------------------+
```

## 6. Network Topologies

A **network topology** is the physical or logical arrangement of devices in a network.

| Topology | Structure | Advantage | Disadvantage |
|---|---|---|---|
| **Bus** | All devices share one backbone cable | Simple and low cost | Cable failure can affect the network |
| **Star** | Devices connect to a central switch | Easy to manage | Central device is a single point of failure |
| **Ring** | Devices form a closed loop | Predictable data flow | One break can disrupt communication |
| **Mesh** | Devices connect to multiple other devices | High redundancy | Expensive and complex |
| **Tree** | Hierarchical arrangement of star networks | Scalable | Root/central failure affects branches |
| **Hybrid** | Combination of topologies | Flexible | More complex to design and troubleshoot |

```text
STAR TOPOLOGY

        PC
         |
PC --- Switch --- PC
         |
        PC
```

```text
MESH TOPOLOGY

PC A ----------- PC B
 | \           / |
 |   \       /   |
 |     \   /     |
PC D ----------- PC C
```

## 7. IP and MAC Addressing

### 7.1 IP Address

An **IP address** is a logical address that identifies a device on a network and helps route packets to the correct destination.

### 7.2 MAC Address

A **MAC address** is a unique hardware identifier assigned to a network interface card. It operates mainly at Layer 2 of the OSI model.

```text
Application data
       |
IP address: Where should the packet go?
       |
MAC address: Which device on this local network receives it?
```

| Address | Layer | Purpose | Example |
|---|---|---|---|
| **MAC address** | Layer 2 | Identifies a physical network interface | `AA:BB:CC:DD:EE:FF` |
| **IPv4 address** | Layer 3 | Identifies a device on an IP network | `192.168.1.10` |
| **IPv6 address** | Layer 3 | Identifies a device using a larger address space | `2001:db8::1` |

## 8. IPv4 and IPv6

### 8.1 IPv4

**IPv4** uses 32-bit addresses, providing approximately 4.3 billion possible addresses.

```text
192.168.1.10
```

### 8.2 IPv6

**IPv6** uses 128-bit addresses and was developed to overcome IPv4 address exhaustion.

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

| Feature | IPv4 | IPv6 |
|---|---|---|
| Address size | 32 bits | 128 bits |
| Notation | Decimal | Hexadecimal |
| Example | `192.168.1.1` | `2001:db8::1` |
| Address space | About 4.3 billion | Extremely large |
| Security | Security added through supporting protocols | IPsec support designed into the protocol suite |

## 9. Public, Private, Static, and Dynamic IPs

| Type | Definition | Example |
|---|---|---|
| **Public IP** | Routable address visible on the Internet | Assigned by an ISP |
| **Private IP** | Address used inside a local network | `192.168.1.10`, `10.0.0.5`, `172.16.0.2` |
| **Static IP** | Manually fixed address that does not change | Server address |
| **Dynamic IP** | Temporarily assigned address, commonly through DHCP | Home laptop address |

### Private IP Ranges

```text
10.0.0.0    - 10.255.255.255
172.16.0.0  - 172.31.255.255
192.168.0.0 - 192.168.255.255
```

## 10. Subnet Mask, Subnetting, and Default Gateway

### 10.1 Subnet Mask

A **subnet mask** separates the network portion of an IP address from the host portion.

```text
IP address:      192.168.1.10
Subnet mask:     255.255.255.0
Network:         192.168.1.0
Host range:      192.168.1.1 - 192.168.1.254
Broadcast:       192.168.1.255
```

### 10.2 Subnetting

**Subnetting** divides a larger network into smaller logical networks to improve organization, reduce broadcast traffic, and support security segmentation.

```text
192.168.1.0/24
        |
        +--> 192.168.1.0/25  Students
        |
        +--> 192.168.1.128/25 Staff
```

### 10.3 Default Gateway

A **default gateway** is the router address used when a device needs to communicate outside its local network.

```text
Laptop: 192.168.1.10
        |
Default gateway: 192.168.1.1
        |
Internet
```

<!-- Dev Note: Have learners run `ipconfig` on Windows or `ip addr` / `ifconfig` on Linux and identify their IP address, subnet mask, and default gateway. -->

## 11. OSI Model

The **OSI model** is a seven-layer conceptual framework that describes how data moves through a network.

| Layer | Name | Function | Examples |
|---|---|---|---|
| 7 | Application | User-facing network services | HTTP, HTTPS, DNS, SMTP |
| 6 | Presentation | Data format, encryption, compression | SSL/TLS, JPEG |
| 5 | Session | Manages sessions | Session establishment and termination |
| 4 | Transport | End-to-end delivery | TCP, UDP |
| 3 | Network | Logical addressing and routing | IP, ICMP |
| 2 | Data Link | MAC addressing and frames | Ethernet, ARP |
| 1 | Physical | Bits and physical transmission | Cables, radio signals |

```text
7 Application  -> Data
6 Presentation -> Data
5 Session      -> Data
4 Transport    -> Segments
3 Network      -> Packets
2 Data Link    -> Frames
1 Physical     -> Bits
```

## 12. TCP/IP Model

The **TCP/IP model** is a practical four-layer model used by the Internet.

| TCP/IP Layer | Corresponding OSI Layers | Examples |
|---|---|---|
| Application | Application, Presentation, Session | HTTP, DNS, SMTP |
| Transport | Transport | TCP, UDP |
| Internet | Network | IP, ICMP |
| Network Access | Data Link, Physical | Ethernet, Wi-Fi |

```text
OSI MODEL                    TCP/IP MODEL
7 Application  \
6 Presentation  >  Application
5 Session       /
4 Transport        Transport
3 Network          Internet
2 Data Link     \
1 Physical       >  Network Access
```

## 13. TCP and UDP

### 13.1 TCP

**Transmission Control Protocol (TCP)** is a connection-oriented transport protocol that provides reliable, ordered, and error-checked delivery of data.

### 13.2 UDP

**User Datagram Protocol (UDP)** is a connectionless transport protocol that provides fast delivery without guaranteed ordering or delivery.

| Feature | TCP | UDP |
|---|---|---|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable | Unreliable |
| Ordering | Ordered | Not ordered |
| Speed | Slower | Faster |
| Use case | Web browsing, email, file transfer | Video streaming, gaming, DNS queries |

### 13.3 TCP Three-Way Handshake

```text
Client                         Server
   |                              |
   |----------- SYN ------------->|   Step 1
   |                              |
   |<------ SYN + ACK ------------|   Step 2
   |                              |
   |----------- ACK ------------->|   Step 3
   |                              |
   |      Connection established  |
```

> **Security relevance:** Attackers may exploit connection mechanisms through SYN floods, where many incomplete connection requests exhaust server resources.

## 14. Ports and Sockets

### 14.1 Port Number

A **port number** identifies a specific application or service on a device.

```text
IP address identifies the device.
Port number identifies the service.
```

### 14.2 Socket

A **socket** is the combination of an IP address and a port number used for communication.

```text
Socket = IP address + Port number
Example: 192.168.1.10:443
```

### 14.3 Common Ports

| Port | Protocol/Service | Purpose |
|---|---|---|
| 20/21 | FTP | File transfer |
| 22 | SSH | Secure remote administration |
| 23 | Telnet | Unencrypted remote administration |
| 25 | SMTP | Sending email |
| 53 | DNS | Domain-name resolution |
| 67/68 | DHCP | Automatic IP configuration |
| 80 | HTTP | Unencrypted web traffic |
| 110 | POP3 | Email retrieval |
| 143 | IMAP | Email retrieval and synchronization |
| 443 | HTTPS | Encrypted web traffic |
| 161 | SNMP | Network management |

## 15. Important Network Protocols

| Protocol | Full Form | Purpose |
|---|---|---|
| **HTTP** | HyperText Transfer Protocol | Transfers web content |
| **HTTPS** | HTTP Secure | Transfers web content over TLS encryption |
| **DNS** | Domain Name System | Converts domain names into IP addresses |
| **DHCP** | Dynamic Host Configuration Protocol | Assigns IP configuration automatically |
| **FTP** | File Transfer Protocol | Transfers files |
| **SMTP** | Simple Mail Transfer Protocol | Sends email |
| **POP3** | Post Office Protocol version 3 | Downloads email |
| **IMAP** | Internet Message Access Protocol | Synchronizes email across devices |
| **Telnet** | Teletype Network | Remote terminal access, unencrypted |
| **SSH** | Secure Shell | Encrypted remote terminal access |
| **ARP** | Address Resolution Protocol | Maps IP addresses to MAC addresses |
| **ICMP** | Internet Control Message Protocol | Reports network errors; used by `ping` |
| **SNMP** | Simple Network Management Protocol | Monitors and manages network devices |

### DNS Resolution Flow

```text
User types example.com
        |
        v
DNS resolver checks cache
        |
        v
DNS lookup performed
        |
        v
IP address returned
        |
        v
Browser connects to web server
```

## 16. Wi-Fi, Bluetooth, and Mobile Networks

### 16.1 Wi-Fi

**Wi-Fi** is a wireless local-area networking technology that allows devices to connect using radio frequencies.

### 16.2 Bluetooth

**Bluetooth** is a short-range wireless technology used for personal-area networking, such as connecting headphones, keyboards, and wearables.

### 16.3 Mobile Network Generations

| Generation | Main Improvement | Example Use |
|---|---|---|
| **2G** | Digital voice and basic SMS | Calls and text messages |
| **3G** | Mobile internet and faster data | Early mobile browsing |
| **4G** | High-speed mobile broadband | HD video and mobile apps |
| **5G** | Very low latency and high capacity | IoT, smart cities, industrial automation |

## 17. Wireless Security

| Standard | Security Level | Status |
|---|---|---|
| **WEP** | Wired Equivalent Privacy | Obsolete and insecure |
| **WPA** | Wi-Fi Protected Access | Improved over WEP but outdated |
| **WPA2** | Stronger encryption using AES | Common, but must be correctly configured |
| **WPA3** | Modern Wi-Fi security standard | Preferred where supported |

### Real-World Example: KRACK Attack

In 2017, researchers disclosed **KRACK**—Key Reinstallation Attacks—against WPA2. An attacker within Wi-Fi range could exploit weaknesses in the four-way handshake to reinstall an already-used key, potentially enabling packet decryption, injection, TCP connection hijacking, and HTTP content injection. [56][57]

```text
Victim joins WPA2 network
        |
        v
Attacker manipulates handshake
        |
        v
Key reuse / reinstallation
        |
        v
Potential traffic decryption or injection
```

> **Defense:** Keep devices patched, use WPA3 where available, use strong passphrases, and avoid trusting open public Wi-Fi.

<!-- Dev Note: Clarify that WPA2 remains widely used and can be secure when patched and configured properly. KRACK showed why timely updates matter. -->

## 18. Network Security Controls

| Control | Definition | Purpose |
|---|---|---|
| **Firewall** | Device or software that filters traffic using rules | Allows or blocks network traffic |
| **IDS** | Intrusion Detection System | Detects and alerts on suspicious activity |
| **IPS** | Intrusion Prevention System | Detects and actively blocks suspicious activity |
| **Proxy server** | Intermediary between client and server | Caching, filtering, privacy, access control |
| **Tor** | Onion-routing network | Routes traffic through multiple relays for privacy |

### Firewall vs IDS vs IPS

```text
Internet
   |
   v
Firewall -----> Allows/blocks traffic
   |
   v
IDS ---------> Detects and alerts
   |
   v
IPS ---------> Detects and blocks
   |
   v
Internal Network
```

## 19. Encryption, SSL/TLS, and Secure Communication

### 19.1 Encryption and Decryption

**Encryption** converts readable data, called plaintext, into unreadable ciphertext. **Decryption** converts ciphertext back into plaintext using the appropriate key.

```text
Plaintext --> Encryption --> Ciphertext --> Transmission
Ciphertext --> Decryption --> Plaintext --> Receiver
```

### 19.2 SSL/TLS

**SSL/TLS** protocols provide encryption, integrity, and authentication for communications. Modern secure web traffic uses **HTTPS**, which is HTTP protected by TLS.

```text
Browser                         Web Server
   |                                |
   |-------- TLS handshake -------->|
   |                                |
   |<------ Certificate exchange ---|
   |                                |
   |------- Encrypted HTTP data --->|
```

> **Important:** HTTPS protects data in transit, but it does not guarantee that a website is trustworthy.

## 20. Network Attacks

### 20.1 Packet Sniffing

**Packet sniffing** is capturing and analyzing network traffic. It can be legitimate for administrators but dangerous on unencrypted networks.

```text
Attacker captures packets
        |
        v
Reads unencrypted credentials or data
```

**Defense:** Use HTTPS, SSH, VPNs, and encrypted protocols.

### 20.2 Network Reconnaissance

**Network reconnaissance** is the process of gathering information about a target network, such as live hosts, open ports, services, and operating systems.

```text
Identify targets
      |
      v
Scan for live hosts
      |
      v
Identify open ports and services
      |
      v
Look for exploitable weaknesses
```

> **Legal warning:** Scanning systems without authorization may be illegal and unethical. Practice only in approved lab environments.

### 20.3 Man-in-the-Middle Attack

A **man-in-the-middle (MitM)** attack occurs when an attacker secretly intercepts or alters communication between two parties.

```text
Client <---- Attacker ----> Server
            (intercepts)
```

**Defense:** HTTPS, certificate validation, VPNs, and secure Wi-Fi.

### 20.4 ARP Spoofing

**ARP spoofing** is an attack in which an attacker sends false ARP messages to associate their MAC address with another device’s IP address, often the default gateway.

```text
Normal:
Victim --> Gateway

ARP spoofing:
Victim --> Attacker --> Gateway
```

**Defense:** Dynamic ARP inspection, port security, network monitoring, and encrypted traffic.

### 20.5 DNS Poisoning

**DNS poisoning** or **DNS cache poisoning** is an attack that inserts false DNS records into a resolver’s cache, causing users to be redirected to attacker-controlled systems.

In 2008, researcher Dan Kaminsky disclosed a DNS cache-poisoning flaw related to the DNS protocol’s query-ID mechanism. The vulnerability could allow spoofed DNS data to redirect users to malicious sites; DNSSEC is considered the complete solution to this class of attack. [58][60]

```text
User requests bank.com
        |
        v
Poisoned DNS cache responds
        |
        v
User is sent to attacker-controlled IP
```

**Defense:** DNSSEC, randomized source ports and transaction IDs, trusted resolvers, and monitoring.

### 20.6 Session Hijacking

**Session hijacking** is an attack in which an attacker obtains or predicts a valid session token and impersonates an authenticated user.

```text
User logs in
     |
Session cookie/token issued
     |
Attacker steals token
     |
Attacker reuses token
     |
Unauthorized access
```

**Defense:** HTTPS, secure and HTTP-only cookies, short session lifetimes, session rotation, and MFA.

### 20.7 Denial-of-Service Attack

A **Denial-of-Service (DoS)** attack attempts to make a service unavailable by exhausting resources. A **Distributed DoS (DDoS)** attack uses many compromised devices.

### Real-World Example: Mirai and Dyn

In October 2016, a DDoS attack against DNS provider Dyn used traffic from devices infected by the Mirai botnet. Mirai targeted IoT devices with weak or default credentials and recruited them into a botnet. The attack disrupted Internet access and affected major online services. [62][64]

```text
Compromised IoT devices
        |
        v
Mirai botnet
        |
        v
Massive DNS query flood
        |
        v
DNS provider overwhelmed
        |
        v
Websites and services unreachable
```

> **Defense:** Change default passwords, update IoT firmware, disable unnecessary services, and use DDoS mitigation services.

### 20.8 Firewall Evasion

**Firewall evasion** is the attempt to bypass firewall rules using techniques such as unusual packet flags, fragmentation, tunneling, or allowed protocols.

> **Ethical note:** Firewall-evasion techniques should only be studied in authorized labs, capture-the-flag environments, or with written permission.

## 21. Key Takeaways

- A network connects devices to share data and resources; the Internet is a global network of networks.
- IP addresses provide logical addressing, while MAC addresses identify physical network interfaces.
- The OSI model has seven layers; the TCP/IP model has four layers.
- TCP is reliable and connection-oriented, while UDP is fast and connectionless.
- Common services include DNS, DHCP, HTTP/HTTPS, email protocols, SSH, ARP, ICMP, and SNMP.
- Network security controls include firewalls, IDS/IPS, VPNs, encryption, and secure wireless standards.
- Major network attacks include sniffing, MitM, ARP spoofing, DNS poisoning, session hijacking, and DDoS.

## 22. Review Questions

1. **Explain the difference between a MAC address and an IP address. Which one is used by a switch and which one is used by a router?**

2. **Compare TCP and UDP. Why would a video-streaming application often use UDP, while an online-banking website uses TCP over HTTPS?**

3. **A user connects to free public Wi-Fi and visits an HTTP website. Explain how a man-in-the-middle attack could compromise confidentiality and list three defenses.**

---

### References

- CERT-EU, *KRACK — Key Reinstallation Attacks: Breaking WPA2* [56][57]  
- Internet Systems Consortium, *CVE-2008-1447: DNS Cache Poisoning Issue (“Kaminsky bug”)* [58]  
- NLnet Labs, *DNS Cache Poisoning Vulnerability (2008)* [60]  
- bit-tech, *Dyn confirms Mirai behind Friday’s DDoS attack* [62]  
- Threatpost, *Mirai-Fueled IoT Botnet Behind DDoS Attacks on DNS Providers* [64]
