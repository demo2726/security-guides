### 🔑 SSH Hardening Key Points

1. **Disable Root Login**

   * Set `PermitRootLogin no` in `/etc/ssh/sshd_config`.
   * Use a normal user + `sudo` instead.

2. **Use Strong Authentication**

   * Prefer SSH keys over passwords (`PasswordAuthentication no`).
   * Use `ssh-keygen -t ed25519` (modern, secure keys).
   * Optionally enforce key-based only authentication.

3. **Change Default SSH Port (Optional)**

   * Move from port `22` to a non-standard port (e.g., `2222`) to reduce automated scans.
   * Update firewall rules accordingly.

4. **Limit Access**

   * Allow only specific users/groups:

     ```
     AllowUsers user1 user2
     AllowGroups sshusers
     ```
   * Restrict which IPs can connect (`/etc/hosts.allow`, firewall, or security groups).

5. **Idle Session & Login Attempt Controls**

   * Disconnect idle sessions:

     ```
     ClientAliveInterval 300
     ClientAliveCountMax 2
     ```
   * Limit failed attempts (`MaxAuthTries 3`).

6. **Enable Logging & Monitoring**

   * Ensure `/var/log/auth.log` (Debian/Ubuntu) or `/var/log/secure` (RHEL/CentOS) is monitored.
   * Use `fail2ban` or intrusion detection tools.

7. **Use SSH Protocol 2 Only**

   * Confirm `Protocol 2` is enforced in config.

8. **Disable X11 & Agent Forwarding (if not needed)**

   * Set `X11Forwarding no`
   * Set `AllowAgentForwarding no`

9. **Regular Updates & Key Rotation**

   * Keep OpenSSH package up to date.
   * Rotate keys periodically.

10. **Multi-Factor Authentication (Optional Advanced)**

* Combine SSH keys with OTP (Google Authenticator, Duo, etc.).

