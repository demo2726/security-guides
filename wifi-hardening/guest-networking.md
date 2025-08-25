Here are **key points** you can use for `security-guides/wifi-hardening/guest-networking.md`:

* **Purpose of Guest Networks**

  * Isolate visitors or untrusted devices from main internal network.
  * Reduce risk of malware or unauthorized access spreading.

* **Network Segmentation**

  * Place guest network on a separate VLAN or SSID.
  * Ensure no routing between guest and internal corporate network.
  * Use firewall rules to restrict access (e.g., only allow internet traffic).

* **Authentication & Access Control**

  * Require WPA2/WPA3 encryption, even for guest networks.
  * Use unique pre-shared keys or captive portals for accountability.
  * Consider time-limited or bandwidth-limited access tokens.

* **Traffic Monitoring & Logging**

  * Monitor guest network for suspicious or excessive traffic.
  * Apply rate limiting or bandwidth throttling to prevent abuse.
  * Log connections for incident response (while respecting privacy laws).

* **Security Best Practices**

  * Disable peer-to-peer communication between guest devices.
  * Restrict access to sensitive services (DNS, internal IPs, printers, etc.).
  * Regularly rotate guest Wi-Fi credentials.
  * Avoid using open/unencrypted guest networks.

* **Business Considerations**

  * Guest networks improve security posture while offering convenience.
  * Helps protect employees’ work devices from guest device compromise.
  * Provides a safer option for IoT devices by isolating them from sensitive data.

Would you like me to also **expand this into a full structured markdown file** (with sections like *Introduction, Setup, Best Practices, Monitoring, Conclusion*) so you can drop it directly into your `security-guides/wifi-hardening/` folder?

