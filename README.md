# Day 1: Introduction to Cyber Security

> **Masterclass Module:** Cyber Security Fundamentals  
> **Duration:** 90–120 minutes  
> **Level:** Beginner  
> **Prerequisites:** Basic computer and internet usage  
> **Learning outcome:** By the end of this module, learners will be able to define cyber security, explain why it is essential, identify major cyber threats and attacker types, and describe common cyber-security career domains.

<!-- Dev Note: Begin with a short discussion: “What digital accounts, devices, or information would hurt you most if they were stolen?” Use answers to introduce assets, threats, and the need for security before presenting formal definitions. -->

## 1. What Is Cyber Security?

### 1.1 Definition

**Cyber security** is the practice of protecting computer systems, networks, applications, devices, data, and users from unauthorized access, misuse, disruption, modification, or destruction.

In simple terms:

> **Cyber security protects digital assets from digital threats.**

### 1.2 Core Objectives

Cyber security aims to preserve the **CIA Triad**:

| Principle | Meaning | Example |
|---|---|---|
| **Confidentiality** | Information is accessible only to authorized people | A student’s marks are visible only to the student and authorized staff |
| **Integrity** | Information remains accurate and unaltered | An attacker cannot change examination results or bank balances |
| **Availability** | Authorized users can access systems when needed | A college portal remains available during result publication |

```text
                +-----------------------+
                |       CIA TRIAD       |
                +-----------------------+
                          |
        +-----------------+-----------------+
        |                 |                 |
+---------------+ +---------------+ +---------------+
|Confidentiality| |   Integrity   | |  Availability |
+---------------+ +---------------+ +---------------+
| Keep data     | | Keep data     | | Keep systems  |
| private       | | accurate      | | accessible    |
+---------------+ +---------------+ +---------------+
```

### 1.3 Cyber Security vs Information Security

| Aspect | Information Security | Cyber Security |
|---|---|---|
| **Scope** | Protects information in all forms | Protects digital systems and electronic information |
| **Assets** | Paper records, verbal information, digital data, intellectual property | Computers, networks, servers, applications, cloud services, digital data |
| **Focus** | Confidentiality, integrity, and availability of information | Defense against digital attacks and cyber threats |
| **Example** | Locking a room containing confidential paper files | Blocking a hacker from accessing a database |

**Relationship:**

```text
+--------------------------------------+
|         INFORMATION SECURITY         |
|                                      |
|   +------------------------------+   |
|   |         CYBER SECURITY       |   |
|   +------------------------------+   |
+--------------------------------------+
```

> **Key point:** Every cyber-security incident affects information security, but not every information-security incident is a cyber incident.

<!-- Dev Note: Reinforce the difference with two quick examples: stolen paper files versus ransomware on a server. Ask learners to classify each as information security, cyber security, or both. -->

## 2. Importance and Need for Cyber Security

### 2.1 Why Cyber Security Matters

Modern life depends on digital systems. Individuals, businesses, hospitals, banks, governments, and critical infrastructure all store and process sensitive data online.

Cyber security is needed to:

- Protect personal data such as passwords, Aadhaar/PAN details, financial records, and medical information.
- Prevent financial fraud and identity theft.
- Maintain business continuity and protect organizational reputation.
- Protect intellectual property and trade secrets.
- Secure critical services such as electricity, transport, healthcare, and banking.
- Comply with privacy and data-protection laws.
- Maintain trust between users, customers, and organizations.

### 2.2 The Security Equation

A cyber risk exists when three conditions come together:

```text
   THREAT + VULNERABILITY + ASSET = RISK
```

| Term | Definition | Example |
|---|---|---|
| **Asset** | Anything valuable that needs protection | Customer database, laptop, source code |
| **Threat** | A potential cause of harm | Ransomware, hacker, insider misuse |
| **Vulnerability** | A weakness that can be exploited | Weak password, outdated software |
| **Risk** | The likelihood and impact of harm | Ransomware encrypts an unpatched server |
| **Control** | A safeguard that reduces risk | MFA, backups, patching, firewall |

