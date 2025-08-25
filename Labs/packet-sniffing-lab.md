**`security-guides/Labs/packet-sniffing-lab.md`**:

* **Objective:** Introduce packet sniffing concepts, tools, and risks in a controlled lab environment.
* **Lab Setup:**

  * Two or more machines on the same network (attacker + victim).
  * Use a switch or hub, or configure a VM network in promiscuous mode.
* **Tools Used:**

  * `Wireshark` for GUI-based packet capture and analysis.
  * `tcpdump` for command-line sniffing.
* **Attack Process:**

  * Capture unencrypted traffic (HTTP, FTP, Telnet, etc.).
  * Filter packets by protocol, IP address, or port.
  * Extract credentials or sensitive data from captured packets (demonstration purposes only).
* **Monitoring & Analysis:**

  * Show how cleartext protocols expose usernames, passwords, and other data.
  * Observe packet headers (source, destination, protocol).
  * Demonstrate session hijacking potential with sniffed information.
* **Defense Mechanisms:**

  * Encrypt traffic using TLS/SSL, SSH, or VPNs.
  * Use secure protocols instead of plaintext (HTTPS instead of HTTP, SFTP instead of FTP).
  * Implement network segmentation to reduce sniffing risk.
  * Deploy IDS/IPS to detect sniffing behavior.
* **Learning Outcome:**

  * Understand how packet sniffers capture and analyze traffic.
  * Recognize the dangers of unencrypted communications.
  * Learn how to secure networks and services against packet sniffing.
