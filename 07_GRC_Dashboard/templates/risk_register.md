# Risk Register Template

## Übersicht

Das Risk Register ist das zentrale Dokument zur Erfassung, Bewertung und Verfolgung aller identifizierten Informationssicherheitsrisiken. Es wird regelmäßig aktualisiert und dient als Grundlage für Management-Entscheidungen und Audits.

---

## Metadaten

| Feld | Wert |
|------|------|
| **Organisation** | [Organisation Name] |
| **Version** | 1.0 |
| **Erstellt am** | [Datum] |
| **Letzte Aktualisierung** | [Datum] |
| **Nächste Review** | [Datum] |
| **Verantwortlich** | [Risk Manager Name] |
| **Klassifikation** | Vertraulich |

---

## Risk Register

### Legende

| Feld | Beschreibung |
|------|--------------|
| **Risk ID** | Eindeutige Kennung (z.B. R-2026-001) |
| **L** | Likelihood (1-5) |
| **I** | Impact (1-5) |
| **Score** | L × I (1-25) |
| **Status** | Open / In Treatment / Closed / Accepted |

---

## Aktive Risiken

| Risk ID | Risiko-Beschreibung | Kategorie | L | I | Inherent Score | Treatment | Residual L | Residual I | Residual Score | Risk Owner | Target Date | Status |
|---------|---------------------|-----------|---|---|----------------|-----------|------------|------------|----------------|------------|-------------|--------|
| R-2026-001 | Ransomware-Angriff auf produktive Systeme durch Phishing-E-Mails | Technisch | 4 | 5 | **20 (Critical)** | Mitigate | 2 | 4 | **8 (Medium)** | IT Security | 2026-03-31 | In Treatment |
| R-2026-002 | Unbefugter Zugriff auf Kundendaten durch kompromittierte Zugangsdaten | Compliance | 3 | 5 | **15 (High)** | Mitigate | 2 | 4 | **8 (Medium)** | IAM Team | 2026-02-28 | In Treatment |
| R-2026-003 | Ausfall des primären Rechenzentrums durch Stromausfall | Operativ | 2 | 5 | **10 (Medium)** | Transfer | 2 | 3 | **6 (Medium)** | IT Ops | 2026-06-30 | Open |
| R-2026-004 | Verlust von Geschäftsgeheimnissen durch Insider Threat | Menschlich | 2 | 4 | **8 (Medium)** | Mitigate | 1 | 3 | **3 (Low)** | HR/Security | 2026-04-30 | In Treatment |
| R-2026-005 | GDPR-Verstoß durch fehlerhafte Datenverarbeitung | Compliance | 3 | 4 | **12 (High)** | Mitigate | 2 | 3 | **6 (Medium)** | DPO | 2026-03-15 | Open |
| R-2026-006 | Supply Chain Compromise durch kompromittierte Drittanbieter-Software | Extern | 3 | 4 | **12 (High)** | Mitigate | 2 | 3 | **6 (Medium)** | Procurement | 2026-05-31 | Open |
| R-2026-007 | KI-System-Fehlfunktion mit Auswirkung auf automatisierte Entscheidungen | AI Risk | 3 | 3 | **9 (Medium)** | Mitigate | 2 | 2 | **4 (Low)** | AI Team | 2026-04-30 | Open |

---

## Risk Treatment Details

### R-2026-001: Ransomware-Angriff

**Beschreibung:**
Angreifer nutzen Phishing-E-Mails, um Ransomware auf Endgeräte zu bringen. Bei erfolgreicher Ausführung werden produktive Systeme und Daten verschlüsselt.

**Ursachen:**
- Unzureichende E-Mail-Filterung
- Mangelndes Security Awareness bei Mitarbeitern
- Fehlende Endpoint Detection & Response (EDR)

**Maßnahmen:**

| Maßnahme | Verantwortlich | Deadline | Status | Wirksamkeit |
|----------|----------------|----------|--------|-------------|
| E-Mail-Security-Gateway mit Advanced Threat Protection | IT Security | 2026-02-15 | In Progress | Hoch |
| Security Awareness Training (Phishing-Simulation) | HR/Security | 2026-01-31 | Completed | Mittel |
| EDR-Lösung auf allen Endgeräten | IT Ops | 2026-03-31 | Planned | Hoch |
| Offline-Backup-Strategie implementieren | IT Ops | 2026-02-28 | In Progress | Hoch |

