# 📋 GDPR Compliance Audit Checklist

## Assessment Overview
This framework was utilized during the **Control Evaluation (Phase 2)** of the MediLink Online Clinic audit. It maps current technical and administrative practices against the core requirements of the General Data Protection Regulation (GDPR). 

The compliance status is categorized as:
* ✅ **Pass:** Control is implemented and effective.
* ⚠️ **Partial:** Control exists but requires significant improvement or formalization.
* ❌ **Fail:** Control is missing or entirely ineffective.

---

## Audit Framework & Findings

| GDPR Article | Control Area | Audit Question | Compliance Status | Audit Findings / Evidence |
| :--- | :--- | :--- | :--- | :--- |
| **Art. 5(1)(c)** | Data Minimization | Are data collection mechanisms strictly limited to what is necessary for the specified purpose? | ⚠️ Partial | Registration forms collect unnecessary optional user data. |
| **Art. 5(1)(e)** | Storage Limitation | Are automated workflows implemented to purge PII/PHI once the retention period expires? | ❌ Fail | Deletion relies entirely on manual database queries; high risk of retention violations. |
| **Art. 7** | Consent | Is user consent explicit, granular, and easily revocable? | ⚠️ Partial | Utilizes a bundled 'Accept All' checkbox; lacks granular toggles for marketing vs. core services. |
| **Art. 15** | Right of Access | Are Subject Access Requests (SARs) processed within the statutory 30-day timeframe? | ⚠️ Partial | Process is manual (email ticketing), leading to slow response times and potential SLA breaches. |
| **Art. 17** | Right to Erasure | Can users request data deletion, and are legal retention exceptions clearly documented? | ❌ Fail | Exceptions for mandatory medical data retention are poorly documented; no clear workflow for 'Right to be Forgotten' requests. |
| **Art. 28** | Processor Contracts | Are formal Data Processing Agreements (DPAs) executed with all third-party sub-processors? | ❌ Fail | Missing DPAs with critical vendors (Stripe, Twilio, SendGrid). Only standard SLAs are in place. |
| **Art. 32(1)(a)**| Security (Encryption) | Is PII and PHI encrypted both at-rest and in-transit? | ✅ Pass | Effective use of TLS 1.3, AWS S3 SSE-KMS, and encrypted PostgreSQL instances. |
| **Art. 32(1)(b)**| Security (Monitoring) | Are core databases actively monitored for unauthorized access or anomalies? | ❌ Fail | Only basic AWS CloudWatch logs exist. No proactive alerting configured for unauthorized DB access. |
| **Art. 32(1)(c)**| Security (Resilience)| Is the ability to restore access to personal data tested regularly? | ⚠️ Partial | Automated daily AWS backups are running, but quarterly restoration tests are not being conducted. |
| **Art. 33** | Breach Notification | Is there a tested Incident Response (IR) plan capable of notifying authorities within 72 hours? | ⚠️ Partial | A basic IR plan exists, but no formal tabletop exercises have been conducted to validate the 72-hour SLA. |
| **Art. 35** | DPIA | Has a Data Protection Impact Assessment (DPIA) been conducted for the processing of health data? | ❌ Fail | Processing of special category data (PHI) is occurring without a mandatory DPIA on record. |

---
*Note: Findings from this checklist have been transferred to the master Risk & Compliance Register for prioritization and remediation tracking.*