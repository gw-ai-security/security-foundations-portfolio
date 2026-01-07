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

## Lernziele & erworbene Skills

Nach Abschluss dieses Projekts kannst du:

| Skill | Beschreibung | Relevanz für Karriere |
|-------|--------------|----------------------|
| NIST IR-Lifecycle | Alle Phasen von Preparation bis Lessons Learned | SOC & IR-Teams |
| Severity-Bewertung | Vorfälle nach Impact × Likelihood klassifizieren | Priorisierung & Eskalation |
| Eskalationspfade | Kommunikationswege definieren und visualisieren | Krisenmanagement |
| DSGVO Art. 33 | 72-Stunden-Meldepflicht verstehen und umsetzen | Compliance |
| Playbook-Entwicklung | Standardisierte Handlungsanweisungen erstellen | Security Operations |
| Tabletop-Übungen | Szenarien für Trainings entwickeln | Team-Führung |

---

## Selbstbewertungs-Checkliste

- [ ] Ich kann die 6 Phasen des NIST IR-Lifecycle erklären
- [ ] Ich kann eine Severity-Bewertung durchführen
- [ ] Ich weiß, wann eine DSGVO-Meldepflicht besteht
- [ ] Ich kann ein Incident Reporting Form ausfüllen
- [ ] Ich kann eine Lessons Learned Analyse durchführen
- [ ] Ich kann eine Tabletop-Übung moderieren

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
04_Incident_Response_Playbook/
│
├── README.md                        → Projektbeschreibung, Ziele, Struktur
├── glossar.md                       → Fachbegriffe Incident Response
│
├── docs/
│   ├── ir_lifecycle.md              → Beschreibung des NIST-IR-Lebenszyklus
│   ├── severity_matrix.md           → Klassifikations- & Eskalationsschema
│   ├── escalation_matrix_mermaid.md → Rollen- & Eskalationspfade (Mermaid)
│   ├── incident_reporting_form.md   → Standardisiertes Formular für IR
│   └── gdpr_iso_mapping.md          → ISO 27001 A.16 + DSGVO Art. 33
│
├── scenarios/
│   ├── scenario_phishing.md         → Phishing-Angriff Szenario
│   ├── scenario_ransomware.md       → Ransomware-Angriff Szenario
│   └── scenario_insider_threat.md   → Insider Threat Szenario
│
└── templates/
    ├── incident_response_template.md
    └── lessons_learned_template.md
```

---

## Projekt-Deliverables

| Deliverable | Datei | Status |
|-------------|-------|--------|
| IR-Lifecycle Dokumentation | `docs/ir_lifecycle.md` | ✅ |
| Severity Matrix | `docs/severity_matrix.md` | ✅ |
| Eskalationsmatrix | `docs/escalation_matrix_mermaid.md` | ✅ |
| ISO/DSGVO Mapping | `docs/gdpr_iso_mapping.md` | ✅ |
| Incident Reporting Form | `docs/incident_reporting_form.md` | ✅ |
| Phishing Szenario | `scenarios/scenario_phishing.md` | ✅ |
| Ransomware Szenario | `scenarios/scenario_ransomware.md` | ✅ |
| Insider Threat Szenario | `scenarios/scenario_insider_threat.md` | ✅ |
| IR Template | `templates/incident_response_template.md` | ✅ |
| Lessons Learned Template | `templates/lessons_learned_template.md` | ✅ |
| Glossar | `glossar.md` | ✅ |

---

## Projektstatus

**Status: ✅ ABGESCHLOSSEN**

- [x] IR-Lifecycle dokumentiert
- [x] Eskalationsmatrix erstellt
- [x] Severity-Matrix dokumentiert
- [x] Szenarien ausgearbeitet (Phishing, Ransomware, Insider Threat)
- [x] Reporting-Template finalisiert
- [x] Lessons Learned Template erstellt
- [x] Glossar erstellt

---

## Weiterführende Standards & Quellen
- NIST SP 800-61r2: *Computer Security Incident Handling Guide*
- SANS Institute: *Incident Handler's Handbook*
- ISO/IEC 27001 A.16: *Information Security Incident Management*
- DSGVO Art. 33: *Meldepflicht bei Verletzungen des Schutzes personenbezogener Daten*

---