### 2.3 Real-World Example: Colonial Pipeline Ransomware Attack

In May 2021, Colonial Pipeline, a major U.S. fuel pipeline operator, suffered a ransomware attack attributed to the DarkSide criminal group. The company shut down pipeline operations to contain the incident, causing fuel-delivery disruption and shortages in parts of the U.S. East Coast. The FBI confirmed DarkSide ransomware was responsible for the network compromise. [42][43]

```text
Attacker gains access
        |
        v
Ransomware encrypts systems / steals data
        |
        v
Operational disruption
        |
        v
Pipeline operations suspended
        |
        v
Fuel shortages and public impact
```

> **Lesson:** Cyber security is not only an IT problem. A cyber incident can affect fuel supply, hospitals, transportation, banking, and public safety.

<!-- Dev Note: Ask learners: “Which CIA principle was most affected in Colonial Pipeline?” Guide them to see that ransomware primarily affected availability, while data theft also created confidentiality risk. -->

### 2.4 Real-World Example: WannaCry Ransomware

In 2017, the WannaCry ransomware campaign infected tens of thousands of systems across more than 150 countries, including the United States, United Kingdom, Spain, Russia, Taiwan, France, and Japan. It exploited unpatched Windows systems and encrypted files, demanding ransom payments. [41]

```text
Unpatched system
        |
        v
WannaCry exploits vulnerability
        |
        v
Files encrypted
        |
        v
Ransom demand displayed
        |
        v
Business/healthcare disruption
```

> **Lesson:** Patching, backups, network segmentation, and user awareness are essential defenses.

<!-- Dev Note: Emphasize that WannaCry spread rapidly because many systems had not applied available security updates. Connect this to the practical habit of enabling automatic updates. -->

## 3. Types of Cyber Threats

### 3.1 Definition

A **cyber threat** is any potential event, actor, or condition that may harm digital systems, compromise data, or disrupt services.

### 3.2 Major Threat Categories

| Threat | Definition | Example |
|---|---|---|
| **Malware** | Malicious software designed to damage, disrupt, or gain unauthorized access | Virus, worm, Trojan, ransomware |
| **Phishing** | Fraudulent messages that trick users into revealing sensitive information | Fake bank email asking for an OTP |
| **Social engineering** | Psychological manipulation of people to bypass security controls | Attacker impersonates IT support |
| **Password attack** | Attempt to obtain or guess credentials | Brute-force or dictionary attack |
| **Denial-of-Service (DoS)** | Attack that makes a service unavailable | Website overwhelmed with traffic |
| **Data breach** | Unauthorized access to confidential data | Customer records leaked online |
| **Insider threat** | A trusted person misuses legitimate access | Employee copies customer data |
| **Man-in-the-Middle (MitM)** | Attacker intercepts communication between two parties | Attacker reads data on an insecure Wi-Fi network |

### 3.3 Malware Types

```text
                       MALWARE
                          |
     +---------+----------+----------+---------+
     |         |          |          |         |
   Virus     Worm      Trojan    Ransomware  Spyware
     |         |          |          |         |
 Attaches   Spreads   Disguised  Encrypts   Secretly
 to files  via network as useful  data and   monitors
           automatically software demands  users
                                  ransom
```

| Malware | How It Works | Realistic Scenario |
|---|---|---|
| **Virus** | Attaches to a file and spreads when the file runs | Infected document executes malicious code |
| **Worm** | Self-replicates across networks | Spreads through an unpatched network service |
| **Trojan** | Pretends to be legitimate software | Fake “free software” installer steals data |
| **Ransomware** | Encrypts files or blocks access and demands payment | Hospital cannot access patient records |
| **Spyware** | Secretly collects user activity | Records browsing activity or credentials |
| **Keylogger** | Records keystrokes | Captures usernames, passwords, and OTPs |

### 3.4 Phishing Flow

