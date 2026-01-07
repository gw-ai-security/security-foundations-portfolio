# Projekt 7 – GRC Dashboard (Governance, Risk & Compliance)

## Überblick

Dieses Projekt implementiert ein vollständiges **GRC Dashboard** zur zentralen Steuerung von Governance, Risikomanagement und Compliance. Es integriert **Business Continuity & Disaster Recovery (BCDR)** und bildet die Grundlage für Executive-Level Security Reporting.

Das Dashboard ermöglicht die Visualisierung von Risiken, Compliance-Status und KPIs auf Management-Ebene und ist konform mit **ISO 27001**, **NIST CSF**, **GDPR** und dem **EU AI Act**.

---

## Projektziele

- Aufbau eines **Risk Registers** mit Risikobewertung und Maßnahmenverfolgung
- Entwicklung eines **KPI-Dashboards** für Security Metrics
- Erstellung eines **Business Impact Analysis (BIA)** Templates
- **Compliance-Mapping** für ISO 27001, GDPR und EU AI Act
- Integration von **BCDR-Planung** (Business Continuity & Disaster Recovery)
- Erstellung **auditfähiger Management-Reports**

---

## Lernziele & erworbene Skills

Nach Abschluss dieses Projekts kannst du:

| Skill | Beschreibung | Relevanz für Karriere |
|-------|--------------|----------------------|
| Risk Management | Risiken identifizieren, bewerten und behandeln | CISO / Risk Manager |
| KPI Design | Security-Metriken definieren und visualisieren | Executive Reporting |
| Compliance Management | Multi-Framework Compliance steuern | GRC Analyst |
| BIA durchführen | Kritische Geschäftsprozesse identifizieren | BCDR Planning |
| BCDR Planning | Recovery-Strategien entwickeln | Business Continuity |
| Executive Reporting | Management-taugliche Reports erstellen | C-Level Communication |
| EU AI Act | KI-Risikokategorien verstehen und anwenden | AI Governance |

---

## Selbstbewertungs-Checkliste

- [ ] Ich kann ein Risk Register erstellen und pflegen
- [ ] Ich verstehe den Unterschied zwischen inherent und residual risk
- [ ] Ich kann Security KPIs definieren und interpretieren
- [ ] Ich kann eine Business Impact Analysis durchführen
- [ ] Ich kenne die RTO/RPO-Konzepte
- [ ] Ich kann ISO 27001, GDPR und EU AI Act Controls mappen
- [ ] Ich kann einen Executive GRC Report schreiben

---

## Projektstruktur

```bash
07_GRC_Dashboard/
│
├── README.md                           # Projektbeschreibung
├── glossary.md                         # GRC-Fachbegriffe
│
├── docs/
│   ├── risk_management_methodology.md  # Risikomanagement-Methodik
│   ├── kpi_framework.md                # KPI-Definitionen & Metriken
│   ├── bia_guide.md                    # Business Impact Analysis Guide
│   ├── bcdr_planning.md                # Business Continuity & DR Planung
│   ├── compliance_mapping.md           # ISO/GDPR/AI Act Mapping
│   └── practical_exercises.md          # Praktische Übungen
│
├── templates/
│   ├── risk_register.md                # Risk Register Template
│   ├── bia_template.md                 # BIA Template
│   ├── bcdr_plan_template.md           # BCDR Plan Template
│   └── kpi_dashboard.md                # KPI Dashboard Template
│
├── diagrams/
│   ├── risk_matrix.md                  # Risiko-Matrix (Mermaid)
│   ├── grc_architecture.md             # GRC-Architektur Diagramm
│   └── bcdr_timeline.md                # Recovery Timeline
│
└── reports/
    └── grc_executive_summary.md        # Management Report
```

---

## Projekt-Deliverables

