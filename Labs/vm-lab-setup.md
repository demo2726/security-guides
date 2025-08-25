### `vm-lab-setup.md`

1. **Purpose of the Lab**

   * Create a safe, isolated environment for practicing security testing.
   * Avoid impacting host machine or production systems.

2. **Virtualization Options**

   * Use **VirtualBox**, **VMware Workstation/Player**, or **Hyper-V**.
   * Containers (Docker) for lightweight setups when applicable.

3. **Networking Setup**

   * Prefer **NAT** or **Host-Only Adapter** for isolation.
   * Avoid bridged mode unless required and controlled.
   * Segment attacker and target VMs within an internal network.

4. **Essential VMs to Include**

   * **Attacker Machine** → Kali Linux, Parrot OS, or similar.
   * **Target Machine(s)** → Intentionally vulnerable systems (Metasploitable, DVWA, Juice Shop, etc.).
   * **Monitoring Tools** → Security Onion, ELK Stack, or Wireshark for traffic analysis (optional).

5. **Baseline Security Practices**

   * Take **snapshots** before running exploits.
   * Limit internet access for target VMs.
   * Use strong host passwords and keep host OS updated.

6. **Resource Planning**

   * Allocate enough **CPU, RAM, and disk** per VM.
   * Use shared folders cautiously (potential attack vector).

7. **Learning Objectives**

   * Safely experiment with exploits.
   * Practice detection and defense in a controlled setup.
   * Develop skills for penetration testing and forensics.

