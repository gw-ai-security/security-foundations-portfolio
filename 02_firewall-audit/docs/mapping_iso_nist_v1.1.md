# Mapping ISO/IEC 27001:2022 & NIST CSF 2.0 – Firewall Rule Audit (Projekt 2)

Zweck: Konsistentes Cross‑Mapping der Projekt‑Artefakte aus **Projekt 2 – Firewall Rule Audit** auf **ISO/IEC 27001:2022 (Annex A)**, **NIST CSF 2.0** sowie **GDPR Art. 32**. Dieses Mapping ersetzt ältere Verweise (ISO 27001:2013) und ist „audit‑ready“ formuliert.

---

## Wie du dieses Mapping nutzt
- **Planung & SoA**: Nutze die ISO‑Kontrollreferenzen für deine Statement‑of‑Applicability (SoA) und Policies.
- **Review**: Nutze die NIST‑CSF‑Kategorien als „Outcome‑Sprache“ für Management‑Berichte und Reifegrad.
- **GDPR‑Kontext**: Art. 32 wird dort referenziert, wo Netzschutz und TOMs unmittelbar betroffen sind.
- **Evidence**: Jede Zeile verweist auf die passenden Projekt‑Artefakte (Checkliste, Guide, Report, CSV).

---

## Crosswalk (Firewall‑Themen → ISO 27001:2022 / NIST CSF 2.0 / GDPR Art. 32 / Evidence)

| Firewall‑Thema | ISO/IEC 27001:2022 Annex A (Auszug) | NIST CSF 2.0 (Kategorie‑Ebene) | GDPR Art. 32 Bezug | Evidence in Projekt 2 |
|---|---|---|---|---|
| Governance & Policy für Netzwerk/Firewalls | **5.1 Policies for information security**, 5.36 Compliance mit Policies | **GV.PO** (Policy), **GV.OV** (Oversight), **GV.RM** (Risk Mgmt) | „angemessenes Schutzniveau“, risikobasiert, regelmäßige Überprüfung | `README.md`, `firewall_audit_guide.md` |
| Asset‑/Service‑Inventar & Rule‑Owner | **5.9 Inventory of information & other associated assets** | **ID.AM** (Asset Mgmt) | „Stand der Technik“, „Kontext & Zwecke“ | `firewall_checklist_template.csv` |
| Baseline: Default‑Deny Inbound, Allowlist Egress (Ports/Protokolle/IPs) | **8.20 Network security**, **8.21 Security of network services** | **PR.PS** (Platform Security), **PR.DS** (Data Security) | Vertraulichkeit/Integrität/Verfügbarkeit (CIA) | `firewall_audit_guide.md`, `firewall_risk_matrix.csv` |
| Netzwerk‑Segmentierung & Zonen (DMZ/Intern/Extern) | **8.22 Segregation in networks** (inkl. VLAN/VRF/SDN‑Segregation) | **PR.PS** | „geeignete Maßnahmen“ zur Eingrenzung von Risiken | `firewall_audit_guide.md`, Diagramm optional |
| Regel‑Lebenszyklus & Change‑Management | **8.9 Configuration management** | **PR.MA** (Maintenance), **GV.OV** | Wirksamkeit der TOMs, regelmäßige Tests | `firewall_checklist_template.csv` (Change‑Felder), `firewall_audit_report.md` |
| Admin‑Zugriff, MFA, Least‑Privilege auf Firewalls | **5.16 Identity management**, **5.17 Authentication information**, **5.18 Access rights** | **PR.AA** (Identity Mgmt, Authn & Access) | Zugriffskontrolle als TOM | `firewall_audit_guide.md` |
| Protokollierung (Rule‑Hits, Drops, Policy‑Änderungen) | **8.15 Logging** | **DE.CM** (Continuous Monitoring) | Nachweis/Beweisführung, Integrität von Logs | `firewall_audit_guide.md`, `firewall_audit_report.md` |
| Sicherheitsüberwachung & Korrelation (SIEM) | **8.16 Monitoring activities** | **DE.CM**, **RS.AN/RS.MA** (Analyse & Incident Mgmt) | Erkennung/Behandlung von Sicherheitsvorfällen | `firewall_audit_guide.md`, `firewall_risk_matrix_flat.csv` |
| Schwachstellen/Hotfixes (Firmware/OS/Module) | **8.8 Management of technical vulnerabilities** | **ID.RA** (Risk Assessment), **PR.MA** | „Stand der Technik“ bei Patches | `firewall_checklist_template.csv` |
| Sichere Baselines (CIS Hardening, No‑Any‑Any) | **8.9 Configuration management** | **PR.PS** | „angemessene Maßnahmen“ | `firewall_audit_guide.md`, `firewall_audit_report.md` |
| Lieferanten/Ketten (Managed Firewall, Cloud Edges) | **5.19/5.20/5.21 Supplier & ICT supply chain** | **GV.SC** (Cyber SCRM) | vertragliche/organisatorische TOMs | `README.md` |
| Business‑Continuity‑Bezug (z. B. Rule‑Restore) | **5.30 ICT readiness for business continuity** | **PR.IR** (Tech Infrastructure Resilience), **RC.RP/RC.CO** | Verfügbarkeit & Wiederherstellung | `firewall_audit_report.md` |