---

### R-2026-002: Unbefugter Datenzugriff

**Beschreibung:**
Durch kompromittierte Zugangsdaten (Credential Theft) könnte ein Angreifer auf Kundendaten zugreifen. Dies würde GDPR-Meldepflichten und Reputationsschäden auslösen.

**Ursachen:**
- Fehlende Multi-Faktor-Authentifizierung
- Schwache Passwortrichtlinien
- Kein Privileged Access Management

**Maßnahmen:**

| Maßnahme | Verantwortlich | Deadline | Status | Wirksamkeit |
|----------|----------------|----------|--------|-------------|
| MFA für alle Benutzerkonten | IAM Team | 2026-02-15 | In Progress | Hoch |
| Passwortrichtlinie verschärfen | IAM Team | 2026-01-31 | Completed | Mittel |
| PAM-Lösung für privilegierte Accounts | IT Security | 2026-03-31 | Planned | Hoch |
| Regelmäßige Access Reviews | IAM Team | Quarterly | Ongoing | Mittel |

---

### R-2026-005: GDPR-Verstoß

**Beschreibung:**
Durch fehlerhafte Datenverarbeitungsprozesse könnten personenbezogene Daten unrechtmäßig verarbeitet werden, was zu Bußgeldern und Reputationsschäden führen kann.

**Ursachen:**
- Unvollständiges Verarbeitungsverzeichnis
- Fehlende Datenschutz-Folgenabschätzungen
- Unklare Datenflüsse bei Drittanbietern

**Maßnahmen:**

| Maßnahme | Verantwortlich | Deadline | Status | Wirksamkeit |
|----------|----------------|----------|--------|-------------|
| Verarbeitungsverzeichnis aktualisieren | DPO | 2026-02-28 | In Progress | Hoch |
| DSFA für kritische Verarbeitungen | DPO | 2026-03-15 | Planned | Hoch |
| Auftragsverarbeiter-Review | Legal/DPO | 2026-04-30 | Planned | Mittel |
| Datenschutz-Schulung für Mitarbeiter | HR/DPO | 2026-02-15 | In Progress | Mittel |

---

## Risk Summary Dashboard

### Risikoverteilung nach Stufe

| Risikostufe | Anzahl | Anteil |
|-------------|--------|--------|
| Critical | 1 | 14% |
| High | 2 | 29% |
| Medium | 3 | 43% |
| Low | 1 | 14% |
| **Gesamt** | **7** | 100% |

### Risikoverteilung nach Kategorie

| Kategorie | Anzahl | Kritischstes Risiko |
|-----------|--------|---------------------|
| Technisch | 1 | R-2026-001 (Critical) |
| Compliance | 2 | R-2026-002 (High) |
| Operativ | 1 | R-2026-003 (Medium) |
| Menschlich | 1 | R-2026-004 (Medium) |
| Extern | 1 | R-2026-006 (High) |
| AI Risk | 1 | R-2026-007 (Medium) |

### Treatment Status

| Status | Anzahl |
|--------|--------|
| Open | 4 |
| In Treatment | 3 |
| Closed | 0 |
| Accepted | 0 |

---

## Akzeptierte Risiken

| Risk ID | Beschreibung | Score | Akzeptiert durch | Datum | Nächste Review |
|---------|--------------|-------|------------------|-------|----------------|
| - | - | - | - | - | - |

---

## Geschlossene Risiken (Historie)

| Risk ID | Beschreibung | Urspr. Score | Schlussdatum | Grund |
|---------|--------------|--------------|--------------|-------|
| - | - | - | - | - |

---

## Änderungshistorie

| Datum | Version | Änderung | Autor |
|-------|---------|----------|-------|
| 2026-01-07 | 1.0 | Initiale Erstellung | Risk Manager |

---

## Genehmigung

| Rolle | Name | Datum | Unterschrift |
|-------|------|-------|--------------|
| Risk Manager | [Name] | [Datum] | _______________ |
| CISO | [Name] | [Datum] | _______________ |
| Management | [Name] | [Datum] | _______________ |
