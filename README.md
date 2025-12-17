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
# 16.3 Network Attack Mitigation

## 16.3.1 The Defense-in-Depth Approach
To reduce the risk of network attacks, you first secure the infrastructure devices (routers, switches, servers, and hosts). Most organizations use a **defense-in-depth** (layered) security model, where multiple security devices and services work together to protect users and assets from TCP/IP threats.

In a layered design, devices are also **hardened** (secured) to prevent threat actors from accessing or tampering with them.

**Example security components in a layered network:**
- **VPN** — Provides secure remote access and site-to-site connections using encrypted tunnels.
- **ASA Firewall** — A dedicated stateful firewall that allows inside users to initiate connections out (and receive the returning traffic), while blocking unsolicited inbound connections from the outside.
- **IPS (Intrusion Prevention System)** — Inspects inbound/outbound traffic for malware, attack signatures, and other threats; can stop recognized threats immediately.
- **ESA/WSA** — Email Security Appliance filters spam/suspicious email; Web Security Appliance filters known/suspicious internet malware sites.
- **AAA Server** — Stores who is authorized to access/manage network devices; network devices authenticate administrative users against this database.

---

## 16.3.2 Keep Backups
Backing up device configurations and data is one of the best protections against **data loss**. A backup is a copy stored on removable media or another system so you can restore data/configurations after failures (including hardware failure). Infrastructure devices should have backups of configuration files and IOS images (e.g., on an FTP or similar server). Backups are typically stored **offsite** to protect them if something happens to the main location. Windows hosts also include backup/restore tools, and users should back up to another drive or to cloud storage.

### Backup considerations

| Consideration | Description |
|---|---|
| **Frequency** | - Perform backups regularly as defined by the security policy.  
- Full backups take time, so do monthly/weekly full backups plus frequent partial backups of changed files. |
| **Validation** | - Always validate backups to confirm data integrity and verify restore procedures. |
| **Storage** | - Move backups to an approved **offsite** location on a daily/weekly/monthly rotation as required by policy. |
| **Security** | - Protect backups with strong passwords (needed to restore the data). |

---

## 16.3.3 Upgrade, Update, and Patch
Staying current with security updates improves your defense as new malware and vulnerabilities appear. A very effective way to reduce worm/malware impact is to:
- Download security updates from OS/application vendors
- Patch all vulnerable systems

In organizations, admins often maintain a **standard software image** (OS + approved apps) for new or upgraded systems. Requirements change, so already-deployed systems must also receive updated patches.

A common approach is enabling **automatic updates** so endpoints download and install security patches without user intervention (example shown with Windows Update).

---

## 16.3.4 Authentication, Authorization, and Accounting
Network devices should be configured so only authorized individuals can access them. **AAA** (“triple A”) is the main framework for controlling administrative access:

- **Authentication** — *Who are you?*
- **Authorization** — *What are you allowed to do? / What limits apply?*
- **Accounting** — *What did you do while you were in the system?* (logging/records)

A simple analogy is a credit card:
- Authentication = identifies the cardholder  
- Authorization = spending limit/permissions  
- Accounting = statement showing what was spent, where, and when  

---

## 16.3.5 Firewalls
A **firewall** is one of the most effective tools for stopping external threats. It sits between networks and controls traffic between them to help prevent unauthorized access.

Core behavior:
- Inside users can typically initiate connections to the internet and receive return traffic.
- Unsolicited traffic initiated from the outside is denied access to inside resources.

A firewall can also allow controlled access to specific services hosted for external users. Those public-facing servers are often placed in a **DMZ (demilitarized zone)**, allowing tighter, separate security policies for that segment.

---

## 16.3.6 Types of Firewalls
Common firewall techniques include:
- **Packet filtering** — Allow/deny traffic based on IP or MAC addresses.
- **Application filtering** — Allow/deny based on application type (often using port numbers).
- **URL filtering** — Allow/deny access to websites using specific URLs or keywords.
- **Stateful Packet Inspection (SPI)** — Ensures inbound traffic is part of legitimate responses to internal requests; can also recognize/filter certain attack types (e.g., DoS-related patterns).

---

## 16.3.7 Endpoint Security
An **endpoint (host)** is a device that acts as a network client (laptops, desktops, servers, smartphones, tablets). Endpoint security is challenging because it heavily depends on user behavior.

Good endpoint security requires:
- Clear, well-documented security policies
- Employee/user training on safe network usage
- Protective tools such as antivirus and host intrusion prevention
- More complete endpoint security often relies on **network access control** solutions

---

## 16.3.8 Check Your Understanding — Network Attack Mitigation

### Question 1
**Which device controls traffic between two or more networks to help prevent unauthorized access?**

- AAA Server  
- **Firewall** ✅  
- IPS  
- ESA/WSA  

### Question 2
**Which device is used by other network devices to authenticate and authorize management access?**

