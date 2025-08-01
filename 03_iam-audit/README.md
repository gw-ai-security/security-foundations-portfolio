# Projekt 3: Identity & Access Management (IAM) Audit

## Ziel

Ziel dieses Projekts ist der Aufbau eines vollständigen IAM-Audit-Templates zur strukturierten Analyse und Dokumentation von Rollen, Rechten und Zugriffspfaden innerhalb einer Organisation.  
Das Template ist auditfähig, ISO 27001- und DSGVO-konform und eignet sich als Grundlage für Access Reviews, Rezertifizierungen und Rollenbereinigungen.

---

## Lern- & Umsetzungsschwerpunkte

- Aufbau und Pflege einer **Rechtematrix** (z. B. mit Google Sheets oder LibreOffice)
- Entwicklung eines **Rollenmodells** mit Zugriffspfaden (draw.io)
- **Risikobewertung** nach Impact & Exposure (z. B. Admin-Zugriffe)
- **Mapping auf ISO 27001 (A.9)** und DSGVO (Art. 5(1)(f), Art. 32)
- Dokumentation und **Audit-Report** im PDF-Format

---

## Skills

| Kompetenzbereich         | Beschreibung                                                |
|--------------------------|--------------------------------------------------------------|
| Least Privilege Prinzip  | Minimierung von Zugriffen auf das Notwendige                |
| Rollenmodellierung       | Abbildung realer Organisationsrollen in Zugriffshierarchien |
| Risikoeinschätzung       | Bewertung kritischer Rechte nach Vertraulichkeit/Integrität |
| Audit-Vorbereitung       | Strukturierte Dokumentation für interne/externe Audits      |
| Datenschutzkonformität   | DSGVO-konformes Berechtigungsmanagement                     |

---

## Tools & Technologien

- **Google Sheets / LibreOffice Calc** – Rechtematrix
- **draw.io (diagrams.net)** – Rollenmodellierung
- **VS Code / Obsidian / Markdown** – Dokumentation
- **LibreOffice / Google Docs** – PDF-Erstellung

---

## Projektstruktur

```bash
03_iam-audit/
├── README.md                         # Projektbeschreibung, Ziel, Toolchain
├── iam-audit/
│   ├── rechte_matrix_template.xlsx  # Zugriffsmatrix mit Bewertung
│   ├── rollenmodell.drawio          # Visuelle Darstellung der Rollen
│   └── gdpr_iso_mapping.md          # Mapping auf ISO 27001 / DSGVO
├── docs/
│   └── access_review_guide.md       # Leitfaden zur Access Review Durchführung
├── report/
│   └── iam_audit_sample.pdf         # Fiktiver Beispielreport für Audits
``` 
