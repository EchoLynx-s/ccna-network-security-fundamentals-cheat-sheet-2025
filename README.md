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
