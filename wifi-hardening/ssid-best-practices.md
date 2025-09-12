# SSID Best Practices

The **SSID (Service Set Identifier)** is the name of your Wi-Fi network. Proper SSID management is an essential part of Wi-Fi hardening to improve security, privacy, and network management.

---

## Why SSID Security Matters

- Prevents unauthorized users from easily identifying your network.  
- Reduces exposure to attacks such as **Wi-Fi spoofing**, **Rogue APs**, and **Evil Twin attacks**.  
- Encourages better network hygiene and compliance with security policies.  

📖 References:  
- [CISA: Securing Wireless Networks](https://www.cisa.gov/resources-tools/resources/securing-wireless-networks)  
- [NIST SP 800-153: Guidelines for Securing Wireless Local Area Networks](https://csrc.nist.gov/publications/detail/sp/800-153/final)  

---

## SSID Best Practices

### 1. Avoid Default SSIDs
- Router manufacturers often use default SSIDs (e.g., “Linksys” or “Netgear”).  
- Attackers can guess default passwords and exploits specific to those brands.  

### 2. Do Not Include Personal Information
- Avoid using names, addresses, or other identifiable information.  
- Example to avoid: `WilliamHomeWiFi` or `123MainSt`.  

### 3. Use Unique and Non-Descriptive Names
- Choose a generic or creative name unrelated to you or your devices.  
- Example: `BlueSky_45` or `Network42`.  

### 4. Disable SSID Broadcast (Optional)
- Hides your network from casual scanning.  
- Note: This is **not a strong security measure** as SSIDs can still be discovered via passive sniffing.  

### 5. Separate Guest Networks
- Create a separate SSID for guests.  
- Apply network segmentation and firewall rules.  

### 6. Change SSID Periodically (Optional)
- Not strictly necessary if WPA2/WPA3 encryption is used, but may help in high-risk environments.  

---

## Additional Wi-Fi Security Recommendations

- Use **WPA3** (or WPA2 if WPA3 is not available).  
- Enable **strong passwords** (12+ characters, mixed case, numbers, symbols).  
- Disable **WPS** (Wi-Fi Protected Setup).  
- Limit **DHCP leases** and consider **MAC filtering** as an additional layer.  
- Monitor for **rogue access points** regularly.  

📖 References:  
- [Wi-Fi Alliance: WPA3 Security](https://www.wi-fi.org/discover-wi-fi/security)  
- [US-CERT: Securing Wireless Networks](https://www.cisa.gov/resources-tools/resources/securing-wireless-networks)  

---

## Example SSID Naming Approaches

| Approach            | Example               | Notes                               |
|--------------------|--------------------|------------------------------------|
| Generic/Neutral     | Network42           | Avoids personal info               |
| Randomized          | BlueSky_45          | Harder to associate with location |
| Guest Network       | Guest_Office        | Separate VLAN and firewall rules  |
| Avoid Default Names | Linksys, Netgear    | Default names attract attackers   |

---

### References

- [CISA – Securing Wireless Networks](https://www.cisa.gov/resources-tools/resources/securing-wireless-networks)  
- [NIST SP 800-153](https://csrc.nist.gov/publications/detail/sp/800-153/final)  
- [Wi-Fi Alliance – WPA3](https://www.wi-fi.org/discover-wi-fi/security)  
- [US-CERT – Wireless Security Tips](https://www.cisa.gov/resources-tools/resources/securing-wireless-networks)  

