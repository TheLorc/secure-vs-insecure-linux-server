# Hardening Steps – Secure Ubuntu Server

## Overview
This file documents the steps taken to secure an Ubuntu server after identifying vulnerabilities in an insecure setup.

## System Hardening
The system was first updated to ensure all packages were patched:

sudo apt update -y
sudo apt upgrade -y

SSH was hardened by disabling root login and password authentication, and configuring SSH key-based authentication using keypairs:

ssh-keygen
PermitRootLogin no
PasswordAuthentication no
sudo systemctl restart ssh

A firewall was enabled using UFW to restrict network access:

sudo ufw enable
sudo ufw allow ssh
sudo ufw status

Unused services were disabled to reduce the attack surface:

sudo systemctl disable <apache2>

Fail2Ban was installed to protect against brute-force attacks:

sudo apt install fail2ban -y
sudo systemctl enable fail2ban
sudo systemctl start fail2ban

## Summary
These steps improved the server’s security by reducing vulnerabilities, limiting access, and enforcing stronger authentication.
