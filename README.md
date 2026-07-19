# 🛡️ GDPR Privacy Impact Assessment (PIA) & Compliance Audit

![GDPR](https://img.shields.io/badge/Compliance-GDPR-blue.svg) ![Risk Management](https://img.shields.io/badge/Domain-GRC%20%26%20Risk%20Management-success.svg) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

> **Disclaimer:** This is a simulated Governance, Risk, and Compliance (GRC) project developed for portfolio demonstration. It simulates a real-world privacy audit and risk assessment environment.

## 📌 Executive Summary
This project outlines a comprehensive **Privacy Impact Assessment (PIA)** and **Gap Analysis** conducted for **MediLink Online Clinic**, a fictional telehealth platform providing virtual medical consultations to European Union (EU) residents. 

Due to the collection and processing of highly sensitive Personally Identifiable Information (PII) and Protected Health Information (PHI), MediLink falls under the strict regulatory obligations of the **General Data Protection Regulation (GDPR)**. This project demonstrates the ability to evaluate technical architectures, identify compliance gaps, and translate regulatory requirements into pragmatic, business-friendly recommendations.

## 🏗️ System Architecture & Data Flow
Understanding the technical landscape is critical for an accurate risk assessment. MediLink's infrastructure was analyzed as follows:
* **Hosting & Storage:** Primary data hosted in AWS EU-Central (Frankfurt) with backups in AWS EU-West (Ireland).
* **Database:** PostgreSQL (Encrypted at rest).
* **File Storage:** AWS S3 with Server-Side Encryption (SSE-KMS) for medical records and prescriptions.
* **Third-Party Sub-processors:** 
  * *Stripe* (Payment Gateway)
  * *Twilio* (Video Conferencing API)
  * *SendGrid* (Email Communications)

## ⚖️ Regulatory Scope (GDPR)
The assessment focused on evaluating MediLink's controls against the following key GDPR Articles:
* **Article 5:** Principles relating to processing of personal data (Data Minimization, Storage Limitation).
* **Article 6 & 9:** Lawfulness of processing and conditions for processing special categories of data (Medical Data).
* **Article 17:** Right to erasure ('Right to be forgotten').
* **Article 32:** Security of processing (Technical and organizational measures).
* **Article 44:** General principle for international data transfers.

## 🛠️ Audit Methodology & Approach
To simulate an industry-standard audit workflow, the following methodology was executed:
1. **Scope Definition & Data Mapping:** Identified all data ingestion points, storage repositories, and cross-border data transfers.
2. **Control Evaluation (Evidence Gathering):** Assessed current technical and administrative controls against a standard GDPR compliance checklist.
3. **Gap Analysis:** Identified discrepancies between regulatory requirements and current operational practices.
4. **Risk Assessment:** Logged findings into a Risk Register, categorizing vulnerabilities based on likelihood and business impact (High/Medium/Low).
5. **Remediation Planning:** Developed actionable, risk-based recommendations balancing regulatory compliance with operational agility.

## 📂 Project Deliverables & Artifacts

| Deliverable | Description | Access Link |
|-------------|-------------|-------------|
| **📄 Formal PIA Report** | A detailed 3-page executive report documenting data purposes, identified gaps, and prioritized recommendations. | [[04-PIA-Report](https://github.com/Isuru-Udana-Pinthu/gdpr-pia-compliance-audit/tree/88d2c8c41c55861c334f3dfad962838b07494f31/04-PIA-Report)] |
| **📊 Risk & Compliance Register** | A dynamic spreadsheet logging risks, control failures, and remediation tracking dashboards. | [[Link](https://docs.google.com/spreadsheets/d/1xe2ddA3EoritDChltQW__UI19VvOTL-nQAUFZRwNG9s/edit?usp=sharing)] |
| **📋 Project Management Board** | Kanban-based tracking of audit tasks and effort estimation. | [[Link](https://app.notion.com/p/GDPR-Scenario-Based-Privacy-Impact-Assessment-PIA-383917282f638071b113c9a70c8f9c75?source=copy_link)] |

## 🔍 Key Findings (Preview)
* **[High Risk] Storage Limitation:** Absence of automated data deletion workflows, increasing the risk of unauthorized retention of non-medical PII.
* **[High Risk] Third-Party Risk Management:** Missing formalized Data Processing Agreements (DPAs) with critical vendors (Stripe, Twilio).
* **[Medium Risk] Data Minimization:** Unnecessary optional fields collected during the initial account creation phase.

## 💡 Technologies & Tools Utilized
* **Frameworks:** GDPR, Privacy by Design principles.
* **Documentation & Dashboards:** Google Workspace (Docs, Sheets) for evidence documentation and risk tracking.
* **Project Management:** Notion, GitHub (Version Control & Markdown reporting).

---
*Authored by Isuru Udana Pintu | GRC & Cybersecurity Portfolio Project*
