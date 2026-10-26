# Introduction to Network Scanning

**Duration:** 5 minutes

## Learning Objectives

By the end of this module, you will be able to:

- Define network scanning.
- Explain real-world cybersecurity applications.
- Differentiate host discovery from port scanning.
- Understand legal and ethical scanning boundaries.

## What Is Network Scanning?

Network scanning is the process of examining a network or system to discover information such as:

- Active devices
- Open ports
- Running services
- Service versions
- Operating system details
- Potential security weaknesses

Security professionals use scanning to understand what is exposed on a network before attackers can find and abuse it.

## Real-World Cybersecurity Applications

Network scanning is used for:

- **Asset discovery:** Identifying devices connected to a network.
- **Attack surface mapping:** Finding exposed services and ports.
- **Vulnerability assessment:** Identifying outdated or risky services.
- **Penetration testing:** Understanding targets within an authorized engagement.
- **Security monitoring:** Detecting unexpected services or devices.
- **System hardening:** Closing unnecessary ports and disabling unused services.

## Host Discovery vs Port Scanning

| Concept | Purpose | Example Question |
|---|---|---|
| Host discovery | Find live devices | “Which computers are online?” |
| Port scanning | Find accessible network ports | “Which ports are open on this device?” |
| Service detection | Identify software behind ports | “Is HTTP, SSH, or FTP running?” |
| Version detection | Identify software versions | “Which version of the service is running?” |

Host discovery answers whether a device is reachable. Port scanning answers which network doors are available on that device. Nmap performs host discovery by default and then scans ports on hosts determined to be online. [88]

## Legal and Ethical Considerations

Network scanning can generate traffic that may be logged, blocked, or considered unauthorized. Before scanning any system, ensure that:

- You own the system, or
- You have explicit written authorization, or
- You are working in an isolated lab environment.

Never scan:

- Public websites without permission
- Your employer’s network without authorization
- School, college, or university networks without permission
- Other people’s devices
- Cloud services outside your own authorized resources

Aggressive scanning can create excessive traffic, trigger intrusion detection systems, disrupt services, or violate laws and policies. Use safe, limited scans during learning.

## Key Takeaways

- Network scanning is a core cybersecurity skill.
- Host discovery finds devices; port scanning finds services.
- Scanning must always be authorized.
- Nmap is widely used for network discovery and security auditing. [89]

## Next Module

Continue to [Networking Fundamentals](../02-networking-fundamentals/README.md).
