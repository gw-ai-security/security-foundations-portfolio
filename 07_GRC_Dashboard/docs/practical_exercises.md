# Praktische Übungen – GRC Dashboard

## Überblick

Diese Übungen vertiefen die Konzepte aus Projekt 7: GRC Dashboard. Sie sind praxisorientiert und bereiten auf echte GRC-Aufgaben sowie Interviews vor.

---

## Übung 1: Risk Register erstellen

### Lernziele
- Risiken systematisch identifizieren
- Inherent und Residual Risk berechnen
- Risk Treatment Optionen anwenden

### Aufgabe

Erstelle ein Risk Register für ein fiktives Unternehmen "TechStart GmbH" (200 Mitarbeiter, Cloud-basiert, B2B SaaS).

**Identifiziere mindestens 5 Risiken aus folgenden Kategorien:**
1. Technisch (z.B. Ransomware, System-Ausfall)
2. Compliance (z.B. GDPR-Verstoß)
3. Operativ (z.B. Key-Person-Dependency)
4. Extern (z.B. Supply Chain)
5. KI-bezogen (falls relevant)

### Template

| Risk ID | Beschreibung | Kategorie | Likelihood (1-5) | Impact (1-5) | Inherent Score | Treatment | Residual L | Residual I | Residual Score | Owner | Status |
|---------|--------------|-----------|------------------|--------------|----------------|-----------|------------|------------|----------------|-------|--------|
| R-001 | | | | | | | | | | | |

### Erwartetes Ergebnis

Ein vollständiges Risk Register mit:
- 5+ dokumentierten Risiken
- Begründung für L/I-Bewertungen
- Konkrete Treatment-Maßnahmen
- Realistische Residual Risk Werte

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

| Risk ID | Beschreibung | Kat. | L | I | Inherent | Treatment | Res. L | Res. I | Residual | Owner |
|---------|--------------|------|---|---|----------|-----------|--------|--------|----------|-------|
| R-001 | Ransomware via Phishing | Tech | 4 | 5 | 20 (Crit) | Mitigate | 2 | 4 | 8 (Med) | CISO |
| R-002 | GDPR-Verstoß durch Datenleck | Comp | 3 | 5 | 15 (High) | Mitigate | 2 | 4 | 8 (Med) | DPO |
| R-003 | CTO-Ausfall (Key Person) | Ops | 3 | 4 | 12 (High) | Mitigate | 2 | 3 | 6 (Med) | CEO |
| R-004 | Cloud-Provider Outage | Ext | 2 | 4 | 8 (Med) | Transfer | 2 | 3 | 6 (Med) | CTO |
| R-005 | AI-Bias in Scoring-System | AI | 3 | 3 | 9 (Med) | Mitigate | 2 | 2 | 4 (Low) | AI Lead |

**Maßnahmen R-001:**
- EDR auf allen Endpoints
- Phishing-Simulationen monatlich
- Immutable Backups
- E-Mail Security Gateway

</details>

---

## Übung 2: KPI Framework entwickeln

### Lernziele
- Security KPIs definieren
- Zielwerte festlegen
- Dashboard-Struktur verstehen

### Aufgabe

Entwickle ein KPI Framework für das Security-Team mit folgenden Bereichen:

1. **Vulnerability Management** (3 KPIs)
2. **Incident Response** (3 KPIs)
3. **Access Management** (3 KPIs)

Für jeden KPI definiere:
- Name und Beschreibung
- Berechnungsformel
- Zielwert
- Datenquelle
- Reporting-Frequenz

### Template

| Bereich | KPI Name | Formel | Zielwert | Datenquelle | Frequenz |
|---------|----------|--------|----------|-------------|----------|
| Vulnerability | | | | | |

### Erwartetes Ergebnis

9 vollständig definierte KPIs mit messbaren Zielwerten.

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

**Vulnerability Management:**
| KPI | Formel | Zielwert | Quelle | Frequenz |
|-----|--------|----------|--------|----------|
| Patch Compliance Rate | Gepatchte Systeme / Gesamt × 100 | > 95% | Vuln Scanner | Wöchentlich |
| Critical Vuln MTTR | Avg(Fix Date - Discovery Date) | < 72h | Ticketing | Monatlich |
| Scan Coverage | Gescannte Assets / Gesamt × 100 | > 98% | Asset CMDB | Monatlich |

**Incident Response:**
| KPI | Formel | Zielwert | Quelle | Frequenz |
|-----|--------|----------|--------|----------|
| Mean Time to Detect | Avg(Detection - Incident Start) | < 24h | SIEM | Monatlich |
| Mean Time to Contain | Avg(Containment - Detection) | < 4h | Ticketing | Monatlich |
| Incidents per 1000 Users | Incidents / Users × 1000 | < 5 | Ticketing | Monatlich |

