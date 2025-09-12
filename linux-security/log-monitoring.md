# Linux Log Monitoring

## Overview
Log monitoring is a critical part of Linux security. System and application logs record events that can indicate:
- Unauthorized access attempts
- Service failures or misconfigurations
- Malware or rootkit activity
- Policy violations

Effective log monitoring helps **detect security incidents early** and supports compliance with security standards.

---

## Key Log Files

Most Linux logs are stored under `/var/log/`. Important examples include:

- **/var/log/auth.log** or **/var/log/secure**  
  Authentication attempts, SSH logins, sudo activity.
- **/var/log/syslog** or **/var/log/messages**  
  General system events and kernel messages.
- **/var/log/kern.log**  
  Kernel-specific events.
- **/var/log/dmesg**  
  Hardware and driver-related messages.
- **/var/log/httpd/** or **/var/log/nginx/**  
  Web server access and error logs.
- **/var/log/faillog**  
  Failed login attempts.

📖 References:  
- [Ubuntu: System Log Files](https://help.ubuntu.com/community/LinuxLogFiles)  
- [Red Hat: Linux Log Files](https://access.redhat.com/solutions/54216)  

---

## Log Monitoring Tools

### 1. **Syslog / rsyslog / journald**
- Collects and manages system logs.
- `journalctl` provides a structured way to query logs (systemd-based distros).
- 📖 [systemd Journal Documentation](https://www.freedesktop.org/software/systemd/man/journald.conf.html)

### 2. **Logwatch**
- Summarizes log activity and emails daily reports.
- 📖 [Logwatch Project](https://sourceforge.net/projects/logwatch/)

### 3. **Logrotate**
- Manages log file size by rotating, compressing, and removing old logs.
- 📖 [GNU Logrotate Manual](https://linux.die.net/man/8/logrotate)

### 4. **Fail2ban**
- Monitors logs for repeated failed logins and bans offending IPs.
- 📖 [Fail2ban Documentation](https://www.fail2ban.org/wiki/index.php/Main_Page)

### 5. **Auditd (Linux Audit Framework)**
- Tracks detailed security-relevant events (e.g., file access, privilege use).
- 📖 [Linux Auditd Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-introduction-to-auditd)

### 6. **SIEM Integration (e.g., Splunk, ELK Stack, Graylog)**
- Centralizes logs for analysis and correlation.
- Useful for large environments.

---

## Best Practices

1. **Centralize logs** using syslog servers or SIEM tools.
2. **Set proper log retention** according to compliance requirements.
3. **Use alerts** to detect unusual login attempts, privilege escalation, or service errors.
4. **Protect log integrity** – ensure logs are not writable by non-privileged users.
5. **Regularly review reports** from Logwatch or similar tools.

---

## Example Commands

- View recent authentication attempts:  
  ```bash
  sudo tail -f /var/log/auth.log

