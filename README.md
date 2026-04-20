# 🔐 Ubuntu Server Security Project

## Overview
This project shows the difference between an insecure and a secure Ubuntu server running in a virtual machine.  
It was created to practice basic Linux security and system hardening.

---

## 🖥️ Environment
- Ubuntu Server (VM)
- VirtualBox / VMware
- SSH access

---

## ⚠️ Insecure Server
The insecure version contains common security weaknesses:
- SSH root login enabled
- Password authentication allowed
- Firewall not configured
- Unnecessary services running

---

## 🔐 Secure Server
The secure version was hardened using basic security steps:
- Disabled SSH root login
- Enabled SSH key authentication
- Configured UFW firewall
- Removed unnecessary services
- Updated system packages
- Added Fail2Ban

---

## 📌 Key Learning
Basic Linux hardening can significantly reduce security risks.
Importance of the principle of least privilege
Gained hands-on experience using a Linux terminal
---

## 📁 Project Structure
- `insecure-phase/`
- `secure-phase/`
