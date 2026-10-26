# Prerequisites

Before starting this course, ensure your computer meets the following requirements.

## Required Knowledge

You do not need advanced cybersecurity knowledge. Basic familiarity with using a terminal or command prompt is helpful.

## Required Tools

| Tool | Purpose | Required? |
|---|---|---|
| Nmap | Network scanning | Required |
| Terminal, Command Prompt, or PowerShell | Run commands | Required |
| Wireshark | Optional packet analysis | Optional |
| VirtualBox | Optional isolated lab environment | Optional |
| Docker | Optional isolated lab environment | Optional |

## Operating System Support

The practical commands include versions for:

- Windows
- Linux
- macOS

## Install Nmap

### Windows

1. Download Nmap from the official website: <https://nmap.org/download.html>
2. Run the installer.
3. Enable the option to install command-line tools if available.
4. Open **Command Prompt** or **PowerShell**.
5. Verify installation:

```powershell
nmap --version
```

### Linux

#### Debian / Ubuntu

```bash
sudo apt update
sudo apt install nmap -y
nmap --version
```

#### Fedora

```bash
sudo dnf install nmap -y
nmap --version
```

#### Arch Linux

```bash
sudo pacman -S nmap
nmap --version
```

### macOS

Install Homebrew if needed, then run:

```bash
brew install nmap
nmap --version
```

## Install Wireshark — Optional

Download Wireshark from the official website: <https://www.wireshark.org/download.html>

Wireshark is optional in this course. It is useful for observing packets generated during a scan, but all required practical tasks can be completed using Nmap alone. The official Wireshark User’s Guide is available at <https://www.wireshark.org/docs/wsug_html_chunked/>. [106]

## Authorization Requirement

You may scan only:

- `localhost`
- Your own computer
- Virtual machines you own
- Isolated lab environments where you have explicit authorization

Do **not** scan public websites, cloud services, office networks, school networks, mobile devices, or third-party systems without explicit written permission.
