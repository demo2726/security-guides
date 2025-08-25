### `web-vuln-lab.md`

1. **Lab Setup**

   * Use a vulnerable web application (e.g., DVWA, Juice Shop, Mutillidae).
   * Run inside a VM or container for isolation.
   * Ensure no exposure to the public internet.

2. **Common Web Vulnerabilities to Test**

   * **SQL Injection (SQLi)** → Test input fields and parameters.
   * **Cross-Site Scripting (XSS)** → Stored & reflected examples.
   * **Cross-Site Request Forgery (CSRF)** → Test forced actions via crafted links.
   * **File Upload Vulnerabilities** → Try uploading malicious files.
   * **Authentication/Session Issues** → Weak passwords, session fixation, cookie theft.

3. **Tools to Use**

   * Burp Suite / OWASP ZAP for interception and fuzzing.
   * sqlmap for automated SQL injection.
   * Browser DevTools for debugging web requests.

4. **Learning Objectives**

   * Understand attacker mindset.
   * Recognize insecure coding patterns.
   * Learn how to exploit, then secure against vulnerabilities.

5. **Safety & Ethics**

   * Only test in a controlled lab.
   * Do **not** use real websites without permission.
   * Document findings for learning purposes.


