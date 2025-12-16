# CCNA – Network Security Fundamentals (Module 16)

Quick-reference notes for NetAcad CCNA – **Module 16: Network Security Fundamentals**.  
Focus is on understanding **threats, attacks, and basic mitigations**, plus how to
**harden Cisco devices** with passwords, SSH, and secure configs.

I use this repo to revise:

- The difference between **threats**, **vulnerabilities**, and **attacks**.
- Common **malware types** and classic **recon / access / DoS** attacks.
- The idea of **defense-in-depth** and layered security.
- Core mitigation tools: **backups, patching, AAA, firewalls, endpoint security**.
- How to **secure Cisco IOS devices**: passwords, SSH, disabling unused services.
- Typical CCNA-style security scenarios and wording for **basic security best practices**.

---

## Table of Contents

- [Module 16 Overview](#module-16-overview)  
- [Module Map](#module-map)  

- [16.0 Introduction](#160-introduction)  
  - [16.0.1 Why should I take this module?](#1601-why-should-i-take-this-module)  
  - [16.0.2 What will I learn to do in this module?](#1602-what-will-i-learn-to-do-in-this-module)  

- [16.1 Security Threats and Vulnerabilities](#161-security-threats-and-vulnerabilities)  
  - [16.1.1 Types of Threats](#1611-types-of-threats)  
  - [16.1.2 Types of Vulnerabilities](#1612-types-of-vulnerabilities)  
  - [16.1.3 Physical Security](#1613-physical-security)  
  - [16.1.4 Check Your Understanding – Security Threats and Vulnerabilities](#1614-check-your-understanding--security-threats-and-vulnerabilities)  

- [16.2 Network Attacks](#162-network-attacks)  
  - [16.2.1 Types of Malware](#1621-types-of-malware)  
  - [16.2.2 Reconnaissance Attacks](#1622-reconnaissance-attacks)  
  - [16.2.3 Access Attacks](#1623-access-attacks)  
  - [16.2.4 Denial of Service Attacks](#1624-denial-of-service-attacks)  
  - [16.2.5 Check Your Understanding – Network Attacks](#1625-check-your-understanding--network-attacks)  
  - [16.2.6 Lab – Research Network Security Threats](#1626-lab--research-network-security-threats)  

- [16.3 Network Attack Mitigations](#163-network-attack-mitigations)  
  - [16.3.1 The Defense-in-Depth Approach](#1631-the-defense-in-depth-approach)  
  - [16.3.2 Keep Backups](#1632-keep-backups)  
  - [16.3.3 Upgrade, Update, and Patch](#1633-upgrade-update-and-patch)  
  - [16.3.4 Authentication, Authorization, and Accounting](#1634-authentication-authorization-and-accounting)  
  - [16.3.5 Firewalls](#1635-firewalls)  
  - [16.3.6 Types of Firewalls](#1636-types-of-firewalls)  
  - [16.3.7 Endpoint Security](#1637-endpoint-security)  
  - [16.3.8 Check Your Understanding – Network Attack Mitigation](#1638-check-your-understanding--network-attack-mitigation)  

- [16.4 Device Security](#164-device-security)  
  - [16.4.1 Cisco AutoSecure](#1641-cisco-autosecure)  
  - [16.4.2 Passwords](#1642-passwords)  
  - [16.4.3 Additional Password Security](#1643-additional-password-security)  
  - [16.4.4 Enable SSH](#1644-enable-ssh)  
  - [16.4.5 Disable Unused Services](#1645-disable-unused-services)  
  - [16.4.6 Packet Tracer – Configure Secure Passwords and SSH](#1646-packet-tracer--configure-secure-passwords-and-ssh)  
  - [16.4.7 Lab – Configure Network Devices with SSH](#1647-lab--configure-network-devices-with-ssh)  

- [16.5 Module Practice and Quiz](#165-module-practice-and-quiz)  
  - [16.5.1 Packet Tracer – Secure Network Devices](#1651-packet-tracer--secure-network-devices)  
  - [16.5.2 Lab – Secure Network Devices](#1652-lab--secure-network-devices)  
  - [16.5.3 What did I learn in this module?](#1653-what-did-i-learn-in-this-module)  
  - [16.5.4 Module Quiz – Network Security Fundamentals](#1654-module-quiz--network-security-fundamentals)  

---

## Module 16 Overview

> **Goal:** Recognise common security threats and attacks, understand basic
> mitigation strategies (defense-in-depth), and apply **foundational hardening**
> to Cisco devices (passwords, SSH, disabling unused services).

---

## Module Map

| Topic                           | Focus                                                                 |
|---------------------------------|-----------------------------------------------------------------------|
| 16.1 Security Threats & Vulnerabilities | Threat types, vulnerabilities, physical security basics         |
| 16.2 Network Attacks            | Malware, recon, access, DoS attacks, examples                        |
| 16.3 Network Attack Mitigations | Defense-in-depth, backups, patching, AAA, firewalls, endpoint sec.   |
| 16.4 Device Security            | Cisco AutoSecure, strong passwords, SSH, disabling unused services   |
| 16.5 Practice and Quiz          | Hands-on PT + labs, summary, and module quiz                         |

---


# CCNA ITN — Module 16: Network Security Fundamentals (Study Guide)

Quick-reference + ultra-detailed study notes for **Cisco NetAcad CCNA: Introduction to Networks (ITN)**  
**Module 16 — Network Security Fundamentals**

> **Status:** This file includes everything from the screenshots you shared so far (**16.0.1 → 16.1.2**).  
> Next sections (16.1.3+, 16.1.4 questions, etc.) will be added when you drop the next prints.

---

## Table of Contents

- [Module 16 Overview](#module-16-overview)
- [Module Map](#module-map)

- [16.0 Introduction](#160-introduction)
  - [16.0.1 Why should I take this module?](#1601-why-should-i-take-this-module)
  - [16.0.2 What will I learn to do in this module?](#1602-what-will-i-learn-to-do-in-this-module)

- [16.1 Security Threats and Vulnerabilities](#161-security-threats-and-vulnerabilities)
  - [16.1.1 Types of Threats](#1611-types-of-threats)
  - [16.1.2 Types of Vulnerabilities](#1612-types-of-vulnerabilities)

---

## Module 16 Overview

**Big idea:** You can build a network that “works” and still be unsafe. Security is the layer that keeps the network **available**, protects **data**, and stops **unauthorized access**.

This module focuses on:
- Why networks must be secured (not just connected).
- Common ways attackers get in (weaknesses + bad configs + weak policies).
- The kinds of damage that happen once access is gained (theft, manipulation, outages).

---

## Module Map

| Topic | What you’re expected to understand |
|---|---|
| **Security Threats and Vulnerabilities** | Why basic security controls are necessary on network devices |
| **Network Attacks** | Identify security vulnerabilities |
| **Network Attack Mitigation** | Identify general mitigation techniques |
| **Device Security** | Configure network devices using device-hardening features to reduce threats |

---

# 16.0 Introduction

## 16.0.1 Why should I take this module?

Think of a network like a house.

- Building the network **without securing it** is like leaving **every door and window wide open** and then going away.
- When security is missing, anyone could:
  - get inside,
  - steal things,
  - break things,
  - or simply create chaos.

And just like on the news, **any network can be broken into** if it’s not protected.

As a network admin (or the person responsible for the network), your job is to make it **hard** for threat actors to successfully gain access.

What this module gives you:
- A high-level overview of **network attack types**
- Practical ideas for reducing the chance that attacks succeed
- **Packet Tracer activities** so you can practice basic network-security techniques

If you already have a network and it’s “working” but not as secure as it could be, this module is the place to start.

---

## 16.0.2 What will I learn to do in this module?

**Module Title:** Network Security Fundamentals  
**Module Objective:** Configure switches and routers with device-hardening features to improve security.

| Topic Title | Topic Objective (what you should be able to do) |
|---|---|
| **Security Threats and Vulnerabilities** | Explain why basic security measures are necessary on network devices. |
| **Network Attacks** | Identify security vulnerabilities. |
| **Network Attack Mitigation** | Identify general mitigation techniques. |
| **Device Security** | Configure network devices with device-hardening features to mitigate security threats. |

---

# 16.1 Security Threats and Vulnerabilities

## 16.1.1 Types of Threats

Modern life depends on wired and wireless networks.
- People and organizations rely on computers + networks for everyday work.
- If an unauthorized person breaks in, the impact can be expensive:
  - **network downtime / outages**
  - **lost work**
  - **lost time and money**
  - **damage** to systems
  - **theft** of important information or assets

### How intruders typically get access
Attackers can get into networks through:
- **software vulnerabilities**
- **hardware-based attacks**
- **guessing usernames and passwords**

Intruders who get access by **changing software** or **taking advantage of software weaknesses** are called **threat actors**.

Once a threat actor gets access, four common “outcomes” (threat types) may happen.

---

### 1) Information theft
**Meaning:** Breaking into a computer to obtain **confidential** information.

What happens next:
- That information can be **used** or **sold**
- A common example is stealing **proprietary company info**, such as **research and development data**

---

### 2) Data loss and manipulation
**Meaning:** Breaking into a computer system to **destroy** data or **change** data records.

Examples:
- **Data loss:** sending a virus that **reformats a hard drive**
- **Data manipulation:** breaking into a records system to **edit values**, like changing the **price of an item**

---

### 3) Identity theft
**Meaning:** A type of information theft where **personal information** is stolen to **take over someone’s identity**.

With stolen identity info, a threat actor may be able to:
- get legal documents,
- apply for credit,
- or make unauthorized online purchases.

Identity theft is a growing issue and can cost **billions of dollars per year**.

---

### 4) Disruption of service
**Meaning:** Preventing legitimate users from accessing services they are allowed to use.

Examples include **denial of service (DoS)** attacks that target:
- servers,
- network devices,
- or network communication links.

---

## 16.1.2 Types of Vulnerabilities

### What “vulnerability” means
A **vulnerability** is the degree of weakness in a network or device.

Important context:
- Some weakness exists naturally in many devices:
  - routers, switches,
  - desktops, servers,
  - even security devices.
- In many real incidents, the attacked targets are often **endpoints**, like servers and desktop PCs.

### The three main sources of weaknesses
There are **three primary categories** of vulnerabilities:
1. **Technological vulnerabilities**
2. **Configuration vulnerabilities**
3. **Security policy vulnerabilities**

Any of these can leave a network/device exposed to many attack types, including:
- **malicious code attacks**
- **network attacks**

---

### Technological vulnerabilities (built-in / structural weaknesses)

| Vulnerability | What it means / examples |
|---|---|
| **TCP/IP protocol weakness** | Some widely used protocols were not designed with strong security in mind. Examples listed: **HTTP**, **FTP**, and **ICMP** are inherently insecure. Also listed: **SNMP** and **SMTP** relate to the insecure structure on which TCP was designed. |
| **Operating system weakness** | Every OS has security issues that must be addressed. Examples listed: **UNIX**, **Linux**, **Mac OS**, **Mac OS X**, **Windows Server 2012**, **Windows 7**, **Windows 8**. These issues are documented in **CERT** archives (Computer Emergency Response Team) at **http://www.cert.org**. |
| **Network equipment weakness** | Networking devices (routers, firewalls, switches) can have weaknesses that must be recognized and protected against. Examples listed include weaknesses involving **password protection**, **lack of authentication**, **routing protocols**, and **firewall holes**. |

---

### Configuration vulnerabilities (weaknesses caused by how things are set up)

| Vulnerability | What it means / examples |
|---|---|
| **Unsecured user accounts** | Account details can be sent insecurely over the network, exposing **usernames** and **passwords** to threat actors. |
| **System accounts with easily guessed passwords** | A very common issue caused by weak/poorly created user passwords. |
| **Misconfigured internet services** | Enabling **JavaScript** in web browsers can allow attacks when visiting untrusted sites because scripts may be controlled by threat actors. Other possible weak points include misconfigured **terminal services**, **FTP**, or **web servers** such as **Microsoft IIS** and **Apache HTTP Server**. |
| **Unsecured default settings within products** | Many products ship with defaults that create or enable security holes if left unchanged. |
| **Misconfigured network equipment** | Incorrect device configuration can create major security problems. Examples listed: misconfigured **access lists**, **routing protocols**, or **SNMP community strings** can create or open security holes. |

---

### Policy vulnerabilities (weaknesses caused by people/process/governance)

| Vulnerability | What it means / examples |
|---|---|
| **Lack of written security policy** | If policy is not written down, it cannot be applied or enforced consistently. |
| **Politics** | Turf wars and political battles can block a consistent security policy. |
| **Lack of authentication continuity** | Badly chosen, default, or easily cracked passwords can allow unauthorized network access. |
| **Logical access controls not applied** | Weak monitoring/auditing can let attacks and unauthorized use continue, wasting resources. This can lead to legal action or termination against IT staff, IT management, or even company leadership that allows unsafe conditions to continue. |
| **Software and hardware installation and changes do not follow policy** | Unauthorized topology changes or installing unapproved applications can create or enable security holes. |
| **Disaster recovery plan is nonexistent** | Without a disaster recovery plan, natural disasters or attacks can cause chaos, panic, and confusion inside the enterprise. |

---

## What’s next
Send the next screenshots (16.1.3 Physical Security and onward) and I’ll keep appending in the exact same style, including **all Check Your Understanding questions + answers** when we reach them.


---# CCNA ITN — Module 16: Network Security Fundamentals (Study Guide)

Quick-reference + ultra-detailed study notes for **Cisco NetAcad CCNA: Introduction to Networks (ITN)**  
**Module 16 — Network Security Fundamentals**

> **Status:** This file includes everything from the screenshots you shared so far (**16.0.1 → 16.1.4**).
> It now includes **16.1.4 Check Your Understanding (Q1–Q7) with answers**.

---

## Table of Contents

- [Module 16 Overview](#module-16-overview)  
- [Module Map](#module-map)  

- [16.0 Introduction](#160-introduction)  
  - [16.0.1 Why should I take this module?](#1601-why-should-i-take-this-module)  
  - [16.0.2 What will I learn to do in this module?](#1602-what-will-i-learn-to-do-in-this-module)  

- [16.1 Security Threats and Vulnerabilities](#161-security-threats-and-vulnerabilities)  
  - [16.1.1 Types of Threats](#1611-types-of-threats)  
  - [16.1.2 Types of Vulnerabilities](#1612-types-of-vulnerabilities)  
  - [16.1.3 Physical Security](#1613-physical-security)  
  - [16.1.4 Check Your Understanding – Security Threats and Vulnerabilities](#1614-check-your-understanding--security-threats-and-vulnerabilities)  

- [16.2 Network Attacks](#162-network-attacks)  
  - [16.2.1 Types of Malware](#1621-types-of-malware)  
  - [16.2.2 Reconnaissance Attacks](#1622-reconnaissance-attacks)  
  - [16.2.3 Access Attacks](#1623-access-attacks)  
  - [16.2.4 Denial of Service Attacks](#1624-denial-of-service-attacks)  
  - [16.2.5 Check Your Understanding – Network Attacks](#1625-check-your-understanding--network-attacks)  
  - [16.2.6 Lab – Research Network Security Threats](#1626-lab--research-network-security-threats)  

- [16.3 Network Attack Mitigations](#163-network-attack-mitigations)  
  - [16.3.1 The Defense-in-Depth Approach](#1631-the-defense-in-depth-approach)  
  - [16.3.2 Keep Backups](#1632-keep-backups)  
  - [16.3.3 Upgrade, Update, and Patch](#1633-upgrade-update-and-patch)  
  - [16.3.4 Authentication, Authorization, and Accounting](#1634-authentication-authorization-and-accounting)  
  - [16.3.5 Firewalls](#1635-firewalls)  
  - [16.3.6 Types of Firewalls](#1636-types-of-firewalls)  
  - [16.3.7 Endpoint Security](#1637-endpoint-security)  
  - [16.3.8 Check Your Understanding – Network Attack Mitigation](#1638-check-your-understanding--network-attack-mitigation)  

- [16.4 Device Security](#164-device-security)  
  - [16.4.1 Cisco AutoSecure](#1641-cisco-autosecure)  
  - [16.4.2 Passwords](#1642-passwords)  
  - [16.4.3 Additional Password Security](#1643-additional-password-security)  
  - [16.4.4 Enable SSH](#1644-enable-ssh)  
  - [16.4.5 Disable Unused Services](#1645-disable-unused-services)  
  - [16.4.6 Packet Tracer – Configure Secure Passwords and SSH](#1646-packet-tracer--configure-secure-passwords-and-ssh)  
  - [16.4.7 Lab – Configure Network Devices with SSH](#1647-lab--configure-network-devices-with-ssh)  

- [16.5 Module Practice and Quiz](#165-module-practice-and-quiz)  
  - [16.5.1 Packet Tracer – Secure Network Devices](#1651-packet-tracer--secure-network-devices)  
  - [16.5.2 Lab – Secure Network Devices](#1652-lab--secure-network-devices)  
  - [16.5.3 What did I learn in this module?](#1653-what-did-i-learn-in-this-module)  
  - [16.5.4 Module Quiz – Network Security Fundamentals](#1654-module-quiz--network-security-fundamentals)  

---

## Module 16 Overview

**Big idea:** You can build a network that “works” and still be unsafe. Security is the layer that keeps the network **available**, protects **data**, and stops **unauthorized access**.

This module focuses on:
- Why networks must be secured (not just connected).
- Common ways attackers get in (weaknesses + bad configs + weak policies).
- The kinds of damage that happen once access is gained (theft, manipulation, outages).

---

## Module Map

| Topic | What you’re expected to understand |
|---|---|
| **Security Threats and Vulnerabilities** | Why basic security controls are necessary on network devices |
| **Network Attacks** | Identify security vulnerabilities |
| **Network Attack Mitigation** | Identify general mitigation techniques |
| **Device Security** | Configure network devices using device-hardening features to reduce threats |

---

# 16.0 Introduction

## 16.0.1 Why should I take this module?

Think of a network like a house.

- Building the network **without securing it** is like leaving **every door and window wide open** and then going away.
- When security is missing, anyone could:
  - get inside,
  - steal things,
  - break things,
  - or simply create chaos.

And just like on the news, **any network can be broken into** if it’s not protected.

As a network admin (or the person responsible for the network), your job is to make it **hard** for threat actors to successfully gain access.

What this module gives you:
- A high-level overview of **network attack types**
- Practical ideas for reducing the chance that attacks succeed
- **Packet Tracer activities** so you can practice basic network-security techniques

If you already have a network and it’s “working” but not as secure as it could be, this module is the place to start.

---

## 16.0.2 What will I learn to do in this module?

**Module Title:** Network Security Fundamentals  
**Module Objective:** Configure switches and routers with device-hardening features to improve security.

| Topic Title | Topic Objective (what you should be able to do) |
|---|---|
| **Security Threats and Vulnerabilities** | Explain why basic security measures are necessary on network devices. |
| **Network Attacks** | Identify security vulnerabilities. |
| **Network Attack Mitigation** | Identify general mitigation techniques. |
| **Device Security** | Configure network devices with device-hardening features to mitigate security threats. |

---

# 16.1 Security Threats and Vulnerabilities

## 16.1.1 Types of Threats

Modern life depends on wired and wireless networks.
- People and organizations rely on computers + networks for everyday work.
- If an unauthorized person breaks in, the impact can be expensive:
  - **network downtime / outages**
  - **lost work**
  - **lost time and money**
  - **damage** to systems
  - **theft** of important information or assets

### How intruders typically get access
Attackers can get into networks through:
- **software vulnerabilities**
- **hardware-based attacks**
- **guessing usernames and passwords**

Intruders who get access by **changing software** or **taking advantage of software weaknesses** are called **threat actors**.

Once a threat actor gets access, four common “outcomes” (threat types) may happen.

---

### 1) Information theft
**Meaning:** Breaking into a computer to obtain **confidential** information.

What happens next:
- That information can be **used** or **sold**
- A common example is stealing **proprietary company info**, such as **research and development data**

---

### 2) Data loss and manipulation
**Meaning:** Breaking into a computer system to **destroy** data or **change** data records.

Examples:
- **Data loss:** sending a virus that **reformats a hard drive**
- **Data manipulation:** breaking into a records system to **edit values**, like changing the **price of an item**

---

### 3) Identity theft
**Meaning:** A type of information theft where **personal information** is stolen to **take over someone’s identity**.

With stolen identity info, a threat actor may be able to:
- get legal documents,
- apply for credit,
- or make unauthorized online purchases.

Identity theft is a growing issue and can cost **billions of dollars per year**.

---

### 4) Disruption of service
**Meaning:** Preventing legitimate users from accessing services they are allowed to use.

Examples include **denial of service (DoS)** attacks that target:
- servers,
- network devices,
- or network communication links.

---

## 16.1.2 Types of Vulnerabilities

### What “vulnerability” means
A **vulnerability** is the degree of weakness in a network or device.

Important context:
- Some weakness exists naturally in many devices:
  - routers, switches,
  - desktops, servers,
  - even security devices.
- In many real incidents, the attacked targets are often **endpoints**, like servers and desktop PCs.

### The three main sources of weaknesses
There are **three primary categories** of vulnerabilities:
1. **Technological vulnerabilities**
2. **Configuration vulnerabilities**
3. **Security policy vulnerabilities**

Any of these can leave a network/device exposed to many attack types, including:
- **malicious code attacks**
- **network attacks**

---

### Technological vulnerabilities (built-in / structural weaknesses)

| Vulnerability | What it means / examples |
|---|---|
| **TCP/IP protocol weakness** | Some widely used protocols were not designed with strong security in mind. Examples listed: **HTTP**, **FTP**, and **ICMP** are inherently insecure. Also listed: **SNMP** and **SMTP** relate to the insecure structure on which TCP was designed. |
| **Operating system weakness** | Every OS has security issues that must be addressed. Examples listed: **UNIX**, **Linux**, **Mac OS**, **Mac OS X**, **Windows Server 2012**, **Windows 7**, **Windows 8**. These issues are documented in **CERT** archives (Computer Emergency Response Team) at **http://www.cert.org**. |
| **Network equipment weakness** | Networking devices (routers, firewalls, switches) can have weaknesses that must be recognized and protected against. Examples listed include weaknesses involving **password protection**, **lack of authentication**, **routing protocols**, and **firewall holes**. |

---

### Configuration vulnerabilities (weaknesses caused by how things are set up)

| Vulnerability | What it means / examples |
|---|---|
| **Unsecured user accounts** | Account details can be sent insecurely over the network, exposing **usernames** and **passwords** to threat actors. |
| **System accounts with easily guessed passwords** | A very common issue caused by weak/poorly created user passwords. |
| **Misconfigured internet services** | Enabling **JavaScript** in web browsers can allow attacks when visiting untrusted sites because scripts may be controlled by threat actors. Other possible weak points include misconfigured **terminal services**, **FTP**, or **web servers** such as **Microsoft IIS** and **Apache HTTP Server**. |
| **Unsecured default settings within products** | Many products ship with defaults that create or enable security holes if left unchanged. |
| **Misconfigured network equipment** | Incorrect device configuration can create major security problems. Examples listed: misconfigured **access lists**, **routing protocols**, or **SNMP community strings** can create or open security holes. |

---

### Policy vulnerabilities (weaknesses caused by people/process/governance)

| Vulnerability | What it means / examples |
|---|---|
| **Lack of written security policy** | If policy is not written down, it cannot be applied or enforced consistently. |
| **Politics** | Turf wars and political battles can block a consistent security policy. |
| **Lack of authentication continuity** | Poorly chosen, easily cracked, or default passwords can allow unauthorized access to the network. |
| **Logical access controls not applied** | Weak monitoring/auditing can let attacks and unauthorized use continue, wasting resources. This can lead to legal action or termination against IT staff, IT management, or even company leadership that allows unsafe conditions to continue. |
| **Software and hardware installation and changes do not follow policy** | Unauthorized topology changes or installing unapproved applications can create or enable security holes. |
| **Disaster recovery plan is nonexistent** | Without a disaster recovery plan, natural disasters or attacks can cause chaos, panic, and confusion inside the enterprise. |

---

## 16.1.3 Physical Security

Physical security is just as critical as “cyber” security. If an attacker (or even an accident) can physically compromise networking resources, they can prevent the organization from using those resources.

A common way to categorize *physical* threats is into four classes:

- **Hardware threats** — Direct physical damage to equipment such as servers, routers, switches, the cabling plant, and workstations.
- **Environmental threats** — Extreme **temperature** (too hot or too cold) or **humidity** (too wet or too dry) that can harm devices.
- **Electrical threats** — Power issues such as **voltage spikes**, **brownouts** (insufficient voltage), **noisy/unconditioned power**, and **complete power loss**.
- **Maintenance threats** — Problems caused by poor maintenance practices (e.g., mishandling sensitive components leading to **electrostatic discharge (ESD)**), missing critical spare parts, bad cabling, and poor labeling.

Because these risks are predictable, a physical security plan should be designed and put into practice to reduce damage and limit downtime.

### Example physical security plan (figure)

**Goal:** Secure the computer room and reduce damage to equipment.

**Figure callouts / layout (what’s shown):**
- A **separate equipment room** containing racks labeled **SVRS**, **WAN**, and **LAN**
- **AC** and a **UPS bay** in the equipment room
- A **locked door** between the help desk area and the equipment room
- A **card reader** at the controlled entry point (help desk side)
- A public-facing **door** into the help desk area

**Steps in the plan:**
1. **Lock up the equipment** and block unauthorized access paths (doors, ceiling, raised floor, windows, ducts, vents).
2. **Monitor and control entry** to the closet/room using **electronic logs**.
3. **Use security cameras** for visibility and evidence.

---

## 16.1.4 Check Your Understanding — Security Threats and Vulnerabilities

### Question 1
**A threat actor sends a virus that can reformat your hard drive. What type of threat is this?**

- Information theft  
- Disruption of service  
- Identity theft  
- ✅ **Data loss or manipulation**

**Answer:** Data loss or manipulation  
**Why:** Reformatting destroys data (a classic *data loss* scenario).

---

### Question 2
**A threat actor makes illegal online purchases using stolen credit information. What type of threat is this?**

- Data loss or manipulation  
- Information theft  
- ✅ **Identity theft**  
- Disruption of service  

**Answer:** Identity theft  
**Why:** Using stolen personal/credit details to buy things is identity takeover/abuse.

---

### Question 3
**A threat actor prevents legitimate users from accessing data services. What type of threat is this?**

- ✅ **Disruption of service**  
- Identity theft  
- Information theft  
- Data loss or manipulation  

**Answer:** Disruption of service  
**Why:** The main impact is blocking availability (DoS-style outcome).

---

### Question 4
**A threat actor steals scientific research data. What type of threat is this?**

- Data loss or manipulation  
- Identity theft  
- ✅ **Information theft**  
- Disruption of service  

**Answer:** Information theft  
**Why:** Research data is confidential/proprietary information being stolen.

---

### Question 5
**A threat actor overloads a network to deny other users network access. What type of threat is this?**

- Identity theft  
- ✅ **Disruption of service**  
- Data loss or manipulation  
- Information theft  

**Answer:** Disruption of service  
**Why:** Overloading the network to block access is denial of service (availability attack).

---

### Question 6
**A threat actor changes/edits data records. What type of threat is this?**

- ✅ **Data loss or manipulation**  
- Identity theft  
- Information theft  
- Disruption of service  

**Answer:** Data loss or manipulation  
**Why:** Altering records is *data manipulation* (integrity impact).

---

### Question 7
**A threat actor steals a company’s user database. What type of threat is this?**

- Disruption of service  
- ✅ **Information theft**  
- Data loss or manipulation  
- Identity theft  

**Answer:** Information theft  
**Why:** A user database is sensitive/confidential information being taken.

---

## What’s next

Send the next screenshots starting at **16.2.1 Types of Malware** (and keep going in order). I’ll keep paraphrasing everything and I’ll capture **every Check Your Understanding question + answer** as we reach them.






16.0.1 Why should I take this module?
Welcome to Network Security Fundamentals!

You may have already set up a network, or you may be getting ready to do just that. Here is something to think about. Setting up a network without securing it is like opening all the doors and windows to your home and then going on vacation. Anyone could come by, gain entry, steal or break items, or just make a mess. As you have seen on the news, it is possible to break into any network! As a network administrator, it is part of your job to make it difficult for threat actors to gain access to your network. This module gives you an overview of types of network attacks and what you can do to reduce a threat actor’s chances of succeeding. It also has Packet Tracer activities to let you practice some basic techniques for network security. If you have a network, but it is not as secure as possible, then you will want to read this module right now!

16.0.2 What will I learn to do in this module?
Module Title: Network Security Fundamentals

Module Objective: Configure switches and routers with device hardening features to enhance security.

<img width="1037" height="302" alt="image" src="https://github.com/user-attachments/assets/52882c3e-0a7a-42e3-8bd8-9f30ec4d2e2b" />





# CCNA ITN — Module 16: Network Security Fundamentals (Study Guide)

Quick-reference + ultra-detailed study notes for **Cisco NetAcad CCNA: Introduction to Networks (ITN)**  
**Module 16 — Network Security Fundamentals**

> **Status:** This file includes everything from the screenshots you shared so far (**16.0.1 → 16.2.3**).  
> **Coverage so far:** 16.0.1 → 16.2.3 (includes 16.1.4 Check Your Understanding Q1–Q7).

---

## Table of Contents

- [Module 16 Overview](#module-16-overview)  
- [Module Map](#module-map)  

- [16.0 Introduction](#160-introduction)  
  - [16.0.1 Why should I take this module?](#1601-why-should-i-take-this-module)  
  - [16.0.2 What will I learn to do in this module?](#1602-what-will-i-learn-to-do-in-this-module)  

- [16.1 Security Threats and Vulnerabilities](#161-security-threats-and-vulnerabilities)  
  - [16.1.1 Types of Threats](#1611-types-of-threats)  
  - [16.1.2 Types of Vulnerabilities](#1612-types-of-vulnerabilities)  
  - [16.1.3 Physical Security](#1613-physical-security)  
  - [16.1.4 Check Your Understanding – Security Threats and Vulnerabilities](#1614-check-your-understanding--security-threats-and-vulnerabilities)  

- [16.2 Network Attacks](#162-network-attacks)  
  - [16.2.1 Types of Malware](#1621-types-of-malware)  
  - [16.2.2 Reconnaissance Attacks](#1622-reconnaissance-attacks)  
  - [16.2.3 Access Attacks](#1623-access-attacks)  
  - [16.2.4 Denial of Service Attacks](#1624-denial-of-service-attacks)  
  - [16.2.5 Check Your Understanding – Network Attacks](#1625-check-your-understanding--network-attacks)  
  - [16.2.6 Lab – Research Network Security Threats](#1626-lab--research-network-security-threats)  

- [16.3 Network Attack Mitigations](#163-network-attack-mitigations)  
  - [16.3.1 The Defense-in-Depth Approach](#1631-the-defense-in-depth-approach)  
  - [16.3.2 Keep Backups](#1632-keep-backups)  
  - [16.3.3 Upgrade, Update, and Patch](#1633-upgrade-update-and-patch)  
  - [16.3.4 Authentication, Authorization, and Accounting](#1634-authentication-authorization-and-accounting)  
  - [16.3.5 Firewalls](#1635-firewalls)  
  - [16.3.6 Types of Firewalls](#1636-types-of-firewalls)  
  - [16.3.7 Endpoint Security](#1637-endpoint-security)  
  - [16.3.8 Check Your Understanding – Network Attack Mitigation](#1638-check-your-understanding--network-attack-mitigation)  

- [16.4 Device Security](#164-device-security)  
  - [16.4.1 Cisco AutoSecure](#1641-cisco-autosecure)  
  - [16.4.2 Passwords](#1642-passwords)  
  - [16.4.3 Additional Password Security](#1643-additional-password-security)  
  - [16.4.4 Enable SSH](#1644-enable-ssh)  
  - [16.4.5 Disable Unused Services](#1645-disable-unused-services)  
  - [16.4.6 Packet Tracer – Configure Secure Passwords and SSH](#1646-packet-tracer--configure-secure-passwords-and-ssh)  
  - [16.4.7 Lab – Configure Network Devices with SSH](#1647-lab--configure-network-devices-with-ssh)  

- [16.5 Module Practice and Quiz](#165-module-practice-and-quiz)  
  - [16.5.1 Packet Tracer – Secure Network Devices](#1651-packet-tracer--secure-network-devices)  
  - [16.5.2 Lab – Secure Network Devices](#1652-lab--secure-network-devices)  
  - [16.5.3 What did I learn in this module?](#1653-what-did-i-learn-in-this-module)  
  - [16.5.4 Module Quiz – Network Security Fundamentals](#1654-module-quiz--network-security-fundamentals)

---

## Module 16 Overview

**Big idea:** You can build a network that “works” and still be unsafe. Security is the layer that keeps the network **available**, protects **data**, and stops **unauthorized access**.

This module focuses on:
- Why networks must be secured (not just connected).
- Common ways attackers get in (weaknesses + bad configs + weak policies).
- The kinds of damage that happen once access is gained (theft, manipulation, outages).

---

## Module Map

| Topic | What you’re expected to understand |
|---|---|
| **Security Threats and Vulnerabilities** | Why basic security controls are necessary on network devices |
| **Network Attacks** | Identify security vulnerabilities |
| **Network Attack Mitigation** | Identify general mitigation techniques |
| **Device Security** | Configure network devices using device-hardening features to reduce threats |

---

# 16.0 Introduction

## 16.0.1 Why should I take this module?

Think of a network like a house.

- Building the network **without securing it** is like leaving **every door and window wide open** and then going away.
- When security is missing, anyone could:
  - get inside,
  - steal things,
  - break things,
  - or simply create chaos.

And just like on the news, **any network can be broken into** if it’s not protected.

As a network admin (or the person responsible for the network), your job is to make it **hard** for threat actors to successfully gain access.

What this module gives you:
- A high-level overview of **network attack types**
- Practical ideas for reducing the chance that attacks succeed
- **Packet Tracer activities** so you can practice basic network-security techniques

If you already have a network and it’s “working” but not as secure as it could be, this module is the place to start.

---

## 16.0.2 What will I learn to do in this module?

**Module Title:** Network Security Fundamentals  
**Module Objective:** Configure switches and routers with device-hardening features to improve security.

| Topic Title | Topic Objective (what you should be able to do) |
|---|---|
| **Security Threats and Vulnerabilities** | Explain why basic security measures are necessary on network devices. |
| **Network Attacks** | Identify security vulnerabilities. |
| **Network Attack Mitigation** | Identify general mitigation techniques. |
| **Device Security** | Configure network devices with device-hardening features to mitigate security threats. |

---

# 16.1 Security Threats and Vulnerabilities

## 16.1.1 Types of Threats

Modern life depends on wired and wireless networks.
- People and organizations rely on computers + networks for everyday work.
- If an unauthorized person breaks in, the impact can be expensive:
  - **network downtime / outages**
  - **lost work**
  - **lost time and money**
  - **damage** to systems
  - **theft** of important information or assets

### How intruders typically get access
Attackers can get into networks through:
- **software vulnerabilities**
- **hardware-based attacks**
- **guessing usernames and passwords**

Intruders who get access by **changing software** or **taking advantage of software weaknesses** are called **threat actors**.

Once a threat actor gets access, four common “outcomes” (threat types) may happen.

---

### 1) Information theft
**Meaning:** Breaking into a computer to obtain **confidential** information.

What happens next:
- That information can be **used** or **sold**
- A common example is stealing **proprietary company info**, such as **research and development data**

---

### 2) Data loss and manipulation
**Meaning:** Breaking into a computer system to **destroy** data or **change** data records.

Examples:
- **Data loss:** sending a virus that **reformats a hard drive**
- **Data manipulation:** breaking into a records system to **edit values**, like changing the **price of an item**

---

### 3) Identity theft
**Meaning:** A type of information theft where **personal information** is stolen to **take over someone’s identity**.

With stolen identity info, a threat actor may be able to:
- get legal documents,
- apply for credit,
- or make unauthorized online purchases.

Identity theft is a growing issue and can cost **billions of dollars per year**.

---

### 4) Disruption of service
**Meaning:** Preventing legitimate users from accessing services they are allowed to use.

Examples include **denial of service (DoS)** attacks that target:
- servers,
- network devices,
- or network communication links.

---

## 16.1.2 Types of Vulnerabilities

### What “vulnerability” means
A **vulnerability** is the degree of weakness in a network or device.

Important context:
- Some weakness exists naturally in many devices:
  - routers, switches,
  - desktops, servers,
  - even security devices.
- In many real incidents, the attacked targets are often **endpoints**, like servers and desktop PCs.

### The three main sources of weaknesses
There are **three primary categories** of vulnerabilities:
1. **Technological vulnerabilities**
2. **Configuration vulnerabilities**
3. **Security policy vulnerabilities**

Any of these can leave a network/device exposed to many attack types, including:
- **malicious code attacks**
- **network attacks**

---

### Technological vulnerabilities (built-in / structural weaknesses)

| Vulnerability | What it means / examples |
|---|---|
| **TCP/IP protocol weakness** | Some widely used protocols were not designed with strong security in mind. Examples listed: **HTTP**, **FTP**, and **ICMP** are inherently insecure. Also listed: **SNMP** and **SMTP** relate to the insecure structure on which TCP was designed. |
| **Operating system weakness** | Every OS has security issues that must be addressed. Examples listed: **UNIX**, **Linux**, **Mac OS**, **Mac OS X**, **Windows Server 2012**, **Windows 7**, **Windows 8**. These issues are documented in **CERT** archives (Computer Emergency Response Team) at **http://www.cert.org**. |
| **Network equipment weakness** | Networking devices (routers, firewalls, switches) can have weaknesses that must be recognized and protected against. Examples listed include weaknesses involving **password protection**, **lack of authentication**, **routing protocols**, and **firewall holes**. |

---

### Configuration vulnerabilities (weaknesses caused by how things are set up)

| Vulnerability | What it means / examples |
|---|---|
| **Unsecured user accounts** | Account details can be sent insecurely over the network, exposing **usernames** and **passwords** to threat actors. |
| **System accounts with easily guessed passwords** | A very common issue caused by weak/poorly created user passwords. |
| **Misconfigured internet services** | Enabling **JavaScript** in web browsers can allow attacks when visiting untrusted sites because scripts may be controlled by threat actors. Other possible weak points include misconfigured **terminal services**, **FTP**, or **web servers** such as **Microsoft IIS** and **Apache HTTP Server**. |
| **Unsecured default settings within products** | Many products ship with defaults that create or enable security holes if left unchanged. |
| **Misconfigured network equipment** | Incorrect device configuration can create major security problems. Examples listed: misconfigured **access lists**, **routing protocols**, or **SNMP community strings** can create or open security holes. |

---

### Policy vulnerabilities (weaknesses caused by people/process/governance)

| Vulnerability | What it means / examples |
|---|---|
| **Lack of written security policy** | If policy is not written down, it cannot be applied or enforced consistently. |
| **Politics** | Turf wars and political battles can block a consistent security policy. |
| **Lack of authentication continuity** | Badly chosen, default, or easily cracked passwords can allow unauthorized network access. |
| **Logical access controls not applied** | Weak monitoring/auditing can let attacks and unauthorized use continue, wasting resources. This can lead to legal action or termination against IT staff, IT management, or even company leadership that allows unsafe conditions to continue. |
| **Software and hardware installation and changes do not follow policy** | Unauthorized topology changes or installing unapproved applications can create or enable security holes. |
| **Disaster recovery plan is nonexistent** | Without a disaster recovery plan, natural disasters or attacks can cause chaos, panic, and confusion inside the enterprise. |

---

## What’s next
Send the next screenshots (16.1.3 Physical Security and onward) and I’ll keep appending in the exact same style, including **all Check Your Understanding questions + answers** when we reach them.
## 16.1.3 Physical Security

Physical security is another major “weak spot” to think about. If someone can **physically** compromise your equipment, they may be able to **deny access** to network resources even without sophisticated hacking.

The module groups physical threats into four classes:

- **Hardware threats** — Physical damage to servers, routers, switches, cabling plant, and workstations.
- **Environmental threats** — Temperature extremes (too hot / too cold) and humidity extremes (too wet / too dry).
- **Electrical threats** — Voltage spikes, insufficient voltage (**brownouts**), unconditioned power (“noise”), and total power loss.
- **Maintenance threats** — Poor handling of key electrical components (example: electrostatic discharge), missing critical spare parts, poor cabling, and poor labelling.

A strong physical security plan should be **designed and implemented** to reduce these risks.

### Example physical security plan concepts (from the diagram)

- **Secure the computer room** (controlled access)
- Apply controls that **limit damage** to equipment (AC, UPS, locked/controlled access)

Steps shown:
1. **Lock up equipment and block unauthorised access paths** (doors, ceiling, raised floor, windows, ducts, vents).
2. **Monitor and control entry** using electronic logs (example: card reader).
3. **Use security cameras** for visibility and evidence.

---

## 16.1.4 Check Your Understanding – Security Threats and Vulnerabilities

> Answers are based on the threat outcomes described in **16.1.1 Types of Threats**.

**Q1.** What kind of threat is described when a threat actor sends you a virus that can reformat your hard drive?  
✅ **Answer:** **Data loss or manipulation**

**Q2.** What kind of threat is described when a threat actor makes illegal online purchases using stolen credit information?  
✅ **Answer:** **Identity theft**

**Q3.** What kind of threat is described when a threat actor prevents legal users from accessing data services?  
✅ **Answer:** **Disruption of service**

**Q4.** What kind of threat is described when a threat actor steals scientific research data?  
✅ **Answer:** **Information theft**

**Q5.** What kind of threat is described when a threat actor overloads a network to deny other users network access?  
✅ **Answer:** **Disruption of service**

**Q6.** What kind of threat is described when a threat actor alters data records?  
✅ **Answer:** **Data loss or manipulation**

**Q7.** What kind of threat is described when a threat actor is stealing the user database of a company?  
✅ **Answer:** **Information theft**

> **Note:** The prints show Q1–Q8 navigation, but only Q1–Q7 were provided here. Send Q8 and I’ll add it in the same format.

---

## 16.2 Network Attacks

This section goes deeper into **how** threat actors gain access to networks or stop authorised users from getting access.

### 16.2.1 Types of Malware

**Malware** = *malicious software*. It is software/code specifically designed to **damage, disrupt, steal**, or perform other “bad” / illegitimate actions against data, hosts, or networks.

Three malware categories highlighted here are: **viruses**, **worms**, and **Trojan horses**.

#### Viruses

A **computer virus** spreads by inserting a copy of itself into (and becoming part of) another program.

Key points from the module:
- It can spread from computer to computer, leaving infections behind.
- Viruses range from mildly annoying to serious damage (including data/software damage and even DoS conditions).
- Most viruses are attached to an **executable file**, meaning:
  - the virus may exist on the system but is not “active” and cannot spread until a user runs/opens the malicious host file/program.
- When the host code runs, the viral code runs too.
- Usually the host program still functions after infection, but some viruses overwrite other programs with copies of themselves, destroying the original host program.
- Viruses can spread when infected software/documents are transferred by:
  - the network,
  - a disk,
  - file sharing,
  - or infected email attachments.

#### Worms

A **worm** is similar to a virus in that it replicates and can cause similar damage, but the big difference is how it spreads:

- Worms are **standalone** software.
- Unlike viruses (which need an infected host file), worms do **not** require a host program or human help to propagate.
- A worm does not need to attach to a program to infect a host; it can enter through a **vulnerability** in the system.
- Worms take advantage of system features to travel through the network **unaided**.

#### Trojan horses

A **Trojan horse** looks legitimate but is harmful—named after the wooden horse story used to infiltrate Troy.

Key points from the module:
- Users are usually tricked into loading and executing it.
- Once active, it can do many kinds of harm (examples given):
  - annoy the user (excessive pop-up windows),
  - change the desktop,
  - damage the host (delete files, steal data),
  - activate and spread other malware (including viruses).
- Trojans are also commonly used to create **back doors** that give attackers access to the system.
- Unlike viruses and worms, Trojans do **not** reproduce by infecting other files.
- They spread mainly via **user interaction**, such as opening an email attachment or downloading and running a file from the internet.

---

### 16.2.2 Reconnaissance Attacks

Networks can be hit by multiple types of network attacks. The module groups them into three big categories:

- **Reconnaissance attacks** — discovering and mapping systems, services, or vulnerabilities  
- **Access attacks** — unauthorised manipulation of data, system access, or user privileges  
- **Denial of service** — disabling or corrupting networks, systems, or services  

Reconnaissance is often about gathering information first:

- Threat actors can use internet tools like **nslookup** and **whois** to determine the IP address space assigned to an organisation.
- After identifying the address space, a threat actor can ping the public IPs to see which addresses are active.
- To automate discovery, the module mentions using a **ping sweep** tool such as **fping** or **gping**.
- A ping sweep systematically pings all network addresses in a given range/subnet—like calling every number in a phonebook to see who answers.

Recon tools highlighted in the interactive content:

#### Internet queries
The threat actor looks for initial information about a target using tools such as:
- Google search,
- organisation websites,
- whois,
- and similar public sources.

#### Ping sweeps
The threat actor runs a ping sweep to determine which IP addresses are active.

#### Port scans
After discovering active IPs, the threat actor performs a port scan on those addresses.

---

### 16.2.3 Access Attacks

Access attacks exploit known weaknesses in services (examples listed):
- authentication services,
- FTP services,
- web services,

to gain entry to:
- web accounts,
- confidential databases,
- other sensitive information.

In short: they allow unauthorised access to information a user has **no right** to view.

The module classifies access attacks into four types:

#### Password attacks
Methods mentioned:
- **brute-force attacks**
- **Trojan horse attacks**
- **packet sniffers**

#### Trust exploitation
In a trust exploitation attack, the threat actor leverages unauthorised privileges to gain access—often by abusing trust relationships.

Scenario described:
- **System A trusts System B**
- **System B trusts everyone**
- The attacker wants access to System A, so they compromise System B first, then use System B to attack System A.

#### Port redirection
In port redirection, a compromised system is used as a base for attacks against other targets.

Example described:
- Attacker uses **SSH (port 22)** to connect to compromised Host A.
- Because Host A is trusted by Host B, the attacker can then use **Telnet (port 23)** to access Host B.

#### Man-in-the-middle
A man-in-the-middle (MitM) attack places the threat actor between two legitimate entities so they can read or modify data in transit.

Steps shown:
1. Victim requests a web page; the request is directed to the threat actor’s computer.
2. The threat actor receives the request and retrieves the real page from the legitimate website.
3. The threat actor can modify the page and change the data.
4. The threat actor forwards the requested (possibly modified) page to the victim.

---

# CCNA ITN — Module 16: Network Security Fundamentals (Study Guide)

Quick-reference + ultra-detailed study notes for **Cisco NetAcad CCNA: Introduction to Networks (ITN)**  
**Module 16 — Network Security Fundamentals**

> **Status:** This file includes everything from the screenshots you shared so far (**16.0.1 → 16.1.2**).  
> Next sections (16.1.3+, 16.1.4 questions, etc.) will be added when you drop the next prints.

---

## Table of Contents

- [Module 16 Overview](#module-16-overview)  
- [Module Map](#module-map)  

- [16.0 Introduction](#160-introduction)  
  - [16.0.1 Why should I take this module?](#1601-why-should-i-take-this-module)  
  - [16.0.2 What will I learn to do in this module?](#1602-what-will-i-learn-to-do-in-this-module)  

- [16.1 Security Threats and Vulnerabilities](#161-security-threats-and-vulnerabilities)  
  - [16.1.1 Types of Threats](#1611-types-of-threats)  
  - [16.1.2 Types of Vulnerabilities](#1612-types-of-vulnerabilities)  
  - [16.1.3 Physical Security](#1613-physical-security)  
  - [16.1.4 Check Your Understanding – Security Threats and Vulnerabilities](#1614-check-your-understanding--security-threats-and-vulnerabilities)  

- [16.2 Network Attacks](#162-network-attacks)  
  - [16.2.1 Types of Malware](#1621-types-of-malware)  
  - [16.2.2 Reconnaissance Attacks](#1622-reconnaissance-attacks)  
  - [16.2.3 Access Attacks](#1623-access-attacks)  
  - [16.2.4 Denial of Service Attacks](#1624-denial-of-service-attacks)  
  - [16.2.5 Check Your Understanding – Network Attacks](#1625-check-your-understanding--network-attacks)  
  - [16.2.6 Lab – Research Network Security Threats](#1626-lab--research-network-security-threats)  

- [16.3 Network Attack Mitigations](#163-network-attack-mitigations)  
  - [16.3.1 The Defense-in-Depth Approach](#1631-the-defense-in-depth-approach)  
  - [16.3.2 Keep Backups](#1632-keep-backups)  
  - [16.3.3 Upgrade, Update, and Patch](#1633-upgrade-update-and-patch)  
  - [16.3.4 Authentication, Authorization, and Accounting](#1634-authentication-authorization-and-accounting)  
  - [16.3.5 Firewalls](#1635-firewalls)  
  - [16.3.6 Types of Firewalls](#1636-types-of-firewalls)  
  - [16.3.7 Endpoint Security](#1637-endpoint-security)  
  - [16.3.8 Check Your Understanding – Network Attack Mitigation](#1638-check-your-understanding--network-attack-mitigation)  

- [16.4 Device Security](#164-device-security)  
  - [16.4.1 Cisco AutoSecure](#1641-cisco-autosecure)  
  - [16.4.2 Passwords](#1642-passwords)  
  - [16.4.3 Additional Password Security](#1643-additional-password-security)  
  - [16.4.4 Enable SSH](#1644-enable-ssh)  
  - [16.4.5 Disable Unused Services](#1645-disable-unused-services)  
  - [16.4.6 Packet Tracer – Configure Secure Passwords and SSH](#1646-packet-tracer--configure-secure-passwords-and-ssh)  
  - [16.4.7 Lab – Configure Network Devices with SSH](#1647-lab--configure-network-devices-with-ssh)  

- [16.5 Module Practice and Quiz](#165-module-practice-and-quiz)  
  - [16.5.1 Packet Tracer – Secure Network Devices](#1651-packet-tracer--secure-network-devices)  
  - [16.5.2 Lab – Secure Network Devices](#1652-lab--secure-network-devices)  
  - [16.5.3 What did I learn in this module?](#1653-what-did-i-learn-in-this-module)  
  - [16.5.4 Module Quiz – Network Security Fundamentals](#1654-module-quiz--network-security-fundamentals)

---

## Module 16 Overview

**Big idea:** You can build a network that “works” and still be unsafe. Security is the layer that keeps the network **available**, protects **data**, and stops **unauthorized access**.

This module focuses on:
- Why networks must be secured (not just connected).
- Common ways attackers get in (weaknesses + bad configs + weak policies).
- The kinds of damage that happen once access is gained (theft, manipulation, outages).

---

## Module Map

| Topic | What you’re expected to understand |
|---|---|
| **Security Threats and Vulnerabilities** | Why basic security controls are necessary on network devices |
| **Network Attacks** | Identify security vulnerabilities |
| **Network Attack Mitigation** | Identify general mitigation techniques |
| **Device Security** | Configure network devices using device-hardening features to reduce threats |

---

# 16.0 Introduction

## 16.0.1 Why should I take this module?

Think of a network like a house.

- Building the network **without securing it** is like leaving **every door and window wide open** and then going away.
- When security is missing, anyone could:
  - get inside,
  - steal things,
  - break things,
  - or simply create chaos.

And just like on the news, **any network can be broken into** if it’s not protected.

As a network admin (or the person responsible for the network), your job is to make it **hard** for threat actors to successfully gain access.

What this module gives you:
- A high-level overview of **network attack types**
- Practical ideas for reducing the chance that attacks succeed
- **Packet Tracer activities** so you can practice basic network-security techniques

If you already have a network and it’s “working” but not as secure as it could be, this module is the place to start.

---

## 16.0.2 What will I learn to do in this module?

**Module Title:** Network Security Fundamentals  
**Module Objective:** Configure switches and routers with device-hardening features to improve security.

| Topic Title | Topic Objective (what you should be able to do) |
|---|---|
| **Security Threats and Vulnerabilities** | Explain why basic security measures are necessary on network devices. |
| **Network Attacks** | Identify security vulnerabilities. |
| **Network Attack Mitigation** | Identify general mitigation techniques. |
| **Device Security** | Configure network devices with device-hardening features to mitigate security threats. |

---

# 16.1 Security Threats and Vulnerabilities

## 16.1.1 Types of Threats

Modern life depends on wired and wireless networks.
- People and organizations rely on computers + networks for everyday work.
- If an unauthorized person breaks in, the impact can be expensive:
  - **network downtime / outages**
  - **lost work**
  - **lost time and money**
  - **damage** to systems
  - **theft** of important information or assets

### How intruders typically get access
Attackers can get into networks through:
- **software vulnerabilities**
- **hardware-based attacks**
- **guessing usernames and passwords**

Intruders who get access by **changing software** or **taking advantage of software weaknesses** are called **threat actors**.

Once a threat actor gets access, four common “outcomes” (threat types) may happen.

---

### 1) Information theft
**Meaning:** Breaking into a computer to obtain **confidential** information.

What happens next:
- That information can be **used** or **sold**
- A common example is stealing **proprietary company info**, such as **research and development data**

---

### 2) Data loss and manipulation
**Meaning:** Breaking into a computer system to **destroy** data or **change** data records.

Examples:
- **Data loss:** sending a virus that **reformats a hard drive**
- **Data manipulation:** breaking into a records system to **edit values**, like changing the **price of an item**

---

### 3) Identity theft
**Meaning:** A type of information theft where **personal information** is stolen to **take over someone’s identity**.

With stolen identity info, a threat actor may be able to:
- get legal documents,
- apply for credit,
- or make unauthorized online purchases.

Identity theft is a growing issue and can cost **billions of dollars per year**.

---

### 4) Disruption of service
**Meaning:** Preventing legitimate users from accessing services they are allowed to use.

Examples include **denial of service (DoS)** attacks that target:
- servers,
- network devices,
- or network communication links.

---

## 16.1.2 Types of Vulnerabilities

### What “vulnerability” means
A **vulnerability** is the degree of weakness in a network or device.

Important context:
- Some weakness exists naturally in many devices:
  - routers, switches,
  - desktops, servers,
  - even security devices.
- In many real incidents, the attacked targets are often **endpoints**, like servers and desktop PCs.

### The three main sources of weaknesses
There are **three primary categories** of vulnerabilities:
1. **Technological vulnerabilities**
2. **Configuration vulnerabilities**
3. **Security policy vulnerabilities**

Any of these can leave a network/device exposed to many attack types, including:
- **malicious code attacks**
- **network attacks**

---

### Technological vulnerabilities (built-in / structural weaknesses)

| Vulnerability | What it means / examples |
|---|---|
| **TCP/IP protocol weakness** | Some widely used protocols were not designed with strong security in mind. Examples listed: **HTTP**, **FTP**, and **ICMP** are inherently insecure. Also listed: **SNMP** and **SMTP** relate to the insecure structure on which TCP was designed. |
| **Operating system weakness** | Every OS has security issues that must be addressed. Examples listed: **UNIX**, **Linux**, **Mac OS**, **Mac OS X**, **Windows Server 2012**, **Windows 7**, **Windows 8**. These issues are documented in **CERT** archives (Computer Emergency Response Team) at **http://www.cert.org**. |
| **Network equipment weakness** | Networking devices (routers, firewalls, switches) can have weaknesses that must be recognized and protected against. Examples listed include weaknesses involving **password protection**, **lack of authentication**, **routing protocols**, and **firewall holes**. |

---

### Configuration vulnerabilities (weaknesses caused by how things are set up)

| Vulnerability | What it means / examples |
|---|---|
| **Unsecured user accounts** | Account details can be sent insecurely over the network, exposing **usernames** and **passwords** to threat actors. |
| **System accounts with easily guessed passwords** | A very common issue caused by weak/poorly created user passwords. |
| **Misconfigured internet services** | Enabling **JavaScript** in web browsers can allow attacks when visiting untrusted sites because scripts may be controlled by threat actors. Other possible weak points include misconfigured **terminal services**, **FTP**, or **web servers** such as **Microsoft IIS** and **Apache HTTP Server**. |
| **Unsecured default settings within products** | Many products ship with defaults that create or enable security holes if left unchanged. |
| **Misconfigured network equipment** | Incorrect device configuration can create major security problems. Examples listed: misconfigured **access lists**, **routing protocols**, or **SNMP community strings** can create or open security holes. |

---

### Policy vulnerabilities (weaknesses caused by people/process/governance)

| Vulnerability | What it means / examples |
|---|---|
| **Lack of written security policy** | If policy is not written down, it cannot be applied or enforced consistently. |
| **Politics** | Turf wars and political battles can block a consistent security policy. |
| **Lack of authentication continuity** | Badly chosen, default, or easily cracked passwords can allow unauthorized network access. |
| **Logical access controls not applied** | Weak monitoring/auditing can let attacks and unauthorized use continue, wasting resources. This can lead to legal action or termination against IT staff, IT management, or even company leadership that allows unsafe conditions to continue. |
| **Software and hardware installation and changes do not follow policy** | Unauthorized topology changes or installing unapproved applications can create or enable security holes. |
| **Disaster recovery plan is nonexistent** | Without a disaster recovery plan, natural disasters or attacks can cause chaos, panic, and confusion inside the enterprise. |

---

## What’s next
Send the next screenshots (16.1.3 Physical Security and onward) and I’ll keep appending in the exact same style, including **all Check Your Understanding questions + answers** when we reach them.
## 16.1.3 Physical Security

Physical security is another major “weak spot” to think about. If someone can **physically** compromise your equipment, they may be able to **deny access** to network resources even without sophisticated hacking.

The module groups physical threats into four classes:

- **Hardware threats** — Physical damage to servers, routers, switches, cabling plant, and workstations.
- **Environmental threats** — Temperature extremes (too hot / too cold) and humidity extremes (too wet / too dry).
- **Electrical threats** — Voltage spikes, insufficient voltage (**brownouts**), unconditioned power (“noise”), and total power loss.
- **Maintenance threats** — Poor handling of key electrical components (example: electrostatic discharge), missing critical spare parts, poor cabling, and poor labelling.

A strong physical security plan should be **designed and implemented** to reduce these risks.

### Example physical security plan concepts (from the diagram)

- **Secure the computer room** (controlled access)
- Apply controls that **limit damage** to equipment (AC, UPS, locked/controlled access)

Steps shown:
1. **Lock up equipment and block unauthorised access paths** (doors, ceiling, raised floor, windows, ducts, vents).
2. **Monitor and control entry** using electronic logs (example: card reader).
3. **Use security cameras** for visibility and evidence.

---

## 16.1.4 Check Your Understanding – Security Threats and Vulnerabilities

> Answers are based on the threat outcomes described in **16.1.1 Types of Threats**.

**Q1.** What kind of threat is described when a threat actor sends you a virus that can reformat your hard drive?  
✅ **Answer:** **Data loss or manipulation**

**Q2.** What kind of threat is described when a threat actor makes illegal online purchases using stolen credit information?  
✅ **Answer:** **Identity theft**

**Q3.** What kind of threat is described when a threat actor prevents legal users from accessing data services?  
✅ **Answer:** **Disruption of service**

**Q4.** What kind of threat is described when a threat actor steals scientific research data?  
✅ **Answer:** **Information theft**

**Q5.** What kind of threat is described when a threat actor overloads a network to deny other users network access?  
✅ **Answer:** **Disruption of service**

**Q6.** What kind of threat is described when a threat actor alters data records?  
✅ **Answer:** **Data loss or manipulation**

**Q7.** What kind of threat is described when a threat actor is stealing the user database of a company?  
✅ **Answer:** **Information theft**

> **Note:** The prints show Q1–Q8 navigation, but only Q1–Q7 were provided here. Send Q8 and I’ll add it in the same format.

---

## 16.2 Network Attacks

This section goes deeper into **how** threat actors gain access to networks or stop authorised users from getting access.

### 16.2.1 Types of Malware

**Malware** = *malicious software*. It is software/code specifically designed to **damage, disrupt, steal**, or perform other “bad” / illegitimate actions against data, hosts, or networks.

Three malware categories highlighted here are: **viruses**, **worms**, and **Trojan horses**.

#### Viruses

A **computer virus** spreads by inserting a copy of itself into (and becoming part of) another program.

Key points from the module:
- It can spread from computer to computer, leaving infections behind.
- Viruses range from mildly annoying to serious damage (including data/software damage and even DoS conditions).
- Most viruses are attached to an **executable file**, meaning:
  - the virus may exist on the system but is not “active” and cannot spread until a user runs/opens the malicious host file/program.
- When the host code runs, the viral code runs too.
- Usually the host program still functions after infection, but some viruses overwrite other programs with copies of themselves, destroying the original host program.
- Viruses can spread when infected software/documents are transferred by:
  - the network,
  - a disk,
  - file sharing,
  - or infected email attachments.

#### Worms

A **worm** is similar to a virus in that it replicates and can cause similar damage, but the big difference is how it spreads:

- Worms are **standalone** software.
- Unlike viruses (which need an infected host file), worms do **not** require a host program or human help to propagate.
- A worm does not need to attach to a program to infect a host; it can enter through a **vulnerability** in the system.
- Worms take advantage of system features to travel through the network **unaided**.

#### Trojan horses

A **Trojan horse** looks legitimate but is harmful—named after the wooden horse story used to infiltrate Troy.

Key points from the module:
- Users are usually tricked into loading and executing it.
- Once active, it can do many kinds of harm (examples given):
  - annoy the user (excessive pop-up windows),
  - change the desktop,
  - damage the host (delete files, steal data),
  - activate and spread other malware (including viruses).
- Trojans are also commonly used to create **back doors** that give attackers access to the system.
- Unlike viruses and worms, Trojans do **not** reproduce by infecting other files.
- They spread mainly via **user interaction**, such as opening an email attachment or downloading and running a file from the internet.

---

### 16.2.2 Reconnaissance Attacks

Networks can be hit by multiple types of network attacks. The module groups them into three big categories:

- **Reconnaissance attacks** — discovering and mapping systems, services, or vulnerabilities  
- **Access attacks** — unauthorised manipulation of data, system access, or user privileges  
- **Denial of service** — disabling or corrupting networks, systems, or services  

Reconnaissance is often about gathering information first:

- Threat actors can use internet tools like **nslookup** and **whois** to determine the IP address space assigned to an organisation.
- After identifying the address space, a threat actor can ping the public IPs to see which addresses are active.
- To automate discovery, the module mentions using a **ping sweep** tool such as **fping** or **gping**.
- A ping sweep systematically pings all network addresses in a given range/subnet—like calling every number in a phonebook to see who answers.

Recon tools highlighted in the interactive content:

#### Internet queries
The threat actor looks for initial information about a target using tools such as:
- Google search,
- organisation websites,
- whois,
- and similar public sources.

#### Ping sweeps
The threat actor runs a ping sweep to determine which IP addresses are active.

#### Port scans
After discovering active IPs, the threat actor performs a port scan on those addresses.

---

### 16.2.3 Access Attacks

Access attacks exploit known weaknesses in services (examples listed):
- authentication services,
- FTP services,
- web services,

to gain entry to:
- web accounts,
- confidential databases,
- other sensitive information.

In short: they allow unauthorised access to information a user has **no right** to view.

The module classifies access attacks into four types:

#### Password attacks
Methods mentioned:
- **brute-force attacks**
- **Trojan horse attacks**
- **packet sniffers**

#### Trust exploitation
In a trust exploitation attack, the threat actor leverages unauthorised privileges to gain access—often by abusing trust relationships.

Scenario described:
- **System A trusts System B**
- **System B trusts everyone**
- The attacker wants access to System A, so they compromise System B first, then use System B to attack System A.

#### Port redirection
In port redirection, a compromised system is used as a base for attacks against other targets.

Example described:
- Attacker uses **SSH (port 22)** to connect to compromised Host A.
- Because Host A is trusted by Host B, the attacker can then use **Telnet (port 23)** to access Host B.

#### Man-in-the-middle
A man-in-the-middle (MitM) attack places the threat actor between two legitimate entities so they can read or modify data in transit.

Steps shown:
1. Victim requests a web page; the request is directed to the threat actor’s computer.
2. The threat actor receives the request and retrieves the real page from the legitimate website.
3. The threat actor can modify the page and change the data.
4. The threat actor forwards the requested (possibly modified) page to the victim.

---

## 16.2.4 Denial of Service Attacks

Denial of service (**DoS**) attacks are one of the most well‑known (and widely reported) attack types, and they’re often difficult to fully eliminate. Because they’re usually easy to launch and can cause major damage, security admins should treat DoS as a high‑priority risk.

At a high level, DoS attacks aim to **stop legitimate users from using a service** by **consuming system resources** (CPU, memory, bandwidth, sessions, etc.). One practical mitigation theme is to **stay current on security updates** for operating systems and applications.

> In NetAcad’s animation, you can switch between examples of **DoS** and **distributed DoS (DDoS)** attacks.

### DoS attack (single source)
A DoS attack is a major risk because it can **interrupt communication** and lead to significant **loss of time and money**. A key point: many DoS attacks are **relatively simple to perform**, even for an unskilled threat actor.

### DDoS attack (multiple coordinated sources)
A **DDoS** attack is like DoS, but it comes from **many coordinated sources** at the same time. A common example is when a threat actor builds a network of infected hosts (often called **zombies**).  
A group of zombies is a **botnet**, and the attacker uses a **command and control (CnC)** program to direct the botnet to launch the DDoS.

---

## 16.2.5 Check Your Understanding – Network Attacks

### Question 1
**Scenario:** ACME Inc.’s web server becomes extremely slow. Investigation shows a computer on the internet is sending a huge number of malformed web requests to the server.  
**What type of attack is this?**

- Denial of service (DoS) attack ✅
- Reconnaissance attack  
- Access attack  
- Malware attack  

**Answer:** **Denial of service (DoS) attack**  
**Why:** Flooding a service with traffic/requests to degrade performance and prevent normal use is the classic DoS goal (resource exhaustion).

### Question 2
**Scenario:** George runs a simple FTP server on his workstation to share a large video. He creates an account with the weak password **“file”** and gives it to a coworker. By Monday, the workstation is compromised and is attempting to upload work documents to the internet.  
**What type of attack is this?**

- Malware attack  
- Access attack ✅
- Reconnaissance attack  
- Denial of service (DoS) attack  

**Answer:** **Access attack**  
**Why:** The entry point is a poorly secured authentication setup (weak password on an exposed service), enabling unauthorized access and misuse.

### Question 3
**Scenario:** Jeremiah downloads and runs a “free program” offered by a random website. After it runs, the OS crashes, key OS files are corrupted, and the PC requires a full disk format and OS reinstall.  
**What type of attack is this?**

- Access attack  
- Malware attack ✅
- Reconnaissance attack  
- Denial of service (DoS) attack  

**Answer:** **Malware attack**  
**Why:** A malicious program caused direct system damage/corruption—typical malware behavior.

### Question 4
**Scenario:** Arianna finds a USB flash drive in a mall parking lot, plugs it into her laptop, opens some photos, and later notices her laptop camera is active.  
**What type of attack is this?**

- Access attack  
- Reconnaissance attack  
- Denial of service (DoS) attack  
- Malware attack ✅  

**Answer:** **Malware attack**  
**Why:** “Found USB” is a common delivery method for malicious code (e.g., trojan/spyware) that can enable unauthorized actions like camera access.

### Question 5
**Scenario:** An ACME print server hasn’t received security updates for 60+ days. It’s now running slowly and sending many malicious packets from its NIC.  
**What type of attack is this?**

- Access attack  
- Reconnaissance attack  
- Denial of service (DoS) attack  
- Malware attack ✅  

**Answer:** **Malware attack**  
**Why:** An unpatched system is a common compromise path. A host that begins generating malicious traffic often indicates infection (e.g., being used as part of a botnet).

### Question 6
**Scenario:** Firewall logs show suspicious traffic: several internet IPs are sending malformed packets to multiple different internal IP addresses, using many random port numbers inside ACME Inc.  
**What type of attack is this?**

- Denial of service (DoS) attack  
- Reconnaissance attack ✅
- Malware attack  
- Access attack  

**Answer:** **Reconnaissance attack**  
**Why:** Probing many targets/ports looks like scanning and mapping—typical recon activity (e.g., port scanning).

---

## 16.2.6 Lab – Research Network Security Threats

### Objectives
- **Part 1:** Explore the **SANS** website  
- **Part 2:** Identify recent network security threats  
- **Part 3:** Research and describe one specific network security threat/attack  

### Background / Scenario
To defend a network, an administrator needs to identify **external threats** that could endanger it. Security‑focused websites help you spot emerging threats and learn mitigation options.

One widely used and trusted resource is **SANS** (*SysAdmin, Audit, Network, Security*). SANS provides resources like:
- a list of the **Top 20 Critical Security Controls for Effective Cyber Defense**
- the weekly **@Risk: The Consensus Security Alert** newsletter (covers new attacks and vulnerabilities)

In this lab you will explore the SANS site, use it to identify recent security threats, compare with other sites that track threats, and then research + present details of one specific network attack.

### Required Resources
- A device with internet access  
- A presentation computer with PowerPoint (or similar presentation software) installed  

### Instructions

#### Part 1: Exploring the SANS Website
In Part 1, you’ll navigate to SANS and review what resources are available.

**Step 1: Locate SANS resources**
- Search the internet for **SANS**.
- On the SANS home page, click **FREE Resources**.

**Question:** List three available resources.  
**Type your answers here.**

**Step 2: Find the CIS Critical Security Controls link**
The CIS Critical Security Controls linked on SANS come from a public‑private partnership involving the **Department of Defense (DoD)**, **National Security Agency (NSA)**, **Center for Internet Security (CIS)**, and the **SANS Institute**. They were created to **prioritize cybersecurity controls and spending for the DoD**, and they have become a key foundation for U.S. government security programs.

From the Resources menu, select **Critical Security Controls** (or similar). The CIS Controls document is hosted on the **CIS** website and requires **free registration** to access. On the SANS CIS Controls page, there’s also a link to download the **2014 SANS Critical Security Controls Poster**, which briefly describes each control.

**Question:** Pick one Control and list implementation suggestions for that Control.  
**Type your answers here.**

**Step 3: Locate the Newsletters menu**
- Highlight the Resources menu and select **Newsletters**.

**Question:** Briefly describe each of the three newsletters available.  
**Type your answers here.**

#### Part 2: Identify Recent Network Security Threats
In Part 2, you’ll use SANS to find recent issues and then compare with other threat‑tracking websites.

**Step 1: Use the @Risk newsletter archive**
- From the Newsletters page, choose **Archive** for **@RISK: The Consensus Security Alert**.
- Scroll to **Archives Volumes** and open a recent weekly newsletter.
- Review the **Notable Recent Security Issues** and **Most Popular Malware Files** sections.

**Question:** List some recent vulnerabilities (check multiple newsletters if needed).  
**Type your answers here.**

**Step 2: Identify other security‑threat websites**
**Questions:**
- Besides SANS, identify other websites that provide recent security threat information.  
  **Type your answers here.**
- List some recent security threats described on those websites.  
  **Type your answers here.**

#### Part 3: Detail a Specific Network Security Attack
In Part 3, choose one real attack, research it, and create a presentation.

**Step 1: Complete the form below for your selected network attack**

- **Name of attack:**  
  _blank_
- **Type of attack:**  
  _blank_
- **Dates of attacks:**  
  _blank_
- **Computers / Organizations affected:**  
  _blank_
- **How it works and what it did:**  
  _blank_
- **Mitigation options:**  
  _blank_
- **References and info links:**  
  _blank_

**Step 2:** Follow your instructor’s guidelines to complete the presentation.

### Reflection Questions
1. What steps can you take to protect your own computer?  
   **Type your answers here.**

2. What are some important steps that organizations can take to protect their resources?  
   **Type your answers here.**

---

## What’s next
Continue with **16.3 Network Attack Mitigations**, starting at:
- 16.3.1 The Defense-in-Depth Approach
- 16.3.2 Keep Backups
- 16.3.3 Upgrade, Update, and Patch