- IPS  
- Firewall  
- **AAA Server** ✅  
- ESA/WSA  


# Module 16 — Network Security Fundamentals (Part 6)

## 16.3.8 Check Your Understanding — Network Attack Mitigation

### Question 3
**Which backup policy consideration is concerned with using strong passwords to protect the backups and for restoring data?**

- Validation  
- **Security**  
- Storage  
- Frequency  

✅ **Answer:** Security

### Question 4
**This zone is used to house servers that should be accessible to outside users.**

- Inside  
- Outside  
- **DMZ**  
- Internet  

✅ **Answer:** DMZ

### Question 5
**Which is appropriate for providing endpoint security?**

- An ESA/WSA  
- **Antivirus software**  
- A server-based firewall  
- A AAA server  

✅ **Answer:** Antivirus software


## 16.4 Device Security

### 16.4.1 Cisco AutoSecure
One area of networks that requires special attention to maintain security is the devices. You probably already have a password for your computer, smart phone, or tablet. Is it as strong as it could be? Are you using other tools to enhance the security of your devices? This topic tells you how.

The security settings are set to the default values when a new operating system is installed on a device. In most cases, this level of security is inadequate. For Cisco routers, the Cisco **AutoSecure** feature can be used to assist securing the system, as shown in the example.

```text
Router# auto secure
      --- AutoSecure Configuration ---
*** AutoSecure configuration enhances the security of
the router but it will not make router absolutely secure
from all security attacks ***
```

In addition, there are some simple steps that should be taken that apply to most operating systems:
- Default usernames and passwords should be changed immediately.
- Access to system resources should be restricted to only the individuals that are authorized to use those resources.
- All unnecessary services and applications should be turned off and uninstalled when possible.

Often, devices shipped from the manufacturer have been sitting in a warehouse for a period of time and do not have the most up-to-date patches installed. It is important to update any software and install any security patches prior to implementation.


### 16.4.2 Passwords
To protect network devices, it is important to use strong passwords. Here are standard guidelines to follow:
- Use a password length of at least eight characters, preferably 10 or more characters. A longer password is a more secure password.
- Make passwords complex. Include a mix of uppercase and lowercase letters, numbers, symbols, and spaces, if allowed.
- Avoid passwords based on repetition, common dictionary words, letter or number sequences, usernames, relative or pet names, biographical information, such as birthdays, ID numbers, ancestor names, or other easily identifiable pieces of information.
- Deliberately misspell a password. For example, Smith = Smyth = 5myth or Security = 5ecur1ty.
- Change passwords often. If a password is unknowingly compromised, the window of opportunity for the threat actor to use the password is limited.
- Do not write passwords down and leave them in obvious places such as on the desk or monitor.

The tables show examples of strong and weak passwords.

**Weak Passwords**

| Weak Password | Why it is Weak |
|---|---|
| `secret` | Simple dictionary password |
| `smith` | Maiden name of mother |
| `toyota` | Make of a car |
| `bob1967` | Name and birthday of the user |
| `Blueleaf23` | Simple words and numbers |

**Strong Passwords**

| Strong Password | Why it is Strong |
|---|---|
| `b67n42d39c` | Combines alphanumeric characters |
| `12^h u4@1p7` | Combines alphanumeric characters, symbols, and includes a space |

On Cisco routers, leading spaces are ignored for passwords, but spaces after the first character are not. Therefore, one method to create a strong password is to use the space bar and create a phrase made of many words. This is called a **passphrase**. A passphrase is often easier to remember than a simple password. It is also longer and harder to guess.


### 16.4.3 Additional Password Security
Strong passwords are only useful if they are secret. There are several steps that can be taken to help ensure that passwords remain secret on a Cisco router and switch including these:
- Encrypting all plaintext passwords
- Setting a minimum acceptable password length
- Deterring brute-force password guessing attacks
- Disabling an inactive privileged EXEC mode access after a specified amount of time.

As shown in the sample configuration in the figure, the **service password-encryption** global configuration command prevents unauthorized individuals from viewing plaintext passwords in the configuration file. This command encrypts all plaintext passwords. Notice in the example, that the password “cisco” has been encrypted as “03095A0F034F”.

To ensure that all configured passwords are a minimum of a specified length, use the **security passwords min-length _length_** command in global configuration mode. In the figure, any new password configured would have to have a minimum length of eight characters.

Threat actors may use password cracking software to conduct a brute-force attack on a network device. This attack continuously attempts to guess the valid passwords until one works. Use the **login block-for _#_ attempts _#_ within _#_** global configuration command to deter this type of attack. In the figure for example, the **login block-for 120 attempts 3 within 60** command will block vty login attempts for 120 seconds if there are three failed login attempts within 60 seconds.

Network administrators can become distracted and accidently leave a privileged EXEC mode session open on a terminal. This could enable an internal threat actor access to change or erase the device configuration.

