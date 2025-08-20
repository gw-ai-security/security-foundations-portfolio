# Mapping Incident Response Playbook – ISO 27001 & DSGVO

Dieses Dokument zeigt, wie das Incident Response Playbook die Anforderungen der **ISO/IEC 27001:2017 (Annex A.16)** und der **DSGVO (Art. 33 & 34)** erfüllt.  
Es dient als Compliance-Nachweis für Audits und Management-Reviews.

---

## ISO/IEC 27001 – Annex A.16 (Information Security Incident Management)

| ISO 27001 Control | Anforderung | Abdeckung im Playbook |
|-------------------|-------------|------------------------|
| **A.16.1.1** Verantwortlichkeiten und Verfahren | Incident-Response-Prozesse müssen definiert und dokumentiert sein | `ir_lifecycle.md`, `README.md` |
| **A.16.1.2** Melden von Informationssicherheitsereignissen | Mitarbeiter und Partner müssen Sicherheitsereignisse melden können | `incident_reporting_form.md` |
| **A.16.1.3** Melden von Schwachstellen | Schwachstellen müssen gemeldet und dokumentiert werden | `incident_reporting_form.md`, Szenarien (Phishing, Ransomware) |
| **A.16.1.4** Bewertung und Entscheidung über Informationssicherheitsereignisse | Ereignisse müssen bewertet und klassifiziert werden | `severity_matrix.md`, Szenarien |
| **A.16.1.5** Reaktion auf Informationssicherheitsvorfälle | Maßnahmen zur Behandlung von Vorfällen müssen definiert sein | `scenarios/*.md` |
| **A.16.1.6** Erfassung von Nachweisen | Forensische Beweise müssen gesichert werden | Szenarien (Ransomware, Insider Threat) |
| **A.16.1.7** Lessons Learned | Aus Vorfällen müssen Verbesserungen abgeleitet werden | `lessons_learned_template.md` |
| **A.16.1.8** Sammlung von Informationen | Organisationen müssen Trends und Statistiken dokumentieren | `sample_incident_report.pdf`, KPIs |
| **A.16.1.9** Kommunikation | Kommunikationsprozesse müssen definiert sein | `escalation_matrix.drawio`, Szenarien |

---

## DSGVO – Artikel 33 & 34

| DSGVO Artikel | Anforderung | Abdeckung im Playbook |
|---------------|-------------|------------------------|
| **Art. 33 Abs. 1** | Verletzungen des Schutzes personenbezogener Daten müssen binnen 72 Stunden an die Aufsichtsbehörde gemeldet werden | `incident_reporting_form.md`, Szenarien |
| **Art. 33 Abs. 3** | Meldung muss Art, Umfang, Folgen und Maßnahmen enthalten | `incident_reporting_form.md`, `sample_incident_report.pdf` |
| **Art. 33 Abs. 5** | Verantwortlicher muss Nachweise zur Erfüllung der Meldepflicht führen | `sample_incident_report.pdf`, Dokumentation aller Szenarien |
| **Art. 34 Abs. 1** | Betroffene Personen müssen bei hohem Risiko informiert werden | Szenarien (Ransomware, Insider Threat) |
| **Art. 34 Abs. 3** | Ausnahme, wenn Daten verschlüsselt oder Maßnahmen das Risiko minimieren | Szenarien (Ransomware), Lessons Learned |

---

## Fazit
Das Incident Response Playbook deckt die Anforderungen von **ISO/IEC 27001 A.16** und **DSGVO Art. 33/34** ab.  
Die enthaltenen Dokumente (Lifecycle, Severity Matrix, Eskalationsmatrix, Szenarien, Templates und Incident Report) bieten eine vollständige Compliance-Grundlage für interne und externe Audits.

---