| Deliverable | Datei | Status |
|-------------|-------|--------|
| Risk Management Methodology | `docs/risk_management_methodology.md` | ✅ |
| KPI Framework | `docs/kpi_framework.md` | ✅ |
| BIA Guide | `docs/bia_guide.md` | ✅ |
| BCDR Planning | `docs/bcdr_planning.md` | ✅ |
| Compliance Mapping | `docs/compliance_mapping.md` | ✅ |
| Practical Exercises | `docs/practical_exercises.md` | ✅ |
| Risk Register Template | `templates/risk_register.md` | ✅ |
| BIA Template | `templates/bia_template.md` | ✅ |
| BCDR Plan Template | `templates/bcdr_plan_template.md` | ✅ |
| KPI Dashboard | `templates/kpi_dashboard.md` | ✅ |
| Risk Matrix Diagram | `diagrams/risk_matrix.md` | ✅ |
| GRC Architecture | `diagrams/grc_architecture.md` | ✅ |
| Executive Report | `reports/grc_executive_summary.md` | ✅ |
| Glossary | `glossary.md` | ✅ |

**Status: ✅ ABGESCHLOSSEN**

---

## Technische Umsetzung

### Software
- **Dokumentation:** Markdown (VS Code, Obsidian)
- **Diagramme:** Mermaid, draw.io
- **Tabellen:** Markdown Tables, Google Sheets
- **Visualisierung:** KPI-Charts in Markdown/HTML
- **PDF Export:** LibreOffice, Obsidian

### Frameworks & Standards
- ISO/IEC 27001:2022 (ISMS)
- ISO 22301 (Business Continuity)
- NIST Cybersecurity Framework 2.0
- NIST SP 800-30 (Risk Assessment)
- GDPR (EU 2016/679)
- EU AI Act (2024)

---

## GRC Framework Übersicht

```
┌─────────────────────────────────────────────────────────────────┐
│                        GRC DASHBOARD                             │
├─────────────────┬─────────────────┬─────────────────────────────┤
│   GOVERNANCE    │      RISK       │         COMPLIANCE          │
├─────────────────┼─────────────────┼─────────────────────────────┤
│ • Policies      │ • Risk Register │ • ISO 27001                 │
│ • Procedures    │ • Risk Matrix   │ • GDPR                      │
│ • Roles & Resp. │ • Risk Treatment│ • EU AI Act                 │
│ • Oversight     │ • KRIs          │ • NIST CSF                  │
├─────────────────┴─────────────────┴─────────────────────────────┤
│                    BUSINESS CONTINUITY                           │
├─────────────────────────────────────────────────────────────────┤
│ • BIA (Business Impact Analysis)                                 │
│ • BCDR Planning (Recovery Strategies)                            │
│ • RTO/RPO Definitions                                            │
│ • Testing & Exercises                                            │
└─────────────────────────────────────────────────────────────────┘
```

---

## Weiterführende Standards & Quellen

| Standard | Beschreibung | Link |
|----------|--------------|------|
| ISO 27001:2022 | Information Security Management | https://www.iso.org/standard/27001 |
| ISO 22301 | Business Continuity Management | https://www.iso.org/standard/75106.html |
| NIST CSF 2.0 | Cybersecurity Framework | https://www.nist.gov/cyberframework |
| NIST SP 800-30 | Risk Assessment Guide | https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final |
| GDPR | EU Datenschutz-Grundverordnung | https://gdpr.eu/ |
| EU AI Act | KI-Verordnung | https://artificialintelligenceact.eu/ |

---

## Karriere-Relevanz

| Rolle | Relevante Skills aus diesem Projekt |
|-------|-------------------------------------|
| **CISO** | Risk Management, Executive Reporting, Compliance Oversight |
| **GRC Manager** | Risk Register, Compliance Mapping, KPI Framework |
| **Risk Analyst** | Risk Assessment, BIA, Risk Treatment |
| **Compliance Officer** | Multi-Framework Mapping, Audit Preparation |
| **BCM Manager** | BCDR Planning, RTO/RPO, Recovery Strategies |

---