By default, Cisco routers will logout an EXEC session after 10 minutes of inactivity. However, you can reduce this setting using the **exec-timeout _minutes seconds_** line configuration command. This command can be applied on line console, auxiliary, and vty lines. In the figure, we are telling the Cisco device to automatically disconnect an inactive user on a vty line after the user has been idle for 5 minutes and 30 seconds.

```text
R1(config)# service password-encryption
R1(config)# security passwords min-length 8
R1(config)# login block-for 120 attempts 3 within 60
R1(config)# line vty 0 4
R1(config-line)# password cisco123
R1(config-line)# exec-timeout 5 30
R1(config-line)# transport input ssh
R1(config-line)# end
R1#
R1# show running-config | section line vty
line vty 0 4
 password 7 094F471A1A0A
 exec-timeout 5 30
 login
 transport input ssh
R1#
```


### 16.4.4 Enable SSH
Telnet simplifies remote device access, but it is not secure. Data contained within a telnet packet is transmitted unencrypted. For this reason, it is highly recommended to enable Secure Shell (SSH) on devices for secure remote access.

It is possible to configure a Cisco device to support SSH using the following six steps:

**Step 1.** Configure a unique device hostname. A device must have a unique hostname other than the default.  
**Step 2.** Configure the IP domain name. Configure the IP domain name of the network by using the global configuration mode command **ip domain name _name_**.  
**Step 3.** Generate a key to encrypt SSH traffic. SSH encrypts traffic between source and destination. However, to do so, a unique authentication key must be generated by using the global configuration command **crypto key generate rsa general-keys modulus _bits_**. The modulus bits determines the size of the key and can be configured from 360 bits to 2048 bits. The larger the bit value, the more secure the key. However, larger bit values also take longer to encrypt and decrypt information. The minimum recommended modulus length is **1024 bits**.  
**Step 4.** Verify or create a local database entry. Create a local database username entry using the **username** global configuration command. In the example, the parameter **secret** is used so that the password will be encrypted using MD5.  
**Step 5.** Authenticate against the local database. Use the **login local** line configuration command to authenticate the vty line against the local database.  
**Step 6.** Enable vty inbound SSH sessions. By default, no input session is allowed on vty lines. You can specify multiple input protocols including Telnet and SSH using the **transport input {ssh | telnet}** command.

As shown in the example, router R1 is configured in the **span.com** domain. This information is used along with the bit value specified in the **crypto key generate rsa general-keys modulus** command to create an encryption key.

Next, a local database entry for a user named Bob is created. Finally, the vty lines are configured to authenticate against the local database and to only accept incoming SSH sessions.

```text
Router# configure terminal
Router(config)# hostname R1
R1(config)# ip domain name span.com
R1(config)# crypto key generate rsa general-keys modulus 1024
The name for the keys will be: R1.span.com % The key modulus size is 1024 bits
% Generating 1024 bit RSA keys, keys will be non-exportable...[OK]
Dec 13 16:19:12.079: %SSH-5-ENABLED: SSH 1.99 has been enabled
R1(config)#

R1(config)# username Bob secret cisco
R1(config)# line vty 0 4
R1(config-line)# login local
R1(config-line)# transport input ssh
R1(config-line)# exit
R1(config)#
```


### 16.4.5 Disable Unused Services
Cisco routers and switches start with a list of active services that may or may not be required in your network. Disable any unused services to preserve system resources, such as CPU cycles and RAM, and prevent threat actors from exploiting these services. The type of services that are on by default will vary depending on the IOS version. For example, IOS-XE typically will have only HTTPS and DHCP ports open. You can verify this with the **show ip ports all** command, as shown in the example.

```text
Router# show ip ports all

Proto Local Address           Foreign Address          State        PID/Program Name
TCP
      Local Address           Foreign Address          (state)
tcp   :::443                  :::*                     LISTEN       309/[IOS]HTTP CORE
tcp   :::443                  *:*                      LISTEN       309/[IOS]HTTP CORE
udp   *:67                     0.0.0.0:0                            387/[IOS]DHCPD Receive

Router#
```

IOS versions prior to IOS-XE use the **show control-plane host open-ports** command. We mention this command because you may see it on older devices. The output is similar. However, notice that this older router has an insecure HTTP server and Telnet running. Both of these services should be disabled. As shown in the example, disable HTTP with the **no ip http server** global configuration command. Disable Telnet by specifying only SSH in the line configuration command, **transport input ssh**.

```text
Router# show control-plane host open-ports
Active internet connections (servers and established)
Prot  Local Address   Foreign Address  Service       State
tcp   *:23            *:0              Telnet        LISTEN
tcp   *:80            *:0              HTTP CORE     LISTEN
udp   *:67            *:0              DHCPD Receive LISTEN

Router# configure terminal
Router(config)# no ip http server
Router(config)# line vty 0 15
Router(config-line)# transport input ssh
```

