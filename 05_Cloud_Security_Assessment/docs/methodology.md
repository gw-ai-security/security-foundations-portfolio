# Methodology – Projekt 5: Cloud Security Assessment Framework

Dieses Dokument beschreibt die Vorgehensweise und Methodik für die Durchführung eines Cloud Security Assessments.  
Es basiert auf aktuellen Best Practices, Standards und professionellen Consulting-Ansätzen im Bereich Cloud Security.  

---

## 1. Scope & Objectives
- **Scope:** AWS und Azure Free Tier Accounts, Fokus auf IAM, Storage, Netzwerk und Logging.  
- **Zielsetzung:**  
  - Identifikation von Fehlkonfigurationen (Misconfigurations)  
  - Bewertung von Risiken nach Impact & Likelihood  
  - Mapping auf internationale Standards (ISO 27017, CIS Benchmarks, NIST CSF)  
  - Erstellung eines Audit-Reports mit Management Summary  

---

## 2. Frameworks & Standards als Basis
- **ISO/IEC 27017** – Cloud Security Controls  
- **CIS Benchmarks** – AWS und Azure Hardening Guides  
- **NIST Cybersecurity Framework (CSF)** – Identify, Protect, Detect, Respond, Recover  
- **GDPR (DSGVO)** – Art. 28 (Auftragsverarbeiter), Art. 32 (Sicherheit der Verarbeitung)  

Diese Standards dienen als **Referenzrahmen** für die Bewertung und Dokumentation der Cloud Security Controls.  

---

## 3. Assessment Workflow

### Schritt 1: Informationssammlung
- Cloud-Architektur verstehen (Diagramme: Netzwerk, IAM, Storage)  
- Bestehende Policies, Security Groups und Berechtigungen dokumentieren  
- Quellen: AWS Config, Azure Policy, Manuelle Konfigurationen  

### Schritt 2: Konfigurationsprüfung
- Durchführung automatisierter Checks mit:  
  - **Prowler (AWS CLI Audit Tool)**  
  - **ScoutSuite (Multi-Cloud Security Tool)**  
- Ergebnisse in JSON/CSV exportieren und archivieren  

### Schritt 3: Risikoanalyse
- Identifizierung kritischer Findings (z. B. offene Ports, überprivilegierte Rollen, unverschlüsselte Daten)  
- Bewertung nach **Impact (Hoch/Mittel/Niedrig)** und **Likelihood**  
- Visualisierung in einer **Risk Matrix**  

### Schritt 4: Compliance Mapping
- Abgleich der Findings mit:  
  - ISO 27017 Controls  
  - CIS Benchmarks  
  - NIST CSF Functions  
- Erstellung eines **compliance_mapping_iso_cis_nist.md** als Deliverable  

### Schritt 5: Reporting
- **Technischer Detailreport (Markdown)** für Security Teams  
- **Management Summary (PDF)** mit KPIs, Risiko-Heatmap und Handlungsempfehlungen  
- Fokus: Umsetzbare Maßnahmen und Priorisierung  

---

## 4. Tools & Deliverables

**Tools**  
- Prowler (AWS CLI Auditing)  
- ScoutSuite (AWS/Azure Multi-Cloud Checks)  
- Google Sheets / LibreOffice Calc (Checklisten, Risk Matrix)  
- draw.io (Architektur- & Risiko-Diagramme)  
- VS Code / Obsidian (Dokumentation, Markdown, PDF Export)  

**Deliverables**  
- `checklist_aws.xlsx` – AWS Security Audit Checkliste  
- `checklist_azure.xlsx` – Azure Security Audit Checkliste  
- `compliance_mapping_iso_cis_nist.md` – Mapping der Findings zu Standards  
- `cloud_risks_playbook.md` – Übersicht typischer Risiken & Controls  
- `cloud_assessment_summary.pdf` – Auditfähiger Report für das Management  

---

## 5. Qualitäts- und Audit-Kriterien
- **Nachvollziehbarkeit:** Alle Findings sind dokumentiert, inkl. Screenshots/JSON-Exports.  
- **Reproduzierbarkeit:** Tools, Versionen und Befehle sind dokumentiert.  
- **Compliance-Fokus:** Jede Empfehlung ist an ISO/NIST/CIS/DSGVO gemappt.  
- **Audit-Readiness:** Reports erfüllen Standards für externe Prüfungen und Interviews.  

---

## 6. Executive Alignment
Das Assessment liefert sowohl **technische Details für Security Teams** als auch **Management-fähige Reports**.  
Damit ist es **CISO-Ready**, auditfähig und praxisorientiert für Banken, Versicherungen und regulierte Branchen.  
