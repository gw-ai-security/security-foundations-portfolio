# Security KPI Dashboard Template

## Dashboard-Übersicht

| Feld | Wert |
|------|------|
| **Organisation** | [Organisation Name] |
| **Berichtszeitraum** | [Monat/Quartal Jahr] |
| **Erstellt am** | [Datum] |
| **Erstellt von** | [Name] |
| **Version** | 1.0 |

---

## Executive Summary

### Gesamt-Status

```
┌─────────────────────────────────────────────────────────────────┐
│                    SECURITY HEALTH SCORE                         │
│                                                                   │
│                         ██████████ 82/100                        │
│                           🟢 Good                                │
│                                                                   │
│    Risk: 🟢     Vulnerabilities: 🟡     Compliance: 🟢          │
│    Incidents: 🟢     Access: 🟡         Training: 🟢            │
└─────────────────────────────────────────────────────────────────┘
```

### Key Highlights

| Kategorie | Status | Trend | Highlight |
|-----------|--------|-------|-----------|
| **Risk Management** | 🟢 | ↓ | Critical Risks reduziert auf 1 |
| **Vulnerability Management** | 🟡 | ↑ | Patch Rate verbessert auf 87% |
| **Incident Response** | 🟢 | ↓ | MTTD unter 24h erreicht |
| **Compliance** | 🟢 | → | ISO Audit bestanden |
| **Access Management** | 🟡 | ↑ | MFA Coverage bei 92% |

---

## 1. Risk Management KPIs

### Risk Overview

| Metrik | Ziel | Aktuell | Vormonat | Trend | Status |
|--------|------|---------|----------|-------|--------|
| Critical Risks | < 2 | 1 | 2 | ↓ | 🟢 |
| High Risks | < 5 | 3 | 4 | ↓ | 🟢 |
| Overdue Treatments | 0 | 2 | 3 | ↓ | 🟡 |
| Risk Exposure Index | < 50 | 45 | 52 | ↓ | 🟢 |

### Risk Distribution

```
Kritisch  ███                                               1 (5%)
Hoch      ██████                                            3 (15%)
Mittel    ████████████████                                  8 (40%)
Niedrig   ████████████████                                  8 (40%)
          ├─────────────────────────────────────────────────┤
          0                                                20
```

### Top 5 Risks

| Rang | Risk ID | Beschreibung | Score | Status |
|------|---------|--------------|-------|--------|
| 1 | R-001 | Ransomware-Angriff | 20 | In Treatment |
| 2 | R-002 | Credential Theft | 15 | In Treatment |
| 3 | R-006 | Supply Chain Compromise | 12 | Open |
| 4 | R-005 | GDPR-Verstoß | 12 | Open |
| 5 | R-003 | Datacenter-Ausfall | 10 | Open |

---

## 2. Vulnerability Management KPIs

### Vulnerability Overview

| Metrik | Ziel | Aktuell | Vormonat | Trend | Status |
|--------|------|---------|----------|-------|--------|
| Patch Compliance | > 95% | 87% | 82% | ↑ +5% | 🟡 |
| Critical Vulns Open | 0 | 3 | 5 | ↓ | 🟡 |
| MTTR (Critical) | < 72h | 96h | 120h | ↓ | 🔴 |
| Scan Coverage | > 98% | 95.6% | 94% | ↑ | 🟡 |

### Vulnerability Trend

```
Monat    Critical  High   Medium   Low    Total
─────────────────────────────────────────────────
Sep        8        25      80     45     158
Okt        6        22      75     42     145
Nov        5        20      68     40     133
Dez        4        18      64     41     127
Jan        3        18      64     42     127
                                   ↓ -20% YoY
```

### Age Analysis

| Alter | Critical | High | Medium | SLA |
|-------|----------|------|--------|-----|
| < 30 Tage | 2 | 12 | 40 | ✅ |
| 30-60 Tage | 1 | 4 | 18 | ⚠️ |
| 60-90 Tage | 0 | 2 | 6 | ⚠️ |
| > 90 Tage | 0 | 0 | 0 | ❌ |

---

## 3. Incident Response KPIs

### Incident Overview

| Metrik | Ziel | Aktuell | Vormonat | Trend | Status |
|--------|------|---------|----------|-------|--------|
| Total Incidents | - | 12 | 15 | ↓ -20% | 🟢 |
| Critical/High | < 2 | 1 | 2 | ↓ | 🟢 |
| MTTD | < 24h | 18h | 22h | ↓ | 🟢 |
| MTTC | < 4h | 3.5h | 4.2h | ↓ | 🟢 |
| MTTR | < 24h | 20h | 28h | ↓ | 🟢 |

### Incident Breakdown

| Kategorie | Anzahl | % | Severity |
|-----------|--------|---|----------|
| Phishing | 5 | 42% | M/L |
| Malware | 3 | 25% | H/M |
| Unauthorized Access | 2 | 17% | H |
| Data Leak | 1 | 8% | M |
| DDoS | 1 | 8% | L |