---

# Module 16 — Part 7: 16.4.6 to 16.5.1 (Device Security + Practice)

> Covers only the items shown in your screenshots: **16.4.6**, **16.4.7**, **16.5**, and **16.5.1**.

---

## 16.4.6 Packet Tracer — Configure Secure Passwords and SSH

### Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| RTA | G0/0 | 172.16.1.1 | 255.255.255.0 | N/A |
| PCA | NIC | 172.16.1.10 | 255.255.255.0 | 172.16.1.1 |
| SW1 | VLAN 1 | 172.16.1.2 | 255.255.255.0 | 172.16.1.1 |

### Scenario (what you’re doing)

You’re asked to prep **RTA** (router) and **SW1** (switch) so they’re ready for deployment. Before connecting them to the network, you must enable baseline security (strong passwords + SSH).

### Step 1 — Configure basic security on the router (RTA)

1. **Configure PCA IPv4 settings** using the addressing table.
2. From PCA, **console into RTA** (Terminal app).
3. Set **hostname**:
   - `hostname RTA`
4. Configure **interface IP + enable it** (use the values from the table).
5. **Encrypt plaintext passwords**:
   - `service password-encryption`
6. Enforce **minimum password length**:
   - `security password min-length 10`
7. Configure a **strong enable secret** (pick one you will remember).
8. Disable DNS lookup (prevents delays when commands are mistyped):
   - `no ip domain-lookup`
9. Set the **domain name** *(case-sensitive in PT scoring)*:
   - `ip domain-name CCNA.com`
10. Create a **local user** with an encrypted secret:
    - `username <any_user> secret <any_password>`
11. Generate **RSA keys (1024-bit)**:
    - `crypto key generate rsa`
    - When asked for the modulus, enter: `1024`
12. Enable brute-force protection:
    - Block logins for **180 seconds** if there are **4 failures within 120 seconds**:
      - `login block-for 180 attempts 4 within 120`
13. Configure **VTY 0–4** for **SSH-only** + local login:
    - `line vty 0 4`
    - `transport input ssh`
    - `login local`
14. Set VTY **EXEC timeout** to **6 minutes**:
    - `exec-timeout 6`
15. Save to NVRAM:
    - `copy running-config startup-config`
16. From PCA, test SSH help and then SSH into RTA:
    - `ssh /?`
    - `SSH -l <username> <target>`

### Step 2 — Configure basic security on the switch (SW1)

1. Open **SW1 → CLI**.
2. Set **hostname**:
   - `hostname SW1`
3. Configure **VLAN 1** management IP + enable it (per addressing table).
4. Configure the **default gateway**:
   - `ip default-gateway 172.16.1.1`
5. **Shut down unused ports** (bulk method using *interface range*).  
   On SW1, shut down everything except **F0/1** and **G0/1**:
   - `interface range f0/2-24, g0/2`
   - `shutdown`
6. Encrypt plaintext passwords:
   - `service password-encryption`
7. Configure a strong **enable secret** (choose your own).
8. Disable DNS lookup:
   - `no ip domain-lookup`
9. Set the **domain name** *(case-sensitive in PT scoring)*:
   - `ip domain-name CCNA.com`
10. Create a local user with an encrypted secret:
    - `username <any_user> secret <any_password>`
11. Generate **RSA keys (1024-bit)**:
    - `crypto key generate rsa` → modulus `1024`
12. Configure **VTY lines** for **SSH-only** + local login:
    - `line vty 0 4`
    - `transport input ssh`
    - `login local`
13. Set **EXEC timeout** to **6 minutes** on VTY lines:
    - `exec-timeout 6`
14. Save to NVRAM:
    - `copy running-config startup-config`

**Files (as provided):**
- `16.4.6-packet-tracer---configure-secure-passwords-and-ssh.pka`
- `16.4.6-packet-tracer---configure-secure-passwords-and-ssh.pdf`

---

## 16.4.7 Lab — Configure Network Devices with SSH

### Topology + Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---:|---:|---:|
| R1 | G0/0/1 | 192.168.1.1 | 255.255.255.0 | N/A |
| S1 | VLAN 1 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |
| PC-A | NIC | 192.168.1.3 | 255.255.255.0 | 192.168.1.1 |

### Objectives

- **Part 1:** Configure basic device settings  
- **Part 2:** Configure the router for SSH access  
- **Part 3:** Configure the switch for SSH access  
- **Part 4:** SSH from the CLI on the Switch

### Background / Scenario (why SSH)

Telnet does not encrypt traffic, so credentials/configs can be captured. **SSH** encrypts the session and provides device authentication, so it is preferred for remote administration.

### Required resources (typical)

- 1 router (ex: Cisco 4221 w/ IOS XE 16.9.x or similar)
- 1 switch (ex: Catalyst 2960 w/ IOS 15.2(2) or similar)
- 1 Windows PC with terminal software (ex: **Tera Term**)
- Console + Ethernet cabling

