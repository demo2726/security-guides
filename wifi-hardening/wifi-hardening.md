**1. Introduction**

I.) Wi-Fi hardening definition: 
Process of strengthening the security of a wireless network so that it’s harder for attackers to break in, spy on traffic, or exploit weaknesses

II.) Why securing Wi-Fi is critical (home users, small businesses, enterprises).

a.)Home users
Protect personal data because a insecure network resks identity theft or data leaks because Wifi modem is the gateway to personal data. Prevent piggybacking which can slow internet or another individual committing illegal activites. SafeGuading Iot devices from explotation.

b.)Small business
Securing Wi-Fi is critical because a breach can erode customer trust by compromising guest devices or internal systems, disrupt business operations by exposing POS systems, servers, or cloud services to data theft or ransomware, and lead to regulatory penalties in industries like healthcare or finance if sensitive customer data is exposed.

c.)Enterprise
In enterprises, Wi-Fi security is vital because the large attack surface of hundreds or thousands of connected devices means one weak link can enable attackers to steal trade secrets or sensitive data, while a compromise could disrupt operations, cause downtime, and cost millions.

**2. Router Setup Basics**

I.) Change default admin username and password
Most routers have a default admin username and password. Attackers know these defaults and can easily break in if you don’t change them. Always set a strong, unique password that’s at least 12 characters long, combining upper/lowercase letters, numbers, and symbols. If possible, change the default username as well to make it harder for automated attacks.

II.) Update router firmware
Router manufacturers release firmware updates to patch security flaws and improve performance. Log in to your router’s admin panel and check for firmware updates regularly. Enable automatic updates if supported to stay protected without manual effort.

III.) Disable remote management unless required
Routers often include a feature that lets you access the admin panel from outside your home or business network. This creates a big attack surface for hackers. Unless you absolutely need it turn off remote management. If remote access is necessary, secure it with a VPN or IP allowlist instead of exposing the router’s login page to the open internet.

**3. Encryption & Authentication**

I.) Difference between WEP, WPA, WPA2, WPA3.

a.) WPA (Wi-Fi Protected Access) 

It was presented by Wi-Fi alliance in late 2002. Wi-Fi Alliance with Electronics Engineers (IEEE) secured the feeble sections of the recently disclosed WEP protocol and presented WPA as an interpretation. It Volume 5, Issue 4, July-August-2019 | http://ijsrcseit.com  has been made compatible with all vendors and existing equipment. The primary concern is to defeat WEP shortcoming without the change in equipment. This was finished by including (TKIP) Temporal Key Integrity Protocol for encryption and 802.1X EAP for authentication purpose to offer high security. To keep away from Information Fabrication (bit flipping), WPA presented Message Integrity Check (MIC) calculation known as "Michael". 

b.) WPA2 (Wi-Fi Protected Access, ver 2)
WPA2 (Wi-Fi protected Access 2) Implements totally IEEE 802.11 standard and improvement over WPA. Furnishes information protection by counter mode with cipher block chaining message Authentication Code Protocol (CCMP) utilizing Advanced Encryption Standard (AES) block cipher. Uses WPA2-Personal and WPA2-enterprise for Authentication. Information Integrity is checked by means of Cipher Block Chaining message validation. Secures against Replay assaults by 48-bit packet number.

c.) WPA3
Wi-Fi union impelled WPA3 the cutting edge remote security standard that can dispose of every current defencelessness. The key highlights of WPA3 are Protection against brute force attacks, WPA3 Secrecy, Protecting Open/Public Networks. WPA3 utilizes SAE (Simultaneous Authentication of Equals) handshake to offer Forward Secrecy, which keeps the offender from decoding old caught traffic. Gives individualized data encryption a component that encodes remote traffic to alleviate the danger of Manin-the-Middle-Attacks. Provides 192 -bit encryption to Wi-Fi associations.

d.) WEP (Wired Equivalent Privacy) 
WEP (Wired Equivalent Privacy) WEP is intended to give security of wired LAN by encryption, utilizing RC4 algorithm with different sides of information correspondence.