**Access Management:**
| KPI | Formel | Zielwert | Quelle | Frequenz |
|-----|--------|----------|--------|----------|
| MFA Adoption Rate | MFA-enabled / Total Accounts × 100 | 100% | IAM | Monatlich |
| Orphaned Accounts | Accounts ohne Owner | < 5 | IAM + HR | Monatlich |
| Access Review Completion | Completed / Due × 100 | 100% | IAM | Quartalsweise |

</details>

---

## Übung 3: Business Impact Analysis

### Lernziele
- Kritische Prozesse identifizieren
- RTO/RPO bestimmen
- Abhängigkeiten analysieren

### Aufgabe

Führe eine Mini-BIA für die IT-Abteilung durch:

1. Identifiziere 4 kritische IT-Prozesse
2. Bewerte den Impact bei Ausfall (4h, 24h, 72h)
3. Definiere RTO und RPO
4. Identifiziere Abhängigkeiten

### Template

| Prozess | Impact 4h | Impact 24h | Impact 72h | RTO | RPO | Abhängigkeiten |
|---------|-----------|------------|------------|-----|-----|----------------|
| | | | | | | |

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

| Prozess | Impact 4h | Impact 24h | Impact 72h | RTO | RPO | Abhängigkeiten |
|---------|-----------|------------|------------|-----|-----|----------------|
| E-Mail-System | Mittel (Produktivität ↓) | Hoch (Kundenkommunikation ↓) | Kritisch (Vertragsrisiken) | 4h | 1h | AD, DNS, Storage |
| ERP-System | Hoch (Keine Aufträge) | Kritisch (Umsatzausfall) | Katastrophal (€50k+/Tag) | 2h | 15min | DB, Network, Auth |
| Active Directory | Kritisch (Kein Login) | Kritisch (Vollständiger Stillstand) | Katastrophal | 30min | 0 | DNS, DHCP |
| VPN-Gateway | Mittel (Remote Work ↓) | Hoch (50% Kapazität) | Hoch | 2h | - | Firewall, AD |

**Priorisierung:**
1. Active Directory (RTO: 30min)
2. ERP-System (RTO: 2h)
3. VPN-Gateway (RTO: 2h)
4. E-Mail-System (RTO: 4h)

</details>

---

## Übung 4: Compliance Mapping

### Lernziele
- Multi-Framework Compliance verstehen
- Controls zu Standards mappen
- Audit-Evidence identifizieren

### Aufgabe

Mappe folgende Sicherheitsmaßnahmen zu ISO 27001, GDPR und (falls anwendbar) EU AI Act:

1. Multi-Faktor-Authentifizierung
2. Datenverschlüsselung (at rest)
3. Security Awareness Training
4. Incident Response Plan
5. Data Retention Policy

### Template

| Maßnahme | ISO 27001 Control | GDPR Artikel | AI Act | Evidence |
|----------|-------------------|--------------|--------|----------|
| MFA | | | | |

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

| Maßnahme | ISO 27001 | GDPR | AI Act | Evidence |
|----------|-----------|------|--------|----------|
| MFA | A.5.17 (Authentication) | Art. 32(1) | Art. 14 (Human oversight) | IAM Config, Policy |
| Encryption at rest | A.8.24 (Cryptography) | Art. 32(1)(a) | Art. 15 (Robustness) | Encryption Policy, Key Management |
| Security Training | A.6.3, 7.2 (Competence) | Art. 39(1)(b) (DPO training) | Art. 14(4) (Competence) | Training Records, Attendance |
| IR Plan | A.5.24-27 (Incident Mgmt) | Art. 33, 34 | Art. 62 (Incident reporting) | IR Playbook, Test Records |
| Retention Policy | A.5.33 (Records) | Art. 5(1)(e), Art. 17 | Art. 10(5) | Retention Schedule, Deletion Logs |

</details>

---

## Übung 5: Executive GRC Report

### Lernziele
- Management-taugliche Kommunikation
- KPIs visualisieren
- Empfehlungen formulieren

### Aufgabe

Erstelle einen 1-seitigen Executive Summary für das Management mit:

1. **Overall Security Posture** (RAG-Status)
2. **Top 3 Risks** mit Trend
3. **Key Metrics** (max. 5)
4. **Top 3 Empfehlungen**

Nutze folgende fiktive Daten:
- 2 Critical Risks, 5 High Risks
- Patch Compliance: 78%
- MTTD: 36 Stunden
- MFA Coverage: 85%
- 1 offenes Critical Audit Finding

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

# Security Executive Summary – Januar 2026

