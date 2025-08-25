

### **Auditd Monitoring **

* **Purpose of auditd**

  * Linux auditing system for tracking security-relevant events.
  * Helps detect suspicious activity, policy violations, and intrusions.

* **Installation & Service**

  * Install with package manager (`apt install auditd` or `yum install audit`).
  * Ensure service is enabled and starts on boot.

* **Audit Rules**

  * Define what system calls or files to monitor.
  * Examples:

    * Watch `/etc/passwd` & `/etc/shadow` for changes.
    * Monitor execution of privileged commands (`/usr/bin/sudo`).
    * Track login/logout events.

* **Configuration**

  * Rules stored in `/etc/audit/audit.rules` or `/etc/audit/rules.d/`.
  * Configure logging to `/var/log/audit/audit.log`.

* **Event Analysis**

  * Use `ausearch` to query audit logs.
  * Use `aureport` for summaries (failed logins, file access, etc.).

* **Best Practices**

  * Tailor rules to system role (e.g., web server, DB server).
  * Protect audit logs from tampering.
  * Forward logs to central SIEM for correlation.
  * Regularly review reports to detect anomalies.

* **Performance Considerations**

  * Too many audit rules = performance impact.
  * Focus on critical files, directories, and commands.