II.) Why to use WPA3-Personal.
a.)Stronger Encryption
WPA3-Personal replaces WPA2’s Pre-Shared Key (PSK) method with a more secure Simultaneous Authentication of Equals (SAE) handshake. This makes it much harder for attackers to crack your Wi-Fi password, even if they capture encrypted traffic.

b.)Protection Against Brute-Force Attacks
In WPA2, attackers could capture a 4-way handshake and then run offline dictionary attacks to guess the Wi-Fi password. WPA3 prevents this by requiring attackers to interact with the network for each password guess, which slows down brute-force attempts significantly.

c.)Forward Secrecy
Even if your Wi-Fi password is compromised in the future, WPA3 ensures that past traffic remains protected. This is because each session uses unique encryption keys, so older data cannot be decrypted retroactively.

d.)Stronger Default Encryption (192-bit option)
WPA3-Personal enforces 128-bit encryption as a baseline and offers even stronger encryption in WPA3-Enterprise (192-bit). This makes it far more resistant to modern cyberattacks.

e.)Better Security for IoT and Smart Devices
WPA3 includes Easy Connect (DPP – Device Provisioning Protocol), which allows secure onboarding of IoT devices without needing to share Wi-Fi passwords openly.

f.)Future-Proofing Your Network
WPA2 is still widely used, but it’s aging and has known weaknesses (e.g., KRACK attack). WPA3 is the new security standard and will ensure your Wi-Fi network is aligned with modern best practices for years to come.

III.) Disable WPA/WEP fallback.
a.)Older Wi-Fi security protocols like WEP and WPA (pre-WPA2) are highly insecure and can be cracked in minutes using freely available tools. Some routers still allow “mixed mode” (e.g., WPA2/WPA), which lets older devices connect by falling back to weaker encryption

**4. SSID (Network Name) Best Practices**

I.)Change the Default SSID

a.)Most routers come with a manufacturer default SSID such as “Linksys,” “Netgear,” or “TP-Link.”

b.)Keeping the default makes it easier for attackers to identify the router brand/model and exploit known vulnerabilities.

c.)Always change the SSID to something unique and non-identifiable to avoid being an easy target.

II.)Avoid Personal Information in SSID

a.)Do not include names, addresses, phone numbers, or other identifiers (e.g., “SmithFamilyWiFi” or “123MainStreetWiFi”).

b.)Attackers can use this info for social engineering, targeted attacks, or even physical location tracking.

c.)A generic name (e.g., “HomeNetwork5G” or “BlueSkyNet”) is safer.

III.)Optionally Disable SSID Broadcast

a.)Routers normally “broadcast” the SSID so nearby devices can detect and connect easily.

b.)Disabling SSID broadcast means devices must know the network name in advance to connect.

**5. Password & Key Management**

Use strong passphrases (length + randomness).

Use passphrases over passwords.

Rotate keys periodically.

**6. Advanced Router Settings**

Disable WPS (Wi-Fi Protected Setup).

Enable MAC filtering (limited effectiveness, but can add layer).

Restrict guest networks to internet-only.

Enable firewall / intrusion detection features (if available).

**7. Network Segmentation**

Set up a guest network for visitors/IoT devices.

Use VLANs (if supported).

**8. Monitoring & Logging**

Check logs for unauthorized devices.

Enable email/alert notifications if router supports.

Tools to monitor connected devices (Fing, ARP watch).

**9. Physical Security**

Place router centrally (limits signal leakage outside building).

Reduce transmit power if available.

**10. Extra Hardening**

DNS security (use DNS-over-HTTPS/DoT, Cloudflare/Google).

Disable unused services (UPnP, Telnet, FTP).

VPN on router or devices for additional encryption.

**11. Forensics Angle (Optional – good for you as a security student)**

How Wi-Fi misconfigurations leave digital evidence.

What logs show when someone brute-forces Wi-Fi.

Example of capturing rogue access points.

**12. Conclusion**

Recap best practices.

Resources/links (NIST Wi-Fi security guides, CIS benchmarks, OWASP IoT project).
