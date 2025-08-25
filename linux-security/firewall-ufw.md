### UFW (Uncomplicated Firewall) Hardening

1. **Enable UFW**

   * Run: `sudo ufw enable`
   * Makes firewall rules active.

2. **Default Policy**

   * Deny all incoming traffic: `sudo ufw default deny incoming`
   * Allow all outgoing traffic: `sudo ufw default allow outgoing`

3. **Allow Only Needed Services**

   * Example: `sudo ufw allow ssh`
   * Open only required ports (e.g., HTTP/HTTPS, DNS).

4. **Limit SSH Connections**

   * Prevent brute-force attacks: `sudo ufw limit ssh`

5. **Allow Specific IPs**

   * Restrict access to trusted hosts:
     `sudo ufw allow from <IP> to any port 22`

6. **Deny by Default**

   * Block everything else unless explicitly allowed.

7. **Logging**

   * Enable logging for monitoring suspicious activity:
     `sudo ufw logging on`

8. **Check Status**

   * Verify rules: `sudo ufw status verbose`

9. **Application Profiles**

   * List available profiles: `sudo ufw app list`
   * Allow via profile: `sudo ufw allow "Nginx Full"`

10. **Disable UFW (if needed)**

    * Turn off firewall safely: `sudo ufw disable`

