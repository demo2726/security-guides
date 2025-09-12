# Multi-Factor Authentication (MFA)

Multi-Factor Authentication (MFA) adds an extra layer of security by requiring more than one method of verification to prove a user’s identity. Even if a password is compromised, MFA helps block unauthorized access.

---

## What is MFA?

- **MFA** requires a combination of at least two of the following factors:
  1. **Something you know** (password, PIN).
  2. **Something you have** (smartphone, hardware token, security key).
  3. **Something you are** (fingerprint, facial recognition, biometrics).

- Example: Logging in with a password **and** a one-time code sent to an authenticator app.

---

## Why MFA Matters

- Passwords alone are vulnerable to phishing, credential stuffing, and brute force attacks.  
- MFA significantly reduces the likelihood of account compromise.  
- Many breaches (including large corporate incidents) could have been prevented with MFA enabled.

---

## Types of MFA

- **SMS-based codes**  
  - Pros: Easy to use, widely available.  
  - Cons: Vulnerable to SIM-swapping and interception.  

- **Authenticator apps (TOTP)** (Google Authenticator, Authy, Microsoft Authenticator)  
  - More secure than SMS, works offline.  

- **Push notifications** (Duo, Okta, Microsoft)  
  - User receives a prompt to approve/deny login.  
  - Faster but can be abused with “MFA fatigue” attacks.  

- **Hardware tokens** (YubiKey, Titan Security Key, FIDO2/WebAuthn devices)  
  - Strongest option, resistant to phishing.  

- **Biometric factors** (fingerprints, facial recognition)  
  - Convenient, but must be combined with another factor for strong assurance.  

---

## Best Practices for MFA

- **Prefer app-based or hardware-based MFA** over SMS.  
- **Enable MFA** on all critical accounts: email, banking, cloud services, work logins.  
- **Educate users** about “MFA fatigue” — don’t blindly approve repeated push requests.  
- **Backup codes**: Store recovery codes securely in case of device loss.  
- **Use passwordless authentication** (FIDO2/WebAuthn) when supported.  
- **For organizations**:  
  - Enforce MFA via policy (Active Directory, cloud IAM).  
  - Monitor login attempts for repeated MFA failures.  

---

## MFA in the Enterprise

- **Zero Trust Security** frameworks require MFA as a baseline.  
- Regulatory compliance often mandates MFA (HIPAA, PCI DSS, NIST).  
- MFA deployment should balance **security, usability, and accessibility**.  

---

## References

- [CISA – Implementing MFA](https://www.cisa.gov/resources-tools/resources/implementing-multi-factor-authentication)
- [NIST Digital Identity Guidelines (SP 800-63B)](https://pages.nist.gov/800-63-3/sp800-63b.html)
- [OWASP – Multi-Factor Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Multifactor_Authentication_Cheat_Sheet.html)
- [FTC – Multi-Factor Authentication Guide](https://consumer.ftc.gov/articles/multi-factor-authentication)
- [Microsoft – Protect yourself with MFA](https://learn.microsoft.com/en-us/security/compass/overview-mfa)

---

