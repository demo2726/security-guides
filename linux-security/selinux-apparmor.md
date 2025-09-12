# SELinux and AppArmor

## Overview
SELinux (Security-Enhanced Linux) and AppArmor are two major **Linux Security Modules (LSMs)** that provide **Mandatory Access Control (MAC)**, offering finer-grained security beyond traditional discretionary access control (DAC).

Both aim to **restrict applications and system services** to the minimum required permissions, reducing the damage if a process is compromised.

---

## SELinux (Security-Enhanced Linux)

- **Developed by**: NSA and maintained by the open-source community.
- **Policy-based**: Uses detailed rules and labels to define what processes can access which files, ports, or other resources.
- **Modes**:
  - **Enforcing**: Actively blocks unauthorized actions.
  - **Permissive**: Logs violations but doesn’t block them.
  - **Disabled**: SELinux is turned off.
- **Strengths**:
  - Very granular control.
  - Powerful for enterprise environments.
- **Challenges**:
  - Complex configuration and learning curve.
  - Misconfiguration can cause service disruptions.

📖 References:  
- [SELinux Project Wiki](https://selinuxproject.org/page/Main_Page)  
- [Red Hat SELinux Guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/using_selinux/index)  

---

## AppArmor

- **Developed by**: Immunix (later Canonical/Ubuntu).
- **Profile-based**: Uses human-readable profiles that define what resources applications can use.
- **Modes**:
  - **Enforce**: Actively blocks unauthorized actions.
  - **Complain**: Logs violations without blocking.
- **Strengths**:
  - Easier to configure and manage than SELinux.
  - Profiles are relatively simple and application-specific.
- **Challenges**:
  - Less granular than SELinux.
  - Primarily used in Ubuntu and SUSE ecosystems.

📖 References:  
- [Ubuntu AppArmor Documentation](https://ubuntu.com/server/docs/security-apparmor)  
- [AppArmor Wiki](https://gitlab.com/apparmor/apparmor/-/wikis/home)  

---

## Comparison

| Feature          | SELinux                                | AppArmor                         |
|------------------|----------------------------------------|----------------------------------|
| **Granularity**  | Very fine-grained, label-based         | Profile-based, simpler rules     |
| **Complexity**   | Steep learning curve                   | Easier to learn/manage           |
| **Adoption**     | Red Hat, CentOS, Fedora, enterprise    | Ubuntu, Debian, SUSE             |
| **Flexibility**  | Highly flexible, powerful policies     | Quick setup, app-specific focus  |

---

## Best Practices

1. **Enable one LSM** – SELinux and AppArmor cannot both enforce policies simultaneously. Choose based on your distribution and needs.
2. **Start permissive/complain mode** – Log violations before enforcing to avoid breaking services.
3. **Regularly audit logs** – Identify and adjust overly restrictive policies.
4. **Use distribution defaults** – Start with vendor-provided policies/profiles before customizing.

---

## Further Reading

- [Linux Security Modules (Kernel Docs)](https://www.kernel.org/doc/html/latest/admin-guide/LSM/index.html)  
- [SELinux Wiki](https://selinuxproject.org/page/Main_Page)  
- [AppArmor Wiki](https://gitlab.com/apparmor/apparmor/-/wikis/home)  
- [Red Hat SELinux Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/using_selinux/index)  
- [Ubuntu AppArmor Docs](https://ubuntu.com/server/docs/security-apparmor)  

