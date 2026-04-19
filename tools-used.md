This section documents the tools and commands used during the insecure configuration phase of the Linux server security project. These tools were used to inspect system status, verify configurations, and identify security weaknesses

- ss
  Used to inspect active network sockets. Helped confirm SSH was listening on port 22.

- ufw
  Used to check firewall rules and verify whether SSH traffic was allowed.

- sshd -T
  Used to view the effective SSH configuration after all system defaults and overrides.

- netstat 
  Used to display active network connections and listening ports. Helped verify that SSH (port 22) was open and actively listening on the system.

- systemctl
Used to check the status of system services such as SSH and Apache2. Helped confirm that services were enabled and actively running in the insecure configuration.

- apt
Used to install and manage system packages such as Apache2. Demonstrated how additional services can increase the system’s attack surface.

- fail2ban
Checked to determine whether brute-force protection was installed. Confirmed that Fail2ban was not installed or active, meaning no automatic protection against repeated login attempts was in place.

#Summary
These tools were used to inspect and document an intentionally insecure Linux server configuration, highlighting exposed services, weak authentication settings, lack of firewall protection, and absence of intrusion prevention mechanisms.
