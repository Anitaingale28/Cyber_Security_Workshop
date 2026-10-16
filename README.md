# Day 4: Information Security Fundamentals

> **Masterclass Module:** Cyber Security Fundamentals  
> **Level:** Beginner   
> **Learning outcome:** By the end of this module, learners will understand information security, the CIA Triad, information classification, access-control models, authentication, data protection, security policies, and backup/recovery.

<!-- Dev Note: Begin with a relatable example such as WhatsApp encryption or online banking. Ask learners what information they would not want strangers to access, change, or lose. -->

## 1. What Is Information Security?

### 1.1 Definition

**Information security** is the practice of protecting information and information systems from unauthorized access, use, disclosure, modification, disruption, or destruction.

Information may exist in many forms:

- Digital data: files, databases, emails, cloud storage.
- Physical data: paper files, printed reports, ID cards.
- Verbal information: private conversations, meetings.
- Intellectual property: research, source code, designs, business plans.

### 1.2 Why Information Security Is Needed

Without information security:

- There would be no privacy.
- Personal and financial data could be misused.
- Banking systems could collapse.
- Identity theft would become common.
- People would not trust the Internet.
- Hospitals and critical systems could be manipulated.
- Government systems could become unstable.
- Smart and autonomous devices could be remotely misused.

### 1.3 Example: WhatsApp Encryption

When one person sends a WhatsApp message to another, only the sender and receiver should be able to read it. Even WhatsApp should not be able to read the message content. This protects **confidentiality** and builds trust in digital communication.

## 2. CIA Triad

The **CIA Triad** is the foundation of information security.

| Principle | Meaning | Online Banking Example |
|---|---|---|
| **Confidentiality** | Only authorized people can access information | Account number, password, balance, and transactions remain private |
| **Integrity** | Information remains accurate and unaltered | Transaction amount cannot be changed during transfer |
| **Availability** | Authorized users can access systems when needed | Banking app and servers remain available for transactions |

```text
                CIA TRIAD
                    |
    +---------------+---------------+
    |               |               |
Confidentiality  Integrity    Availability
    |               |               |
Keep data       Keep data      Keep systems
private         accurate       accessible
```

### 2.1 Confidentiality

Confidentiality prevents unauthorized people from viewing sensitive information.

**Controls:**

- Passwords.
- OTPs.
- Encryption.
- Access control.
- Authentication.

### 2.2 Integrity

Integrity ensures that data is not changed by unauthorized users.

**Example:** If ₹500 is transferred, neither the sender’s nor receiver’s balance should be altered incorrectly during the transaction.

**Controls:**

- Hashing.
- Digital signatures.
- Version control.
- Audit logs.

### 2.3 Availability

Availability ensures that authorized users can access information and services whenever required.

**Example:** A banking website should be available when a user wants to transfer money or check their balance.

**Controls:**

- Backup servers.
- Redundant systems.
- Disaster-recovery planning.
- DDoS protection.

## 3. Information Classification

**Information classification** is the process of organizing information based on its sensitivity and the impact caused if it is disclosed.

| Classification | Meaning | Examples |
|---|---|---|
| **Public** | Can be shared with everyone | Website content, advertisements, public videos |
| **Private / Internal** | For internal organization use only | Internal emails, company policies |
| **Confidential** | Sensitive data that can cause harm if leaked | Examination papers, business plans |
| **Restricted / Highly Confidential** | Extremely sensitive information with strict access rules | Defense data, medical records, national-security data |

```text
Public
  |
  v
Private / Internal
  |
  v
Confidential
  |
  v
Restricted / Highly Confidential
```

> **Key point:** As sensitivity increases, access restrictions and security controls must also increase.

## 4. Access Control Models

**Access control** determines who can access which information and what actions they can perform.

### 4.1 Discretionary Access Control — DAC

In **DAC**, the owner of the data decides who can access it and what permissions they receive.

**Example:** A Google Drive file owner can allow another person to view or edit the file.

```text
File Owner
    |
Decides access
    |
Viewer / Editor / No access
```

**Advantage:** Flexible.  
**Limitation:** Security depends on the owner’s decisions.

### 4.2 Mandatory Access Control — MAC

In **MAC**, access is controlled by strict system-enforced rules. Users cannot freely share access.

**Example:** Military or government systems may require a specific security clearance to access classified files.

**Advantage:** Very strict and secure.  
**Limitation:** Less flexible.

### 4.3 Role-Based Access Control — RBAC

In **RBAC**, access is assigned based on a user’s role in an organization.

**Example:** A founder may access company-wide data, while an intern may access only project-related information.

```text
User -> Role -> Permissions
Intern -> Intern Role -> Limited access
Manager -> Manager Role -> Higher access
```

**Advantage:** Easy to manage in organizations.  
**Limitation:** Role explosion can occur if too many roles are created.

### 4.4 Attribute-Based Access Control — ABAC

In **ABAC**, access depends on attributes such as location, time, department, device, or job title.

**Example:** An employee can access office data only during office hours and only from the office network.

```text
Access Decision =
User attributes
+ Resource attributes
+ Environment conditions
+ Security policy
```

**Advantage:** Highly flexible and granular.  
**Limitation:** More complex to design and manage.

## 5. Authentication Methods

**Authentication** is the process of verifying a user’s identity before granting access.

