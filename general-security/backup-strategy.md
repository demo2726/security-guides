# Backup Strategy

Backups are a critical part of cybersecurity and business continuity. A strong backup strategy ensures that data can be restored after incidents such as ransomware, hardware failure, or accidental deletion.

---

## Why Backups Matter

- Protect against ransomware and malware that encrypt or destroy data.  
- Enable recovery after accidental deletion or corruption.  
- Meet compliance requirements (HIPAA, PCI DSS, GDPR, ISO 27001).  
- Reduce downtime and financial impact of incidents.  

---

## Core Principles of Backup Strategy

1. **The 3-2-1 Rule**  
   - Keep **3 copies** of your data (1 primary + 2 backups).  
   - Store on **2 different media types** (e.g., local disk + cloud).  
   - Keep **1 copy offsite/offline** (air-gapped or immutable).  

2. **Regular Backup Schedule**  
   - Daily for critical data.  
   - Weekly/monthly for less critical data.  
   - Automate whenever possible.  

3. **Encryption & Security**  
   - Encrypt backups both **in transit** and **at rest**.  
   - Protect access with strong authentication (MFA for cloud backups).  

4. **Testing & Validation**  
   - Regularly test restoring data from backups.  
   - Verify integrity and usability of backups.  

5. **Retention Policies**  
   - Define how long backups are kept (e.g., 30 days, 6 months, 7 years).  
   - Balance storage costs with compliance and business needs.  

---

## Types of Backups

- **Full Backup** – Entire data set; simplest but time-consuming.  
- **Incremental Backup** – Copies only changes since last backup; fast but requires multiple sets to restore.  
- **Differential Backup** – Copies changes since last full backup; balance between speed and recovery ease.  
- **Image-Based Backup** – Captures a complete system snapshot for rapid recovery.  
- **Cloud Backup** – Flexible, scalable, and offsite by default.  

---

## Best Practices

- Follow the **3-2-1 rule** or improved variations like **3-2-1-1-0** (one offline, zero errors after testing).  
- Keep at least one **offline/air-gapped backup** to protect against ransomware.  
- Document backup procedures and responsibilities.  
- Use immutable storage (WORM: Write Once, Read Many) when available.  
- Align backup frequency with **Recovery Point Objective (RPO)** and **Recovery Time Objective (RTO)** requirements.  
- Include backups as part of your **incident response plan**.  

---

## References

- [CISA – Ransomware Guide: Backup and Recovery](https://www.cisa.gov/stopransomware/ransomware-guide)  
- [NIST SP 800-34 Rev. 1 – Contingency Planning Guide](https://csrc.nist.gov/publications/detail/sp/800-34/rev-1/final)  
- [NCSC (UK) – Backup and Recovery](https://www.ncsc.gov.uk/collection/10-steps-to-cyber-security/data-recovery-and-backup)  
- [US-CERT – Data Backup Options](https://us-cert.cisa.gov/ncas/tips/ST04-023)  
- [ISO/IEC 27031 – ICT Readiness for Business Continuity](https://www.iso.org/standard/44374.html)  

---

