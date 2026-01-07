# Projekt 2: Firewall Rule Audit Template

Dieses Projekt liefert eine auditfähige, risikobasierte Checklisten-Vorlage zur Bewertung von Firewall-Regelwerken in Netzwerken. Ziel ist es, Sicherheitslücken durch fehlkonfigurierte, überflüssige oder zu weit gefasste Regeln systematisch zu identifizieren und auf Basis von ISO/IEC 27001 und NIST CSF zu bewerten.

---

## Projektziel

- Erstellung eines standardisierten Firewall-Audit-Templates
- Bewertung von Regeln nach Risiko (Impact × Likelihood)
- Dokumentation von Schwachstellen und Handlungsempfehlungen
- Auditfähigkeit für interne und externe Prüfungen (z. B. ISO 27001)

---

## Projektstruktur

```plaintext
firewall-audit/
├── README.md                            # Diese Projektbeschreibung
├── firewall_checklist_template.xlsx     # Haupt-Checkliste mit Regelbewertung
├── firewall_risk_matrix.xlsx            # Bewertungsmatrix für Impact & Likelihood
├── docs/
│   ├── firewall_audit_guide.md          # Anleitung zur Durchführung
│   └── mapping_iso_nist.md              # Controls-Mapping ISO/NIST
└── report/
    └── firewall_audit_report.pdf        # Musterreport für Dokumentation
```

## Eingesetzte Tools

| Tool                    | Zweck                                      |
|-------------------------|---------------------------------------------|
| Google Sheets / Excel   | Checkliste und Filterfunktionen             |
| VS Code / Obsidian      | Markdown-Dokumentation                      |
| draw.io / diagrams.net  | Visualisierung von Netzwerkzonen            |
| LibreOffice / PDF Export| Erstellung finaler Reports                  |

Alle verwendeten Tools sind kostenfrei nutzbar.

---

## Inhalt der Audit-Checkliste

Die Datei `firewall_checklist_template.xlsx` enthält u. a. folgende Spalten:

- **Rule ID**  
- **Beschreibung der Regel**  
- **Quelle / Ziel / Port / Protokoll / Richtung**  
- **Risikoeinschätzung**: Hoch / Mittel / Niedrig  
- **Empfehlungen**: z. B. Einschränkung, Logging, Entfernung  
- **Freigabe / Review-Feld**

---

## Risikobewertung

Die Datei `firewall_risk_matrix.xlsx` unterstützt die systematische Bewertung nach:

- **Impact**: Mögliche Auswirkung bei Missbrauch  
- **Likelihood**: Eintrittswahrscheinlichkeit  

Daraus ergibt sich der **Risikolevel**: Hoch / Mittel / Niedrig

---

## Mapping auf Standards

| Framework      | Relevanter Control / Maßnahme                             |
|----------------|------------------------------------------------------------|
| ISO/IEC 27001  | A.13.1.1 – Maßnahmen zur Netzwerksicherheit                |
| NIST CSF       | PR.AC-5 (Access Control), DE.CM-7 (Monitoring Network Activity) |

Weitere Details: siehe [`docs/mapping_iso_nist.md`](./docs/mapping_iso_nist.md)

---

## Ablauf der Audit-Durchführung

1. **Export oder Sichtung** des aktuellen Firewall-Regelwerks  
2. **Übertragung** in die Checkliste (`firewall_checklist_template.xlsx`)  
3. **Bewertung** jeder Regel gemäß Risiko-Matrix  
4. **Empfehlungen** pro Regel eintragen  
5. **Review** mit Freigabevermerk (Name + Datum)  
6. **PDF-Erstellung** des Auditberichts (siehe `report/`)  
7. **Optional**: Visualisierung der Netzwerkzonen mit draw.io  

Anleitung: siehe [`docs/firewall_audit_guide.md`](./docs/firewall_audit_guide.md)

---

## Beispielhafte Schwachstellen

- `ANY → ANY → ALLOW`
- Offene Admin-Ports (z. B. RDP, SSH) aus externen Quellen
- Doppelte oder widersprüchliche Regeln
- Fehlende Kommentare oder Review-Dokumentation
- Unklare Zuständigkeit ("Rule Ownership")

---

## Deliverables

| Datei                          | Zweck                                             | Status |
|--------------------------------|----------------------------------------------------| ------ |
| `docs/firewall_audit_guide.md`         | Schritt-für-Schritt-Anleitung zur Durchführung    | ✅ |
| `docs/mapping_iso_nist.md`             | Regulatorische Verankerung (ISO/NIST Mapping)     | ✅ |
| `docs/mapping_iso_nist_v1.1.md`        | Erweitertes Mapping für ISO 27001:2022           | ✅ |
| `reports/firewall_audit_report.md`     | Dokumentierter, auditfähiger Ergebnisreport       | ✅ |
| `glossary.md`                          | Fachbegriffe Firewall & Netzwerk-Security        | ✅ |

---

## Nutzung & Lizenz

- Alle Inhalte stehen unter der **MIT-Lizenz**
- Frei verwendbar mit Attribution
- Die Excel-Vorlagen sind individuell anpassbar für unterschiedliche Infrastrukturen
- Entwickelt für Schulungs-, Consulting- und Audit-Zwecke

---

---

## Lernziele & erworbene Skills

Nach Abschluss dieses Projekts kannst du:

| Skill | Beschreibung | Relevanz für Karriere |
|-------|--------------|----------------------|
| Firewall-Regelwerke analysieren | Regeln systematisch bewerten und dokumentieren | Core Security Skill |
| Risikobewertung | Impact × Likelihood Matrix anwenden | Grundlage für Priorisierung |
| Compliance-Mapping | ISO 27001 & NIST CSF Controls zuordnen | Audit-Vorbereitung |
| Auditfähige Dokumentation | Professionelle Reports erstellen | Interview- & Portfolio-Ready |
| Netzwerk-Security Grundlagen | Paketfilter, Zonen, ACLs verstehen | Basis für Network Security |

---

## Selbstbewertungs-Checkliste

Prüfe nach Abschluss des Projekts:

- [ ] Ich kann eine Firewall-Regel anhand von Quelle/Ziel/Port/Protokoll beschreiben
- [ ] Ich verstehe den Unterschied zwischen Stateful und Stateless Firewalls
- [ ] Ich kann eine Risikobewertung (Impact × Likelihood) durchführen
- [ ] Ich weiß, welche ISO 27001 Controls für Netzwerksicherheit relevant sind
- [ ] Ich kann typische Schwachstellen in Firewall-Konfigurationen erkennen
- [ ] Ich kann einen auditfähigen Firewall-Report erstellen

---

## Weiterentwicklung

**Geplante Erweiterungen:**

- Integration eines Regelparsers (CSV → XLSX automatisiert)
- Beispielkonfigurationen auf Basis von OPNsense / pfSense
- Automatisierte Visualisierung von Regelwerken (draw.io oder Python + Graphlib)

---

