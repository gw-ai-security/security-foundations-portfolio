# Projekt 5 – Cloud Security Assessment Framework

## Überblick
Dieses Projekt baut ein praxisorientiertes Framework für die **Sicherheitsbewertung von Cloud-Umgebungen** (AWS & Azure) auf.  
Ziel ist es, Cloud-spezifische Risiken zu erkennen, diese anhand von **ISO 27017**, **CIS Benchmarks** und **NIST CSF** einzuordnen und die Ergebnisse in einem **auditfähigen Report** zu dokumentieren.  

Das Projekt simuliert einen vollständigen Audit-Prozess: von der Checkliste über die technische Bewertung bis hin zu einem Management-tauglichen Risikoüberblick.  

---

## Zielsetzung
- Entwicklung einer **standardisierten Cloud-Checkliste** für AWS & Azure  
- Erstellung einer **Risiko-Matrix** und eines **Compliance-Mappings**  
- Dokumentation typischer Schwachstellen (z. B. offene S3-Buckets, überprivilegierte Accounts, offene Ports)  
- Erstellung eines **Cloud Security Assessment Reports** (Management Summary + technische Details)  

---

## Lerninhalte
- **Cloud Security Grundlagen**
  - Shared Responsibility Model (AWS, Azure)
  - Identity & Access Management in Cloud-Umgebungen
  - Netzwerksicherheit (NSGs, Security Groups)
  - Storage Security (S3-Buckets, Blob Storage, Verschlüsselung)

- **Frameworks & Standards**
  - ISO 27017: Cloud Security Controls
  - CIS Benchmarks (AWS/Azure)
  - NIST CSF (PR.AC, PR.DS, DE.CM)

- **Risiken & Schwachstellen**
  - Misconfigurations
  - Unrestricted Access (0.0.0.0/0)
  - Überprivilegierte IAM-Rollen
  - Fehlende Logging- oder Verschlüsselungseinstellungen

---

## Erwartete Skills
- Durchführung einer **Cloud-Sicherheitsprüfung** (AWS/Azure)  
- Anwendung von **Security-Benchmarks & Standards**  
- Erstellung und Nutzung von **Checklisten & Risiko-Matrizen**  
- **Reporting-Fähigkeiten** für Management und Audit  
- Vergleich von Cloud-Umgebungen im Sicherheitskontext  

---

## Technische Umsetzung
- **Software**
  - AWS Free Tier, Azure Free Account
  - Google Sheets oder LibreOffice Calc (Checklisten)
  - draw.io (Cloud-Architektur-Skizzen)
  - Optional: ScoutSuite, Prowler (AWS CLI Auditing Tools)

- **Hardware**
  - Laptop/PC mit Internetzugang
  - Optional: Virtuelle Testumgebung für Cloud-Accounts

---

## Deliverables
- `cloud-security/checklist_aws.xlsx` – Audit-Checkliste für AWS  
- `cloud-security/checklist_azure.xlsx` – Audit-Checkliste für Azure  
- `cloud-security/compliance_mapping_iso_cis_nist.md` – Framework-Mapping  
- `docs/cloud_risks_playbook.md` – Playbook mit typischen Risiken & Gegenmaßnahmen  
- `report/cloud_assessment_summary.pdf` – Management-tauglicher Risikoüberblick  

---

 