```text
Attacker sends fake email
        |
        v
User clicks malicious link
        |
        v
Fake login page opens
        |
        v
User enters username/password/OTP
        |
        v
Attacker captures credentials
        |
        v
Attacker accesses real account
```

> **Defense:** Verify sender addresses, avoid clicking unexpected links, never share OTPs, and use multi-factor authentication.

<!-- Dev Note: Run a “spot the phishing email” activity. Show a legitimate-looking message and ask learners to identify urgency, suspicious links, spelling/domain issues, and requests for sensitive information. -->

## 4. Types of Cyber Attackers

### 4.1 Definition

A **cyber attacker** or **threat actor** is an individual, group, or organization that attempts to exploit systems, people, or processes to gain unauthorized access, steal data, disrupt services, or cause harm.

### 4.2 Attacker Categories

| Attacker Type | Motivation | Typical Actions | Example |
|---|---|---|---|
| **Black-hat hacker** | Financial gain, data theft, disruption | Hacking, malware, ransomware | Criminal group deploying ransomware |
| **White-hat hacker** | Improve security with authorization | Ethical hacking, vulnerability testing | Penetration tester hired by a company |
| **Grey-hat hacker** | Curiosity, recognition, sometimes disclosure without permission | Finds and exposes vulnerabilities | Researcher reports a flaw publicly without authorization |
| **Script kiddie** | Fun, attention, experimentation | Uses existing tools without deep expertise | Runs a downloaded attack tool |
| **Insider threat** | Revenge, greed, negligence, ideology | Misuses authorized access | Employee leaks customer data |
| **Hacktivist** | Political or social cause | Website defacement, leaks, DDoS | Group attacks an organization to protest a policy |
| **State-sponsored actor** | Espionage, disruption, strategic advantage | Advanced persistent threats, espionage | Nation-state group targeting critical infrastructure |
| **Cybercriminal organization** | Profit | Ransomware, fraud, data theft | Ransomware-as-a-service group |

### 4.3 Attacker Motivation Model

```text
                 WHY DO ATTACKERS ATTACK?
                             |
     +-----------+-----------+-----------+-----------+
     |           |           |           |           |
   Money      Ideology    Espionage    Revenge     Curiosity
     |           |           |           |           |
 Ransomware  Hacktivism  State-sponsored Insider     Script
 Fraud       DDoS        APTs        threats       kiddies
 Data theft  Leaks       Theft       Sabotage     Experimentation
```

### 4.4 Real-World Example: Ransomware Criminals

The Colonial Pipeline incident illustrates financially motivated cybercriminals. DarkSide used ransomware to compromise Colonial Pipeline’s networks, and the company’s shutdown caused major fuel-delivery disruption. The FBI confirmed DarkSide’s responsibility for the compromise. [42][50]

> **Lesson:** Attackers are not always lone hackers. Modern attacks may involve organized criminal groups, affiliates, and ransomware-as-a-service ecosystems.

<!-- Dev Note: Avoid portraying all hackers as criminals. Clearly distinguish authorized ethical hackers from unauthorized attackers, and stress that permission and legal authorization are essential in security testing. -->

## 5. Cyber Security Career Domains

### 5.1 Overview

Cyber security careers are commonly grouped into **defensive**, **offensive**, **governance**, and **engineering** domains.

```text
                    CYBER SECURITY CAREERS
                              |
      +------------+----------+-----------+------------+
      |            |          |           |            |
 Defensive    Offensive   Governance   Engineering   Response &
 Security     Security    Risk &       & Cloud       Forensics
 (Blue Team)  (Red Team)  Compliance   Security
```

### 5.2 Career Domains