---

### Part 1 — Configure basic device settings

#### Step 1: Cable the network
- Cable devices as shown in the topology.

#### Step 2: Initialize and reload
- Ensure the router and switch are erased (no startup config), then reload.

#### Step 3: Configure the router
From console on **R1**:

- Disable DNS lookup:
  - `no ip domain-lookup`
- Set privileged EXEC encrypted password to **class**
- Set console password to **cisco** and require login
- Set VTY password to **cisco** and require login
- Encrypt plaintext passwords:
  - `service password-encryption`
- Configure a warning banner (MOTD) about unauthorized access
- Configure and enable **G0/0/1** with `192.168.1.1/24`
- Save configuration:
  - `copy running-config startup-config`

#### Step 4: Configure PC-A
- Set IP/mask to match the addressing table.
- Set the default gateway to `192.168.1.1`.

#### Step 5: Verify connectivity
- From PC-A: `ping 192.168.1.1`

---

### Part 2 — Configure the router for SSH access

#### What SSH needs (in Packet Tracer + IOS)
- A hostname and domain name (used when generating keys)
- RSA keys
- A local username/secret
- VTY lines configured to accept SSH and authenticate with the local database

#### Minimum required settings for this lab
- Local user: `admin` / `Adm1nP@55`
- Enable SSH on VTY lines (permit **Telnet + SSH** if the lab says so)
- Use `login local` on the VTY lines
- Save config

#### Test SSH from PC-A
- Use Tera Term to SSH to `192.168.1.1`
- Login with `admin` / `Adm1nP@55`

---

### Part 3 — Configure the switch for SSH access

#### Step 1: Basic settings on S1
- `no ip domain-lookup`
- Privileged EXEC password: **class**
- Console password: **cisco** + `login`
- VTY password: **cisco** + `login`
- `service password-encryption`
- MOTD banner
- VLAN 1 SVI: `192.168.1.11/24`
- Default gateway: `192.168.1.1`
- Save config

#### Step 2: Enable SSH on S1 (same idea as R1)
- Set hostname + domain name
- Generate RSA keys
- Create local user `admin` / `Adm1nP@55`
- Configure VTY lines for SSH (and Telnet if required) + `login local`

#### Quick test
- SSH from PC-A to `192.168.1.11`

**Question (lab):** Are you able to establish an SSH session with the switch?  
> Write your answer here.

---

### Part 4 — SSH from the switch CLI

- View available SSH parameters:
  - `ssh ?`
- SSH from **S1 → R1**:
  - `ssh -l admin 192.168.1.1`

**Question (lab):** What versions of SSH are supported from the CLI?  
> Write your answer here.

**Reflection question:** How would you give multiple users (each with their own username) access to a network device?  
> Write your answer here.

**File (as provided):**
- `16.4.7-lab---configure-network-devices-with-ssh.pdf`

---

## 16.5 Module Practice and Quiz

This section starts the **Module Practice and Quiz** area.

---

## 16.5.1 Packet Tracer — Secure Network Devices

### Addressing Table (fill the blanks)

| Device | Interface | Address | Mask | Gateway |
|---|---|---:|---:|---:|
| RTR-A | G0/0/0 | 192.168.1.1 | 255.255.255.0 | N/A |
| RTR-A | G0/0/1 | 192.168.2.1 | 255.255.255.0 | N/A |
| SW-1 | SVI | 192.168.1.254 | 255.255.255.0 | **_____** |
| PC | NIC | 192.168.1.2 | 255.255.255.0 | **_____** |
| Laptop | NIC | 192.168.1.10 | 255.255.255.0 | **_____** |
| Remote PC | NIC | 192.168.2.10 | 255.255.255.0 | **_____** |

### Step 1 — Document the network
- Complete the missing **Gateway** fields in the addressing table.

### Step 2 — Router configuration requirements (RTR-A)

- Disable DNS lookup.
- Configure hostname.
- Set minimum password length: **10**.
- Console password (10 chars): `@Cons1234!`
- Console + VTY idle timeout: **7 minutes**.
- Enable secret: encrypted (allowed to match activity requirements).
- MOTD banner warning.
- `service password-encryption`
- Local user: `NETadmin` / `LogAdmin!9`
- SSH domain name: `security.com`
- RSA modulus: `1024`
- VTY lines: **SSH-only** + `login local`
- Login block: **45 seconds** if **3 failures within 100 seconds**.

### Step 3 — Switch configuration requirements (SW-1)

- Shut down unused ports.
- Configure SVI management + default gateway so it can be managed and reachable.
- Enable secret: `@Cons1234!`
- Enable SSH similarly to the router.
- Local user: `NETadmin` / `LogAdmin!9`
- VTY lines: **SSH-only**, using local authentication and restricted to the admin account per the activity.
- Hosts on both LANs should successfully **ping** the switch management interface.