| Method | Meaning | Examples |
|---|---|---|
| **Knowledge-based** | Something you know | Password, PIN, security question |
| **Possession-based** | Something you have | OTP, ATM card, smartphone, authenticator app |
| **Biometric-based** | Something you are | Fingerprint, face recognition, voice recognition |
| **Location-based** | Based on location or network | Office Wi-Fi access, geo-restricted login |
| **Multi-factor authentication** | Combination of two or more factors | Password + OTP |

```text
Authentication Factors

Something you know  -> Password, PIN
Something you have  -> OTP, ATM card, phone
Something you are   -> Fingerprint, face, voice
```

### 5.1 Multi-Factor Authentication — MFA

**MFA** uses two or more different authentication factors.

**Example:**

```text
Password + OTP + Fingerprint
```

Using a password and PIN together is **not** true MFA because both belong to the same factor: something you know.

## 6. Data Protection Techniques

**Data protection** means applying controls to keep information secure throughout its lifecycle.

| Technique | Purpose | Example |
|---|---|---|
| **Encryption** | Converts readable data into unreadable ciphertext | Encrypting bank details |
| **Access control** | Limits who can access data | Role-based permissions |
| **Authentication** | Verifies user identity | Password and OTP |
| **Backup** | Creates copies of data | Cloud or external-drive backup |
| **Data masking** | Hides sensitive data | Showing only last four digits of a card |
| **Data loss prevention** | Prevents unauthorized sharing | Blocking sensitive file uploads |
| **Hashing** | Verifies data integrity | Password hashing |

### 6.1 Encryption and Decryption

```text
Plaintext --> Encryption --> Ciphertext
Ciphertext --> Decryption --> Plaintext
```

- **Plaintext:** Original readable data.
- **Ciphertext:** Encrypted unreadable data.
- **Key:** Secret value used for encryption or decryption.

## 7. Security Policies

A **security policy** is a documented set of rules that defines how an organization protects its information, systems, and users.

### 7.1 Types of Security Policies

| Policy | Purpose |
|---|---|
| **Acceptable Use Policy** | Defines proper use of organizational systems |
| **Password Policy** | Defines password length, complexity, and change rules |
| **Access Control Policy** | Defines who can access what data |
| **Data Classification Policy** | Defines sensitivity levels of information |
| **Backup Policy** | Defines backup frequency and recovery rules |
| **Incident Response Policy** | Defines how to respond to security incidents |
| **Remote Work Policy** | Defines secure work-from-home practices |

### 7.2 Example: Password Policy

- Minimum 12 characters.
- Use uppercase, lowercase, numbers, and symbols.
- Do not reuse old passwords.
- Do not share passwords.
- Enable MFA wherever possible.

## 8. Data Backup and Recovery

**Data backup** is the process of creating copies of important data so that it can be restored after deletion, corruption, hardware failure, ransomware, or disaster.

**Data recovery** is the process of restoring data from a backup after an incident.

### 8.1 3-2-1 Backup Rule

The **3-2-1 backup rule** recommends:

- Keep **3** copies of important data.
- Store the copies on **2** different types of storage media.
- Keep **1** copy off-site.

```text
Original Data
      |
      +--> Copy 1: External hard drive
      |
      +--> Copy 2: Cloud storage
      |
      +--> Copy 3: Off-site backup
```

### 8.2 Backup Types

| Backup Type | What It Copies | Speed | Storage Needed |
|---|---|---|---|
| **Full backup** | All selected data | Slowest | Highest |
| **Incremental backup** | Only data changed since the last backup | Fast | Low |
| **Differential backup** | Data changed since the last full backup | Medium | Medium |

### 8.3 Backup Best Practices

- Automate backups.
- Encrypt backups.
- Keep at least one offline backup.
- Store one backup off-site.
- Test restoration regularly.
- Protect backup credentials.
- Maintain backup logs.

> **Important:** A backup is useful only if it can be successfully restored.

## 9. Quick Revision

```text
Information Security
      |
      +--> CIA Triad
      |       |-- Confidentiality
      |       |-- Integrity
      |       |-- Availability
      |
      +--> Information Classification
      |       |-- Public
      |       |-- Private/Internal
      |       |-- Confidential
      |       |-- Restricted
      |
      +--> Access Control Models
      |       |-- DAC
      |       |-- MAC
      |       |-- RBAC
      |       |-- ABAC
      |
      +--> Authentication
      |       |-- Knowledge
      |       |-- Possession
      |       |-- Biometric
      |       |-- MFA
      |
      +--> Data Protection
      |       |-- Encryption
      |       |-- Backup
      |       |-- Masking
      |
      +--> Security Policies
      |
      +--> Backup and Recovery
```

## 10. Revision

- **Information security:** Protection of information in all forms from unauthorized access, modification, disclosure, disruption, or destruction.
- **Confidentiality:** Ensuring information is accessible only to authorized users.
- **Integrity:** Ensuring information remains accurate, complete, and unaltered.
- **Availability:** Ensuring authorized users can access information and systems when needed.
- **DAC:** Access model where the data owner decides permissions.
- **MAC:** Access model where strict system-enforced rules control access.
- **RBAC:** Access model where permissions are assigned based on user roles.
- **ABAC:** Access model where permissions depend on user, resource, and environment attributes.
- **Authentication:** Process of verifying a user’s identity.
- **MFA:** Use of two or more different authentication factors.
- **Encryption:** Converting plaintext into ciphertext to protect confidentiality.
- **Backup:** Copy of data kept for recovery after loss or attack.
- **Recovery:** Process of restoring data and systems after an incident.

