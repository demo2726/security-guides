# Linux Security Guides

This document consolidates several Linux security topics, including **SELinux/AppArmor**, **Log Monitoring**, and **Fail2ban**. It is aimed at beginner-to-intermediate users for hardening Linux systems.

---

## Table of Contents

1. [SELinux and AppArmor](#selinux-and-apparmor)  
2. [Linux Log Monitoring](#linux-log-monitoring)  
3. [Fail2ban Setup](#fail2ban-setup)  

---

## SELinux and AppArmor

### Overview
SELinux (Security-Enhanced Linux) and AppArmor are **Linux Security Modules (LSMs)** that provide **Mandatory Access Control (MAC)**. They restrict applications and services to the minimum permissions required.

---

### SELinux

- **Developed by**: NSA, open-source community  
- **Policy-based**: Detailed rules and labels define access.  
- **Modes**:
  - **Enforcing** – Blocks unauthorized actions  
  - **Permissive** – Logs violations only  
  - **Disabled** – Turns SELinux off  
- **Strengths**: Granular control for enterprise environments  
- **Challenges**: Complex configuration  

📖 References:  
- [SELinux Project Wiki](https://selinuxproject.org/page/Main_Page)  
- [Red Hat SELinux Guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/using_selinux/index)  

---

### AppArmor

- **Developed by**: Canonical/Ubuntu  
- **Profile-based**: Human-readable application-specific profiles  
- **Modes**:
  - **Enforce** – Blocks unauthorized actions  
  - **Complain** – Logs violations only  
- **Strengths**: Easier configuration than SELinux  
- **Challenges**: Less granular, mostly Ubuntu/SUSE  

📖 References:  
- [Ubuntu AppArmor Documentation](https://ubuntu.com/server/docs/security-apparmor)  
- [AppArmor Wiki](https://gitlab.com/apparmor/apparmor/-/wikis/home)  

---

### Comparison

| Feature          | SELinux                       | AppArmor                     |
|------------------|-------------------------------|-------------------------------|
| Granularity      | Very fine-grained             | Profile-based, simpler       |
| Complexity       | Steep learning curve          | Easier to manage             |
| Adoption         | Red Hat, CentOS, Fedora       | Ubuntu, Debian, SUSE         |
| Flexibility      | Highly flexible policies      | Quick setup, app-specific    |

---

### Best Practices

1. Enable one LSM only.  
2. Start in **permissive/complain mode** before enforcing.  
3. Audit logs regularly for violations.  
4. Use distribution defaults before customizing policies.  

---

## Linux Log Monitoring

### Overview
Log monitoring is essential to detect unauthorized access, service failures, malware activity, or policy violations. Logs are typically stored in `/var/log/`.

---

### Key Log Files

- `/var/log/auth.log` or `/var/log/secure` – Authentication logs  
- `/var/log/syslog` or `/var/log/messages` – General system events  
- `/var/log/kern.log` – Kernel messages  
- `/var/log/dmesg` – Hardware/driver messages  
- `/var/log/httpd/` or `/var/log/nginx/` – Web server logs  
- `/var/log/faillog` – Failed logins  

📖 References:  
- [Ubuntu Linux Log Files](https://help.ubuntu.com/community/LinuxLogFiles)  
- [Red Hat Linux Log Files](https://access.redhat.com/solutions/54216)  

---

### Log Monitoring Tools

- **Syslog / rsyslog / journald**: Collects and queries logs (`journalctl`)  
- **Logwatch**: Summarizes logs, emails reports  
- **Logrotate**: Rotates, compresses, and removes old logs  
- **Fail2ban**: Monitors logs for failed logins, bans IPs  
- **Auditd**: Tracks detailed security events  
- **SIEM tools**: Splunk, ELK, Graylog for centralized log analysis  

📖 References:  
- [systemd Journal Docs](https://www.freedesktop.org/software/systemd/man/journald.conf.html)  
- [Auditd Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-introduction-to-auditd)  

---

### Best Practices

1. Centralize logs with a syslog server or SIEM.  
2. Set retention policies according to compliance needs.  
3. Use alerts for unusual activity.  
4. Protect log integrity.  
5. Regularly review logs and reports.  

---

### Example Commands

```bash
# View authentication attempts
sudo tail -f /var/log/auth.log

# Search failed logins
grep "Failed password" /var/log/auth.log

# Query systemd logs for SSH
journalctl -u ssh

