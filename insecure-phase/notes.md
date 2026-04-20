## 1. SSH Configuration

SSH service is enabled and listening on port 22.

### Observations:
- SSH is active and running
- Port 22 is open on all interfaces (0.0.0.0)
- Password authentication is enabled
- Root login is allowed (`PermitRootLogin yes`)

### Risk:
- Open SSH access allows remote login attempts
- Password authentication enables brute-force attacks
- Root login increases impact of compromise

---

## 2. Firewall Configuration

### Observations:
- No active firewall (UFW disabled)

### Evidence:
- `ufw status` shows inactive state

### Risk:
- All services are exposed to any network connection
- No filtering of inbound or outbound traffic

---

## 3. Unnecessary Services

### Observations:
- Apache2 web server installed and running
- Additional services increase system attack surface

### Risk:
- More services = more potential vulnerabilities
- Unused services may be exploited if unpatched

---

## 4. User Account Security

### Observations:
- Test user created with weak password (e.g. password123)
- Password policy not enforced

### Risk:
- Weak passwords are susceptible to guessing attacks
- No complexity or lockout policy in place

---

## 5. Intrusion Prevention

### Observations:
- Fail2ban is not installed or active on the system

### Risk:
- No protection against repeated failed login attempts
- System is more vulnerable to brute-force SSH attacks
- No automatic banning of malicious IP addresses

---

## 6. Summary

This system is intentionally misconfigured to demonstrate insecure defaults commonly found in poorly hardened Linux servers. Key weaknesses include exposed SSH access, lack of firewall protection, weak authentication, absence of intrusion prevention (Fail2ban), and unnecessary services.
