**`security-guides/Labs/ssh-brute-force-lab.md`:**

* **Objective:** Demonstrate SSH brute force attacks in a controlled lab environment.
* **Lab Setup:**

  * Create two VMs: one as the attacker (e.g., Kali Linux) and one as the target (e.g., Ubuntu server).
  * Ensure SSH is enabled on the target machine.
  * Use weak or default credentials to simulate a vulnerable system.
* **Tools Used:**

  * `hydra` or `medusa` for SSH brute-force attempts.
  * Optional: custom wordlists with `rockyou.txt`.
* **Attack Process:**

  * Run brute-force attempts from attacker VM against the target SSH service.
  * Observe login attempts and system responses.
* **Monitoring:**

  * On the target machine, monitor `/var/log/auth.log` for failed login attempts.
  * Use IDS/IPS (like Fail2ban, Snort, or Suricata) to detect brute-force patterns.
* **Defense Mechanisms:**

  * Implement rate limiting or account lockouts.
  * Use SSH keys instead of passwords.
  * Enable Fail2ban to block repeated failed attempts.
  * Configure UFW/iptables to limit SSH access by IP.
* **Learning Outcome:**

  * Understand how brute force attacks work.
  * Learn how to detect them in logs.
  * Practice defensive configurations to harden SSH services.