**Files (as provided):**
- `16.5.1-packet-tracer---secure-network-devices.pka`
- `16.5.1-packet-tracer---secure-network-devices.pdf`


---

# Module 16 — Network Security Fundamentals
> **This file covers only:** 16.5.2, 16.5.3, and 16.5.4 (Q1–Q6)

## 16.5.2 Lab — Secure Network Devices
### Objectives
- Part 1: Configure basic device settings
- Part 2: Configure basic security measures on the router
- Part 3: Verify that your security measures have been implemented correctly
- Part 4: Configure basic security measures on the switch

### Addressing Table
| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---:|---:|---:|
| R1 | G0/0/1 | 192.168.1.1 | 255.255.255.0 | N/A |
| S1 | VLAN 1 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |
| PC-A | NIC | 192.168.1.3 | 255.255.255.0 | 192.168.1.1 |

---
## Part 1 — Configure Basic Device Settings
### Step 1 — Cable the network
- Cable the devices according to the lab topology.

### Step 2 — Initialize and reload
- Initialize and reload the router and switch (erase startup config / reload) so you start from a clean state.

### Step 3 — Configure router and switch
#### Configure PC-A
- Set IPv4 settings on **PC-A** according to the Addressing Table.

#### Configure R1 (basic configuration)
```text
enable
configure terminal
no ip domain-lookup
hostname R1

enable secret cisco

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 15
 password cisco
 login
 exit

banner motd $ Unauthorized access is strictly prohibited. $

interface g0/0/1
 ip address 192.168.1.1 255.255.255.0
 no shutdown
exit
end
copy running-config startup-config
```

#### Configure S1 (basic configuration)
```text
enable
configure terminal
hostname S1

enable secret cisco

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 15
 password cisco
 login
 exit

banner motd $ Unauthorized access is strictly prohibited. $

interface vlan 1
 ip address 192.168.1.11 255.255.255.0
 no shutdown
exit
ip default-gateway 192.168.1.1
end
copy running-config startup-config
```

---
## Part 2 — Configure Basic Security Measures on the Router
### Step 1 — Encrypt clear-text passwords and upgrade to stronger passwords
```text
configure terminal
service password-encryption
security passwords min-length 12

enable secret $cisco!PRIV*

line console 0
 password $cisco!CON*
 login
 exit

line vty 0 15
 password $cisco!VTY*
 login
 exit
end
copy running-config startup-config
```

### Step 2 — Configure SSH-only remote access
Lab requirements:
- Username: `SSHadmin`
- Password (secret): `55HAdm!n2020`
- Domain name: `ccna-lab.com`
- RSA key modulus: `1024`

```text
configure terminal
username SSHadmin secret 55HAdm!n2020
ip domain-name ccna-lab.com
crypto key generate rsa general-keys modulus 1024
ip ssh version 2

line vty 0 15
 transport input ssh
 login local
 exit
end
copy running-config startup-config
```

### Step 3 — Console/VTY best practices
- Disconnect users after **5 minutes** of inactivity.
- Block vty logins for **2 minutes** if **3** failed logins happen within **1 minute**.

```text
configure terminal
login block-for 120 attempts 3 within 60

line console 0
 exec-timeout 5 0
 exit

line vty 0 15
 exec-timeout 5 0
 exit
end
copy running-config startup-config
```

---
## Part 3 — Verify that your security measures have been implemented correctly
### Step 1 — Verify unused ports are administratively down
```text
show ip interface brief
```
- Any unused interfaces that are **up** should be disabled with `shutdown`.

### Step 2 — Test Telnet vs SSH from PC-A
On **PC-A**, open a terminal emulator (ex: Tera Term):
- Confirm you can ping the devices:
  - `ping 192.168.1.1`
  - `ping 192.168.1.11`
- Try Telnet to `192.168.1.1` (expected: **blocked**, because VTY allows SSH only).
- SSH to R1 and log in using `SSHadmin`.

**Login-block test (as in the lab):** Intentionally mistype the username/password and observe what happens when you fail to log in repeatedly.

### Step 3 — Use `show login` during the quiet period
From the **router console**, run:
```text
show login
```
- Observe whether the router is currently blocking logins and how many seconds remain.

### Step 4 — Confirm banner and privileged access
- After the lockout timer expires, SSH to R1 again and note what message/banner is displayed.
- Enter privileged EXEC mode with:
  - `enable`
  - Password: `$cisco!PRIV*`
- Review the final security config:
```text
show running-config
```