### Response Time Trend

```
MTTD (Stunden)
40h |
35h |  ●
30h |      ●
25h |          ●
20h |              ●
15h |                  ●
    └──────────────────────
       Sep  Okt  Nov  Dez  Jan
```

---

## 4. Compliance KPIs

### Compliance Overview

| Framework | Status | Score | Nächstes Audit |
|-----------|--------|-------|----------------|
| ISO 27001 | ✅ Zertifiziert | 92% | Q3 2026 |
| GDPR | ✅ Compliant | 88% | Ongoing |
| SOX (IT Controls) | ✅ Compliant | 95% | Q4 2026 |
| PCI-DSS | 🟡 In Progress | 75% | Q2 2026 |

### Audit Findings

| Priorität | Offen | In Arbeit | Geschlossen | Überfällig |
|-----------|-------|-----------|-------------|------------|
| Critical | 0 | 0 | 2 | 0 |
| High | 1 | 2 | 5 | 0 |
| Medium | 2 | 3 | 8 | 1 |
| Low | 1 | 2 | 12 | 0 |

### Policy Compliance

| Policy | Systeme | Compliant | Rate |
|--------|---------|-----------|------|
| Password Policy | 745 | 720 | 97% |
| Encryption | 200 | 185 | 93% |
| Logging | 165 | 160 | 97% |
| Access Control | 745 | 700 | 94% |

---

## 5. Access Management KPIs

### Access Overview

| Metrik | Ziel | Aktuell | Vormonat | Trend | Status |
|--------|------|---------|----------|-------|--------|
| MFA Adoption | 100% | 92% | 88% | ↑ +4% | 🟡 |
| Orphaned Accounts | < 5 | 2 | 5 | ↓ | 🟢 |
| Privileged Accounts | < 50 | 48 | 52 | ↓ | 🟢 |
| Access Reviews Done | 100% | 85% | 80% | ↑ | 🟡 |

### MFA Coverage

| Benutzergruppe | Total | MFA aktiv | Rate |
|----------------|-------|-----------|------|
| Privileged | 48 | 48 | 100% |
| Standard Users | 800 | 735 | 92% |
| Service Accounts | 100 | 80 | 80% |
| **Gesamt** | **948** | **863** | **91%** |

---

## 6. Security Awareness KPIs

### Training Overview

| Metrik | Ziel | Aktuell | Vormonat | Status |
|--------|------|---------|----------|--------|
| Training Completion | 100% | 92% | 88% | 🟡 |
| Phishing Test Pass Rate | > 90% | 85% | 78% | 🟡 |
| New Hire Training | 100% | 100% | 100% | 🟢 |

### Training by Department

| Abteilung | Mitarbeiter | Geschult | Rate |
|-----------|-------------|----------|------|
| IT | 80 | 80 | 100% |
| Finance | 120 | 115 | 96% |
| Sales | 200 | 175 | 88% |
| Operations | 400 | 360 | 90% |

---

## 7. Business Continuity KPIs

### BC Overview

| Metrik | Ziel | Aktuell | Status |
|--------|------|---------|--------|
| BC Plan Current | < 12 Monate | 8 Monate | 🟢 |
| DR Tests Passed | 100% | 100% | 🟢 |
| Backup Success Rate | > 99% | 99.5% | 🟢 |
| RTO Achievement | 100% | 95% | 🟡 |

### Last DR Test Results

| System | RTO Target | Actual | Status |
|--------|------------|--------|--------|
| AD/DNS | 30min | 25min | ✅ |
| Database | 1h | 55min | ✅ |
| E-Mail | 2h | 2h 15min | ⚠️ |
| ERP | 4h | 3h 45min | ✅ |

---

## 8. Action Items

### High Priority (This Month)

| ID | Action | Owner | Due Date | Status |
|----|--------|-------|----------|--------|
| A-001 | MTTR für Critical Vulns verbessern | Security Team | [Datum] | In Progress |
| A-002 | MFA für Sales-Abteilung | IAM Team | [Datum] | Planned |
| A-003 | PCI-DSS Gap Remediation | Compliance | [Datum] | In Progress |

### Medium Priority (This Quarter)

| ID | Action | Owner | Due Date | Status |
|----|--------|-------|----------|--------|
| A-004 | E-Mail DR-Zeit optimieren | IT Ops | [Datum] | Planned |
| A-005 | Phishing-Training intensivieren | HR | [Datum] | Planned |

---

## Anhang: KPI Definitionen

| KPI | Formel | Datenquelle |
|-----|--------|-------------|
| Patch Compliance | Gepatchte Systeme / Gesamt × 100 | Vulnerability Scanner |
| MTTD | Σ(Detection Time - Incident Start) / Incidents | SIEM, Ticketing |
| MFA Adoption | MFA-aktivierte Accounts / Gesamt × 100 | IAM System |
| Risk Exposure Index | Σ(Risk Score × Weight) / Max × 100 | Risk Register |

---

## Nächster Report: [Datum]
