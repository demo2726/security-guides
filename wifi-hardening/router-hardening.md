### **Router Hardening **

* **Change Default Credentials**

  * Replace default admin usernames/passwords immediately.
  * Use strong, unique passwords and enable MFA if supported.

* **Firmware & Software Updates**

  * Regularly update router firmware to patch vulnerabilities.
  * Enable automatic updates where possible.

* **Disable Unnecessary Services**

  * Turn off WPS, UPnP, Telnet, FTP, or remote management unless required.
  * If remote admin is necessary, restrict to VPN or specific IPs.

* **Secure Wireless Settings**

  * Use WPA3 (or WPA2 if older devices require).
  * Disable insecure protocols like WEP.
  * Hide SSID broadcasting if appropriate (not foolproof but reduces exposure).

* **Network Segmentation**

  * Separate guest network and IoT devices from internal LAN.
  * Use VLANs/firewall rules to control traffic.

* **Access Control**

  * Limit number of allowed devices or enable MAC filtering (secondary measure).
  * Restrict admin access to wired connections or trusted IP ranges.

* **Firewall & Intrusion Protection**

  * Enable built-in router firewall features.
  * Block inbound traffic by default unless explicitly required.

* **Logging & Monitoring**

  * Enable logging of access attempts and configuration changes.
  * Monitor for unauthorized devices or abnormal traffic patterns.

* **DNS Security**

  * Use trusted DNS resolvers (e.g., DoH/DoT, internal DNS).
  * Block malicious domains where supported.

* **Backup & Recovery**

  * Backup router configuration securely.
  * Document settings for disaster recovery.


