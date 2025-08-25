### Patching Guide

* **Importance of Patching**

  * Patching fixes security vulnerabilities, stability issues, and performance problems.
  * Unpatched systems are a common entry point for attackers.

* **Types of Patches**

  * **Security patches** – address vulnerabilities.
  * **Bug fixes** – correct functionality errors.
  * **Feature updates** – add improvements.

* **Patch Management Process**

  1. **Asset Inventory** – know all systems, software, and versions in use.
  2. **Vulnerability Scanning** – detect missing or outdated patches.
  3. **Prioritization** – patch critical vulnerabilities first (CVSS scoring, exposure).
  4. **Testing** – verify patches in staging before production deployment.
  5. **Deployment** – apply patches systematically.
  6. **Verification** – confirm patch success and system stability.
  7. **Documentation** – track applied patches for auditing.

* **Best Practices**

  * Enable **automatic updates** when feasible.
  * Maintain a **regular patch schedule** (e.g., Patch Tuesday, weekly updates).
  * Subscribe to **vendor advisories** for zero-day alerts.
  * Use a **centralized patch management system** (e.g., WSUS, SCCM, Ansible, Puppet).
  * Have a **rollback plan** in case a patch causes issues.
  * Apply **firmware and third-party patches**, not just OS updates.

* **Security Considerations**

  * Zero-day vulnerabilities may require emergency patching.
  * Outdated or unsupported software should be upgraded or decommissioned.
  * Patching must balance **security, availability, and operational continuity**.