| Domain | Purpose | Common Roles | Key Skills |
|---|---|---|---|
| **Security Operations (SOC)** | Monitor, detect, and respond to security alerts | SOC Analyst, Threat Hunter | SIEM tools, log analysis, incident triage |
| **Incident Response & Forensics** | Investigate and recover from incidents | Incident Responder, Digital Forensics Analyst | Malware analysis, evidence handling, log forensics |
| **Offensive Security** | Find weaknesses before attackers exploit them | Penetration Tester, Red Teamer, Bug Bounty Hunter | Networking, Linux, web security, exploitation, reporting |
| **Governance, Risk & Compliance (GRC)** | Manage policies, risks, audits, and compliance | GRC Analyst, Risk Manager, Auditor | Risk assessment, frameworks, documentation, audits |
| **Security Engineering & Architecture** | Build secure systems and infrastructure | Security Engineer, Security Architect | Cloud, networking, identity, encryption, automation |
| **Application Security** | Secure software throughout development | AppSec Engineer, Secure Code Reviewer | Secure coding, OWASP Top 10, SAST/DAST |
| **Cloud Security** | Protect cloud platforms and workloads | Cloud Security Engineer | AWS/Azure/GCP, IAM, containers, cloud configuration |
| **Security Awareness & Training** | Reduce human-driven risk | Awareness Trainer, Security Educator | Communication, phishing simulations, policy training |

### 5.3 Blue Team vs Red Team

```text
        +---------------------+         +---------------------+
        |      RED TEAM       |         |      BLUE TEAM      |
        +---------------------+         +---------------------+
        | Offensive security  |         | Defensive security  |
        | Simulates attackers |  <--->  | Detects and stops   |
        | Finds weaknesses    |         | real attacks        |
        +---------------------+         +---------------------+
                     \                       /
                      \                     /
                       +-------------------+
                       |  PURPLE TEAMING   |
                       | Improves defenses |
                       +-------------------+
```

### 5.4 Beginner-Friendly Career Paths

| Starting Point | Suitable Roles | Why It Is Beginner-Friendly |
|---|---|---|
| **SOC Analyst** | Tier 1 SOC Analyst, Security Analyst | Focuses on monitoring alerts, investigating events, and escalation |
| **GRC Analyst** | Compliance Analyst, Risk Analyst | Uses documentation, policies, and risk-assessment skills |
| **IT Support to Security** | Helpdesk → Security Analyst | Builds practical knowledge of systems, users, and troubleshooting |
| **Developer to AppSec** | Secure Developer, AppSec Engineer | Leverages programming and software-development knowledge |

> **Career note:** SOC analysis, penetration testing, GRC, cloud security, and incident response are widely recognized cyber-security career paths. [48][55]

<!-- Dev Note: Ask learners to select one career path and identify one technical skill, one soft skill, and one certification or learning resource they would pursue next. Avoid implying that certifications alone guarantee employment. -->

## 6. Key Takeaways

- **Cyber security** protects digital systems, networks, data, and users from harm.
- The **CIA Triad**—Confidentiality, Integrity, and Availability—is the foundation of security.
- Cyber security is a specialized subset of the broader field of **information security**.
- Threats include malware, phishing, social engineering, password attacks, DoS attacks, insider threats, and data breaches.
- Attackers vary by motivation: criminals seek profit, hacktivists seek ideology, insiders misuse access, and state-sponsored actors pursue espionage or disruption.
- Career domains include SOC operations, incident response, offensive security, GRC, cloud security, application security, and security architecture.

## 7. Review Questions

1. **Explain the difference between cyber security and information security using one example of each.**

2. **A ransomware attack encrypts a hospital’s patient records and makes its systems unavailable. Identify which parts of the CIA Triad are affected and justify your answer.**

3. **Compare a white-hat hacker, black-hat hacker, and insider threat in terms of authorization, motivation, and potential impact.**

---

### References

- CISA, *Indicators Associated With WannaCry Ransomware* [41]  
- BBC News, *US fuel pipeline hackers ‘didn’t mean to create problems’* [42]  
- NPR, *What We Know About The Ransomware Attack On A Critical U.S. Pipeline* [43]  
- Pluralsight, *Cybersecurity career paths: 2026 job guide* [48]
