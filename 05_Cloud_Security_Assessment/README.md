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

## Lernziele & erworbene Skills

Nach Abschluss dieses Projekts kannst du:

| Skill | Beschreibung | Relevanz für Karriere |
|-------|--------------|----------------------|
| Cloud Security Assessment | Systematische Prüfung von AWS/Azure-Umgebungen | Cloud Security Consultant |
| Shared Responsibility | Verantwortlichkeiten zwischen Provider und Kunde verstehen | Cloud-Architektur |
| CIS Benchmarks | Hardening-Standards für Cloud-Konfigurationen anwenden | Compliance & Audit |
| ISO 27017 | Cloud-spezifische Sicherheitskontrollen kennen | Zertifizierungsvorbereitung |
| Risk Assessment | Cloud-Risiken identifizieren und bewerten | Management Reporting |
| Tools (Prowler/ScoutSuite) | Automatisierte Cloud-Security-Scans durchführen | Hands-on Security |  

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
```bash
05-cloud-security-assessment/
│
├── README.md                           # Projektübersicht (bereits erstellt)
├── glossary.md                         # Glossar mit allen Normen & Begriffen
│
├── cloud-security/
│   ├── checklist_aws.xlsx              # Audit-Checkliste für AWS
│   ├── checklist_azure.xlsx            # Audit-Checkliste für Azure
│   └── compliance_mapping_iso_cis_nist.md   # Mapping auf ISO 27017, CIS Benchmarks, NIST CSF
│
├── docs/
│   ├── cloud_risks_playbook.md         # Übersicht typischer Cloud-Risiken & Gegenmaßnahmen
│   ├── methodology.md                  # Beschreibung der Auditmethodik & Tools
│   └── references.md                   # Quellen, Standards, Normen
│
├── diagrams/
│   ├── aws_architecture.drawio         # Beispielhafte Cloud-Architektur (AWS)
│   ├── azure_architecture.drawio       # Beispielhafte Cloud-Architektur (Azure)
│   └── risk_matrix.drawio              # Visualisierung der Risiko-Matrix
│
├── report/
│   ├── cloud_assessment_summary.pdf    # Finaler Management-Report
│   └── cloud_assessment_detailed.md    # Technischer Detailreport (Markdown)
│
└── tools/
    ├── prowler_results/                # Ergebnisse aus Prowler (AWS CLI Audit Tool)
    │   └── example_scan.json
    └── scoutsuite_results/             # Ergebnisse aus ScoutSuite (Multi-Cloud)
        └── example_scan.json
```

## Selbstbewertungs-Checkliste

- [ ] Ich kann das Shared Responsibility Model für IaaS/PaaS/SaaS erklären
- [ ] Ich kenne die Top 5 Cloud-Security-Risiken
- [ ] Ich kann CIS Benchmarks auf AWS/Azure anwenden
- [ ] Ich verstehe ISO 27017 Cloud Controls
- [ ] Ich kann einen Cloud Security Assessment Report erstellen
- [ ] Ich kann Tools wie Prowler oder ScoutSuite nutzen

---

## Projekt-Deliverables

| Deliverable | Datei | Status |
|-------------|-------|--------|
| Compliance Mapping | `cloud_security/compliance_mapping_iso_cis_nist.md` | ✅ |
| Cloud Risks Playbook | `docs/cloud_risks_playbook.md` | ✅ |
| Methodology | `docs/methodology.md` | ✅ |
| References | `docs/references.md` | ✅ |
| AWS Architecture | `diagrams/aws_architecture.md` | ✅ |
| Azure Architecture | `diagrams/azure_architecture.md` | ✅ |
| Risk Matrix | `diagrams/risk_matrix.md` | ✅ |
| Shared Responsibility Model | `diagrams/shared_responsibility_model.md` | ✅ |
| Assessment Report | `report/cloud_security_assessment_report.md` | ✅ |
| Detailed Report | `report/cloud_assessment_detailed.md` | ✅ |
| Glossary | `glossary.md` | ✅ |
| AWS CLI Commands | `tools/aws_cli_commands.md` | ✅ |

**Status: ✅ ABGESCHLOSSEN**  

---

 