> Hinweis: Frühere ISO 27001:2013‑Verweise (z. B. A.13.1.x „Network security“) werden in der 2022‑Struktur vorrangig durch **A.8.20/8.21/8.22** abgedeckt.  

---

## Minimal‑Mapping je Prüfpunkt (konkret umsetzbar)

- **„Any‑Any identifizieren und entfernen“** → ISO: 8.20/8.22; NIST: PR.PS; GDPR: Art. 32(1) a–d. Evidence: Checkliste‑Felder „Quelle/Ziel/Port“, Report‑Finding.  
- **„Egress‑Filter auf bekannte Ziele/Ports“** → ISO: 8.20/8.21; NIST: PR.PS; GDPR: Art. 32. Evidence: Risk‑Matrix‑Eintrag, Rule‑Hit‑Statistik.  
- **„Admin‑Plane‑Absicherung (SSH v2, MFA, mgmt‑VRF)“** → ISO: 5.16/5.17/5.18, 8.20; NIST: PR.AA/PR.PS; GDPR: Art. 32(1)(b). Evidence: Guide‑Kapitel „Betriebsrichtlinien“, Report‑Kontrolltest.  
- **„Logging & Korrelation im SIEM“** → ISO: 8.15/8.16; NIST: DE.CM, RS.AN; GDPR: Art. 32(1)(d) Test/Assess/Evaluate. Evidence: Report‑Screenshots/Tabellen, CSV‑Export.  
- **„Regel‑Change nur via Ticket & 4‑Augen“** → ISO: 8.9, 5.36; NIST: GV.OV, PR.MA; GDPR: Nachweis der Wirksamkeit. Evidence: Checkliste‑Spalten „Owner/Approver/Datum“.  

---

## Migrationsnotiz (2013 → 2022)
- **Netzwerkbezogene 2013‑Kontrollen** (u. a. A.13.1.1/13.1.3) mappen in **A.8.20 (Network security), A.8.21 (Security of network services), A.8.22 (Segregation in networks)** der 2022‑Version.  
- Organisations‑ und Zugriffskontrollen liegen heute zentral in **A.5.15–A.5.18** (Access, Identity, Authn‑Information, Access Rights).  
- Logging/Monitoring ist in **A.8.15/A.8.16** gebündelt; Konfiguration/Hardening in **A.8.9**.

---

## Evidence‑Referenzen (Projekt 2)

- `firewall_audit_guide.md` – Vorgehen, Prüffragen, Kontrollziele  
- `firewall_checklist_template.csv` – Regeln/Owner/Änderungen/Risiko  
- `firewall_risk_matrix.csv` & `firewall_risk_matrix_flat.csv` – Bewertung/Heatmap  
- `firewall_audit_report.md` – Findings, Maßnahmen, KPI‑Hook  
- `README.md` – Scope, Struktur, Compliance‑Hinweise

---

## Lizenz
Empfehlung: **MIT** (für Templates/Dokumente). Alternativ **CC BY‑SA 4.0** für Text‑Werke; konsistent im Repo halten.

---

*Version: 1.1 (20‑08‑2025)*