---
## Part 4 — Configure Basic Security Measures on the Switch
### Step 1 — Apply switch security measures
```text
enable
configure terminal
service password-encryption
security passwords min-length 12

enable secret $cisco!PRIV*

line console 0
 password $cisco!CON*
 login
 exit

line vty 0 15
 password $cisco!VTY*
 login
 exit

username SSHadmin secret 55HAdm!n2020
ip domain-name ccna-lab.com
crypto key generate rsa general-keys modulus 1024
ip ssh version 2

line vty 0 15
 transport input ssh
 login local
 exec-timeout 5 0
 exit

login block-for 120 attempts 3 within 60

line console 0
 exec-timeout 5 0
 exit
end
copy running-config startup-config
```

### Step 2 — Verify all unused ports are disabled
```text
show ip interface brief
```
- Shut down unused ports (use `interface range` to do multiple at once).

Example:
```text
configure terminal
interface range fa0/1-4, fa0/7-24, gi0/1-2
 shutdown
end
copy running-config startup-config
```

### Step 3 — Verify switch security works
- SSH to the switch and intentionally mistype credentials to see if login access is blocked.
- After the 120 seconds expire, SSH again as `SSHadmin` / `55HAdm!n2020`.
- Confirm the banner appears and you can enter privileged EXEC mode using `$cisco!PRIV*`.
- Run `show running-config` to confirm your settings.

### Reflection Questions
1. The password `cisco` was used for console and VTY in Part 1. When is it used *after* best-practice security measures are applied?
   - **Answer:** It shouldn’t be used anymore (it’s replaced by the stronger line passwords and SSH/local authentication).

### Router Interface Summary Table (reference)
| Router Model | Ethernet Interface #1 | Ethernet Interface #2 | Serial Interface #1 | Serial Interface #2 |
|---|---|---|---|---|
| 1800 | Fast Ethernet 0/0 (F0/0) | Fast Ethernet 0/1 (F0/1) | Serial 0/0/0 (S0/0/0) | Serial 0/0/1 (S0/0/1) |
| 1900 | Gigabit Ethernet 0/0 (G0/0) | Gigabit Ethernet 0/1 (G0/1) | Serial 0/0/0 (S0/0/0) | Serial 0/0/1 (S0/0/1) |
| 2801 | Fast Ethernet 0/0 (F0/0) | Fast Ethernet 0/1 (F0/1) | Serial 0/0/0 (S0/0/0) | Serial 0/0/1 (S0/0/1) |
| 2811 | Fast Ethernet 0/0 (F0/0) | Fast Ethernet 0/1 (F0/1) | Serial 0/0/0 (S0/0/0) | Serial 0/0/1 (S0/0/1) |
| 2900 | Gigabit Ethernet 0/0 (G0/0) | Gigabit Ethernet 0/1 (G0/1) | Serial 0/0/0 (S0/0/0) | Serial 0/0/1 (S0/0/1) |
| 4221 | Gigabit Ethernet 0/0/0 (G0/0/0) | Gigabit Ethernet 0/0/1 (G0/0/1) | Serial 0/1/0 (S0/1/0) | Serial 0/1/1 (S0/1/1) |
| 4300 | Gigabit Ethernet 0/0/0 (G0/0/0) | Gigabit Ethernet 0/0/1 (G0/0/1) | Serial 0/1/0 (S0/1/0) | Serial 0/1/1 (S0/1/1) |

---

## 16.5.3 What did I learn in this module?
### Security Threats and Vulnerabilities
- Network attacks can lead to lost time/money and stolen or damaged information.
- Attackers often succeed by exploiting software vulnerabilities or misconfigurations.
- Four common threat outcomes: information theft, data loss/manipulation, identity theft, and disruption of service.
- Three primary vulnerability categories: technological, configuration, and weak/missing security policy.
- Physical threats commonly fall into four classes: hardware, environmental, electrical, and maintenance.

### Network Attacks
- Malware is malicious software designed to damage, disrupt, steal, or perform unauthorized actions.
- Viruses, worms, and Trojan horses are common malware types.
- Network attacks commonly fall into three groups:
  - **Reconnaissance** (internet queries, ping sweeps, and port scans)
  - **Access attacks** (password attacks/brute force, Trojans, packet sniffers, trust exploitation, port redirection, man-in-the-middle)
  - **Denial of Service** (DoS and DDoS)

### Network Attack Mitigation
- Secure devices first (routers, switches, servers, hosts), then layer controls (defense-in-depth).
- Common security components/services: VPN, firewall (ASA), IPS, ESA/WSA, and AAA servers.
- Keep backups of configs and OS/IOS images (e.g., on FTP or similar) so you can restore quickly after failure.
- Patch vulnerable systems and manage critical updates (ideally with automation).
- AAA provides **Authentication**, **Authorization**, and **Accounting**.
- Firewalls typically sit between networks and control traffic; public-facing servers often live in a **DMZ**.
- Firewall methods include packet filtering, application filtering, URL filtering, and SPI.
- Endpoint security includes policies, antivirus, and host intrusion prevention; more advanced solutions can use network access control.

