## SSH Configuration Check Using `sshd -T`

### Context
While checking the SSH configuration, I could not clearly see the value for `PermitRootLogin` in the config file. Because of this, I needed a way to confirm what setting SSH was actually using at runtime.

---

### Investigation Approach
To find the active SSH configuration, I used:

```bash
sshd -T | grep permitrootlogin
