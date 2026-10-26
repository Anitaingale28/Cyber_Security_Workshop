# Networking Fundamentals


## Learning Objectives

By the end of this module, you will be able to:

- Explain IP addresses and ports.
- Differentiate TCP and UDP.
- Identify common network services.
- Explain open, closed, and filtered port states.

## IP Addresses

An IP address identifies a device on a network.

| Address | Meaning |
|---|---|
| `127.0.0.1` | IPv4 localhost address |
| `::1` | IPv6 localhost address |
| `192.168.x.x` | Common private network address |
| `10.x.x.x` | Common private network address |
| `172.16.x.x–172.31.x.x` | Private network address range |

In this course, `localhost` means your own computer. Scanning `localhost` examines services running on your local machine only.

## Ports

A port is a numbered communication endpoint used by services and applications.

| Port | Common Service | Protocol |
|---:|---|---|
| 20/21 | FTP | TCP |
| 22 | SSH | TCP |
| 23 | Telnet | TCP |
| 25 | SMTP | TCP |
| 53 | DNS | TCP/UDP |
| 80 | HTTP | TCP |
| 443 | HTTPS | TCP |
| 3389 | Remote Desktop | TCP |
| 8080 | Alternate HTTP | TCP |

## TCP vs UDP

| Feature | TCP | UDP |
|---|---|---|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable delivery | No delivery guarantee |
| Ordering | Ordered packets | No guaranteed ordering |
| Common uses | HTTP, HTTPS, SSH, FTP | DNS, streaming, gaming |

TCP establishes a connection before transferring data. UDP sends packets without establishing a connection first.

## Common Network Services

Common services include:

- **HTTP/HTTPS:** Web traffic.
- **SSH:** Secure remote administration.
- **FTP:** File transfer.
- **DNS:** Domain name resolution.
- **SMTP:** Email sending.
- **SMB:** Windows file and printer sharing.

## Port States

Nmap commonly reports ports as `open`, `closed`, `filtered`, `unfiltered`, `open|filtered`, or `closed|filtered`. [92]

| State | Meaning | Security Relevance |
|---|---|---|
| Open | A service is listening and accepting connections | Potential attack surface |
| Closed | The port is reachable, but no service is listening | Usually lower risk |
| Filtered | A firewall or filter prevents Nmap from determining the state | May indicate protection or blocked access |
| Unfiltered | Port is reachable, but state cannot be determined | Requires further analysis |

## Important Limitation

Your localhost scan results depend on the services actually running on your computer. If a service is not installed or running, its port may appear closed or may not appear at all. Do not assume that every port state can be demonstrated on localhost.

## Next Module

Continue to [Nmap Basics](../03-nmap-basics/README.md).