## Overall Status: 🟡 ATTENTION REQUIRED

## Key Metrics

| Metrik | Status | Wert | Trend |
|--------|--------|------|-------|
| Risk Exposure | 🔴 | 2 Critical | ↑ |
| Patch Compliance | 🔴 | 78% | ↓ |
| Incident Detection | 🟡 | 36h | → |
| MFA Coverage | 🟡 | 85% | ↑ |
| Audit Findings | 🔴 | 1 Critical | → |

## Top 3 Risks

1. **Ransomware (Critical)** – Erhöhte Bedrohungslage, niedrige Patch-Rate
2. **Credential Theft (Critical)** – 15% User ohne MFA
3. **Audit Non-Compliance (High)** – Offenes Critical Finding

## Empfehlungen

| # | Empfehlung | Investment | ROI |
|---|------------|------------|-----|
| 1 | Emergency Patching Campaign | €15k | Risk ↓ 40% |
| 2 | MFA Rollout abschließen (30 Tage) | €5k | Risk ↓ 25% |
| 3 | Audit Finding remediieren | €10k | Compliance ✓ |

**Entscheidung erforderlich:** Budget-Freigabe für Empfehlungen 1-3

</details>

---

## Übung 6: BCDR Szenario

### Lernziele
- Recovery-Entscheidungen treffen
- Priorisierungen begründen
- Kommunikationsplan erstellen

### Aufgabe

**Szenario:** Ransomware hat das Hauptrechenzentrum verschlüsselt. 
- Alle Server betroffen
- Backups vom Vortag verfügbar
- DR-Site vorhanden (Cold Standby)

**Aufgaben:**
1. Welche 5 Systeme werden zuerst wiederhergestellt?
2. Erstelle einen Timeline (0-24h)
3. Wen informierst du wann?

### Musterlösung

<details>
<summary>Lösung anzeigen</summary>

**Recovery-Priorisierung:**
1. Network/Firewall (RTO: 30min) - Basis für alles
2. Active Directory/DNS (RTO: 30min) - Authentifizierung
3. Datenbank-Cluster (RTO: 1h) - Datenbasis
4. ERP-System (RTO: 2h) - Kerngeschäft
5. E-Mail (RTO: 4h) - Kommunikation

**Timeline:**
```
0:00  - Incident erkannt, CMT alarmiert
0:15  - DR-Entscheidung: Cold Site aktivieren
0:30  - Network-Team startet DR-Site
1:00  - Network up, AD-Restore beginnt
1:30  - AD/DNS funktionsfähig
2:00  - DB-Restore beginnt
3:00  - DB online, Integrity Check
4:00  - ERP-Restore beginnt
6:00  - ERP + E-Mail online
8:00  - User-Zugang aktiviert
24:00 - Normalbetrieb (eingeschränkt)
```

**Kommunikation:**
| Zeit | Empfänger | Nachricht |
|------|-----------|-----------|
| 0:15 | CMT, IT-Team | DR aktiviert |
| 0:30 | Management | Incident bestätigt |
| 1:00 | Alle Mitarbeiter | Systemausfall, Updates folgen |
| 2:00 | Key Customers | Service Impact Notification |
| 6:00 | Alle | Status: Systeme werden wiederhergestellt |
| 8:00 | Alle | Zugang wiederhergestellt |

</details>

---

## Selbstbewertung

Nach Abschluss aller Übungen, bewerte dich selbst:

| Kompetenz | Anfänger | Fortgeschritten | Experte |
|-----------|----------|-----------------|---------|
| Risk Register erstellen | ☐ | ☐ | ☐ |
| KPIs definieren | ☐ | ☐ | ☐ |
| BIA durchführen | ☐ | ☐ | ☐ |
| Compliance Mapping | ☐ | ☐ | ☐ |
| Executive Reporting | ☐ | ☐ | ☐ |
| BCDR-Entscheidungen | ☐ | ☐ | ☐ |

---

## Interview-Fragen zum Üben

1. "Erklären Sie den Unterschied zwischen Inherent und Residual Risk."
2. "Wie würden Sie RTO/RPO für ein kritisches System bestimmen?"
3. "Welche KPIs würden Sie einem CISO für monatliches Reporting empfehlen?"
4. "Wie mappen Sie ISO 27001 Controls auf GDPR-Anforderungen?"
5. "Beschreiben Sie Ihre ersten 24 Stunden nach einem Ransomware-Angriff."

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| ISACA GRC Resources | https://www.isaca.org/resources/grc |
| NIST SP 800-30 | https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final |
| ISO 22301 Overview | https://www.iso.org/iso-22301-business-continuity.html |
| FAIR Institute | https://www.fairinstitute.org/ |
