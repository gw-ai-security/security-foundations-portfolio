# Incident Response Playbook

## Projektbeschreibung
Dieses Projekt entwickelt ein **vollständiges Incident Response Playbook** auf Basis der Standards  
**NIST SP 800-61r2**, **SANS Incident Handling Framework**, **ISO/IEC 27001 A.16** und **DSGVO Art. 33**.  

Ziel ist es, ein **einsatzfähiges Handbuch** für Audits, Tabletop-Übungen und interne Sicherheitsprozesse zu schaffen.  
Das Playbook bildet den gesamten Lebenszyklus eines Sicherheitsvorfalls ab – von der Vorbereitung bis zu den Lessons Learned.  

---

## Ziele
- Standardisiertes Vorgehen für die Bearbeitung von Security Incidents  
- Einbindung von Rollen, Verantwortlichkeiten und Eskalationspfaden  
- Dokumentation der **Meldepflichten** nach DSGVO (72h-Regel)  
- Erstellung von **realistischen Szenarien** (Phishing, Ransomware, Insider Threat)  
- Audit- und Management-taugliche Reports  

---

## Technische Umsetzung
**Software**
- [VS Code](https://code.visualstudio.com/) oder [Obsidian](https://obsidian.md/) für Dokumentation  
- [draw.io](https://app.diagrams.net/) für Eskalations- & Severity-Matrix  
- Markdown + PDF Export für Reports  
- Optional: Wazuh oder ELK-Stack für Log-Simulationen  

**Hardware**
- Standardrechner ausreichend  
- Optional VM (Ubuntu/Kali) für Szenarien  

---

## Lerninhalte
- **Incident Lifecycle**: Preparation, Detection, Analysis, Containment, Eradication, Recovery, Lessons Learned  
- **Severity & Impact Matrix**: Einstufung von Vorfällen nach Kritikalität  
- **Eskalationspfade**: Rollen, Verantwortlichkeiten, Kommunikationswege  
- **Dokumentations-Templates**: Incident Report, Lessons Learned, Reporting Form  
- **Compliance-Aspekte**: ISO 27001 A.16 & DSGVO Art. 33  

---

## Projektstruktur
```
incident-response-playbook/
│
├── README.md                        → Projektbeschreibung, Ziele, Struktur
│
├── docs/
│   ├── ir_lifecycle.md              → Beschreibung des NIST-IR-Lebenszyklus
│   ├── severity_matrix.md           → Klassifikations- & Eskalationsschema
│   ├── escalation_matrix.drawio     → Rollen- & Eskalationspfade
│   ├── incident_reporting_form.md   → Standardisiertes Formular für IR
│   └── gdpr_iso_mapping.md          → ISO 27001 A.16 + DSGVO Art. 33
│
├── scenarios/
│   ├── scenario_phishing.md
│   ├── scenario_ransomware.md
│   └── scenario_insider_threat.md
│
├── templates/
│   ├── incident_response_template.md
│   └── lessons_learned_template.md
│
└── report/
    └── sample_incident_report.pdf   → Musterdokumentation (fiktiv, realistisch)
```

---

## Deliverables
- **Incident Response Template** (Markdown)  
- **Severity & Escalation Matrix** (draw.io + Markdown)  
- **Mindestens 3 Szenarien** (Phishing, Ransomware, Insider Threat)  
- **Incident Reporting Form** (nach ISO & DSGVO)  
- **Auditfähiger Musterreport** (PDF)  

---

## Projektstatus & KPIs
- [ ] IR-Lifecycle dokumentiert  
- [ ] Eskalationsmatrix erstellt  
- [ ] Severity-Matrix dokumentiert  
- [ ] Szenarien ausgearbeitet  
- [ ] Reporting-Template finalisiert  
- [ ] Musterreport generiert  

**Fertig, wenn:**  
- Alle Dokumente vorhanden und konsistent sind  
- Szenarien in Tabletop-Übungen genutzt werden können  
- Ein vollständiger Muster-Report auditfähig im Repo liegt  

---

## Weiterführende Standards & Quellen
- NIST SP 800-61r2: *Computer Security Incident Handling Guide*  
- SANS Institute: *Incident Handler’s Handbook*  
- ISO/IEC 27001 A.16: *Information Security Incident Management*  
- DSGVO Art. 33: *Meldepflicht bei Verletzungen des Schutzes personenbezogener Daten*  

---