### Device Security
- Default OS/device settings are often inadequate; hardening is required.
- Cisco AutoSecure can help improve device security, but it does not guarantee complete protection.
- Good practices include changing defaults, restricting access, disabling unnecessary services, using strong passwords/passphrases, enabling SSH, encrypting stored passwords, using lockout controls, and auto-disconnecting inactive sessions.

---

## 16.5.4 Module Quiz — Network Security Fundamentals (Q1–Q6)

### Question 1
Which component is designed to protect against unauthorized communications to and from a computer?

- Security center
- Port scanner
- Antimalware
- Antivirus
- Firewall

**Answer:** Firewall

### Question 2
Which command will block login attempts on RouterA for a period of 30 seconds if there are 2 failed login attempts within 10 seconds?

- RouterA(config)# login block-for 10 attempts 2 within 30
- RouterA(config)# login block-for 30 attempts 2 within 10
- RouterA(config)# login block-for 30 attempts 10 within 2
- RouterA(config)# login block-for 2 attempts 30 within 10

**Answer:** RouterA(config)# login block-for 30 attempts 2 within 10

### Question 3
What is the purpose of the network security accounting function?

- To keep track of the actions of a user
- To determine which resources a user can access
- To require users to prove who they are
- To provide challenge and response questions

**Answer:** To keep track of the actions of a user

### Question 4
What type of attack may involve the use of tools such as nslookup and fping?

- Denial of service attack
- Access attack
- Worm attack
- Reconnaissance attack

**Answer:** Reconnaissance attack

### Question 5
Which benefit does SSH offer over Telnet for remotely managing a router?

- TCP usage
- Connections via multiple VTY lines
- Encryption
- Authorization

**Answer:** Encryption

### Question 6
What is one of the most effective security tools available for protecting users from external threats?

- Firewalls
- Router that run AAA services
- Patch servers
- Password encryption techniques

**Answer:** Firewalls

---
# 16.5.4 Module Quiz — Network Security Fundamentals (Q6–Q15)

> Extracted from your screenshots (Result Page view).  
> Format: question + choices + **correct answer**.

---

## Question 6
**What is one of the most effective security tools available for protecting users from external threats?**

- Router that run AAA services  
- Patch servers  
- Password encryption techniques  
- **Firewalls** ✅

**Answer:** Firewalls

---

## Question 7
**Which type of network threat is intended to prevent authorized users from accessing resources?**

- Access attacks  
- Reconnaissance attacks  
- Trust exploitation  
- **DoS attacks** ✅

**Answer:** DoS attacks

---

## Question 8
**Which three services are provided by the AAA framework? (Choose three.)**

- Automation  
- Autobalancing  
- **Accounting** ✅  
- **Authorization** ✅  
- **Authentication** ✅  

**Answer:** Authentication, Authorization, Accounting

---

## Question 9
**Which malicious code attack is self-contained and tries to exploit a specific vulnerability in a system being attacked?**

- Virus  
- **Worm** ✅  
- Trojan horse  
- Social engineering  

**Answer:** Worm

---

## Question 10
**Some routers and switches in a wiring closet malfunctioned after an air conditioning unit failed. What type of threat does this situation describe?**

- Configuration  
- **Environmental** ✅  
- Electrical 
- Maintenance  

**Answer:** Environmental

---

## Question 11
**What does the term vulnerability mean?**

- A computer that contains sensitive information  
- A method of attack to exploit a target  
- A known target or victim machine  
- A potential threat that a hacker creates  
- **A weakness that makes a target susceptible to an attack** ✅

**Answer:** A weakness that makes a target susceptible to an attack

---

## Question 12
**What three configuration steps must be performed to implement SSH access to a router? (Choose three.)**

- A password on the console line 
- **An IP domain name** ✅  
- **A user account** ✅  
- An enable mode password  
- **A unique hostname** ✅  

**Answer:** A unique hostname, an IP domain name, and a user account

---

## Question 13
**What is the objective of a network reconnaissance attack?**

- Unauthorized manipulation of data  
- Disabling network systems or services  
- Denying access to resources by legitimate users  
- **Discovery and mapping of systems** ✅

**Answer:** Discovery and mapping of systems

---

## Question 14
**For security reasons a network administrator needs to ensure that local computers cannot ping each other. Which settings can accomplish this task?**

- Smartcard settings  
- **Firewall settings** ✅  
- MAC address settings  
- File system settings  

**Answer:** Firewall settings

---

## Question 15
**A network administrator establishes a connection to a switch via SSH. What characteristic uniquely describes the SSH connection?**

- Out-of-band access to a switch through the use of a virtual terminal with password authentication  
- Remote access to the switch through the use of a telephone dialup connection  
- On-site access to a switch through the use of a directly connected PC and a console cable  
- **Remote access to a switch where data is encrypted during the session** ✅  
- Direct access to the switch through the use of a terminal emulation program  

**Answer:** Remote access to a switch where data is encrypted during the session


---
