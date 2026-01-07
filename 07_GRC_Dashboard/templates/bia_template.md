# Business Impact Analysis (BIA) Template

## Dokumentinformationen

| Feld | Wert |
|------|------|
| **Organisation** | [Organisation Name] |
| **Version** | 1.0 |
| **Erstellt am** | [Datum] |
| **Erstellt von** | [Name] |
| **Genehmigt von** | [Name] |
| **Nächste Review** | [Datum + 12 Monate] |
| **Klassifikation** | Vertraulich |

---

## 1. Executive Summary

### Zweck
Diese Business Impact Analysis identifiziert kritische Geschäftsprozesse, bewertet die Auswirkungen von Ausfällen und definiert Recovery-Anforderungen als Grundlage für Business Continuity Planning.

### Scope
- **Organisationseinheiten:** [Liste]
- **Prozesse:** Kern- und unterstützende Geschäftsprozesse
- **Standorte:** [Liste]
- **Zeitrahmen der Analyse:** [Datum bis Datum]

### Kritische Findings

| Finding | Impact | Empfehlung |
|---------|--------|------------|
| [Prozess A] ohne DR-Lösung | Kritisch | DR-Site implementieren |
| [Prozess B] mit unklaren RTOs | Hoch | RTO/RPO definieren |
| [System C] Single Point of Failure | Hoch | Redundanz einführen |

---

## 2. Prozess-Inventar

### 2.1 Kernprozesse

| ID | Prozess | Abteilung | Owner | Kritikalität | RTO | RPO |
|----|---------|-----------|-------|--------------|-----|-----|
| BP-001 | [Prozess Name] | [Abt.] | [Name] | Kritisch | 1h | 0 |
| BP-002 | [Prozess Name] | [Abt.] | [Name] | Kritisch | 4h | 1h |
| BP-003 | [Prozess Name] | [Abt.] | [Name] | Hoch | 8h | 4h |
| BP-004 | [Prozess Name] | [Abt.] | [Name] | Mittel | 24h | 8h |
| BP-005 | [Prozess Name] | [Abt.] | [Name] | Gering | 72h | 24h |

### 2.2 Unterstützende Prozesse

| ID | Prozess | Abteilung | Owner | Kritikalität | RTO | RPO |
|----|---------|-----------|-------|--------------|-----|-----|
| SP-001 | IT-Infrastruktur | IT | [Name] | Kritisch | 1h | 0 |
| SP-002 | Helpdesk | IT | [Name] | Hoch | 4h | - |
| SP-003 | HR-Verwaltung | HR | [Name] | Mittel | 24h | 24h |
| SP-004 | Facility Management | Ops | [Name] | Mittel | 8h | - |

---

## 3. Impact-Analyse

### 3.1 Impact-Kategorien

#### Finanzieller Impact

| Prozess | 0-4h | 4-24h | 1-3 Tage | 3-7 Tage | > 7 Tage |
|---------|------|-------|----------|----------|----------|
| BP-001 | [€] | [€] | [€] | [€] | [€] |
| BP-002 | [€] | [€] | [€] | [€] | [€] |
| BP-003 | [€] | [€] | [€] | [€] | [€] |

#### Operativer Impact

| Prozess | 0-4h | 4-24h | 1-3 Tage | 3-7 Tage | > 7 Tage |
|---------|------|-------|----------|----------|----------|
| BP-001 | Gering | Mittel | Hoch | Kritisch | Katastrophal |
| BP-002 | Minimal | Gering | Mittel | Hoch | Kritisch |
| BP-003 | Minimal | Minimal | Gering | Mittel | Hoch |

#### Reputations-Impact

| Prozess | Beschreibung | Severity |
|---------|--------------|----------|
| BP-001 | Kundenbeschwerden, Social Media | Hoch |
| BP-002 | Negative Presse möglich | Mittel |
| BP-003 | Interne Unzufriedenheit | Gering |

#### Compliance/Rechtlicher Impact

| Prozess | Regulierung | Konsequenz | Severity |
|---------|-------------|------------|----------|
| BP-001 | GDPR Art. 32 | Bußgeld bis 4% Umsatz | Kritisch |
| BP-002 | Vertragsstrafen | [Betrag] | Hoch |
| BP-003 | Keine direkten | - | Gering |

---

## 4. RTO/RPO-Definition

### 4.1 Recovery Time Objective (RTO)

| Tier | RTO | Prozesse | Begründung |
|------|-----|----------|------------|
| **Tier 1** | < 1h | BP-001, SP-001 | Umsatzkritisch, keine Toleranz |
| **Tier 2** | < 4h | BP-002, SP-002 | SLA-Verpflichtungen |
| **Tier 3** | < 24h | BP-003, SP-003 | Wichtig, aber verzögerbar |
| **Tier 4** | < 72h | BP-004, BP-005 | Nicht zeitkritisch |

### 4.2 Recovery Point Objective (RPO)

| Tier | RPO | Systeme | Backup-Strategie |
|------|-----|---------|------------------|
| **Tier 1** | 0 (Real-time) | [Liste] | Synchrone Replikation |
| **Tier 2** | < 1h | [Liste] | Stündliche Snapshots |
| **Tier 3** | < 4h | [Liste] | 4-Stunden Incremental |
| **Tier 4** | < 24h | [Liste] | Tägliche Backups |

---

## 5. Ressourcen-Abhängigkeiten

### 5.1 IT-Systeme

| Prozess | Primäre Systeme | Sekundäre Systeme | Cloud-Dienste |
|---------|-----------------|-------------------|---------------|
| BP-001 | [ERP, CRM] | [Reporting] | [Cloud Service] |
| BP-002 | [System A] | [System B] | [Cloud Service] |
| BP-003 | [System C] | [System D] | - |

### 5.2 Personal

| Prozess | Min. Personal | Kritische Rollen | Remote-fähig |
|---------|---------------|------------------|--------------|
| BP-001 | [Anzahl] | [Rollen] | Ja / Nein |
| BP-002 | [Anzahl] | [Rollen] | Ja / Nein |
| BP-003 | [Anzahl] | [Rollen] | Ja / Nein |

### 5.3 Externe Abhängigkeiten

| Prozess | Lieferant/Partner | Service | Kritikalität |
|---------|-------------------|---------|--------------|
| BP-001 | [Name] | [Service] | Kritisch |
| BP-002 | [Name] | [Service] | Hoch |
| BP-003 | [Name] | [Service] | Mittel |

### 5.4 Standort-Anforderungen

| Prozess | Standort | Alternativer Standort | Remote-Option |
|---------|----------|----------------------|---------------|
| BP-001 | HQ | DR-Site | Teilweise |
| BP-002 | HQ | Remote | Ja |
| BP-003 | HQ | Remote | Ja |

---

## 6. Workaround-Verfahren

### Manuelle Alternativen

| Prozess | Normal | Workaround | Max. Dauer | Einschränkungen |
|---------|--------|------------|------------|-----------------|
| BP-001 | [System] | [Alternative] | 24h | [Beschreibung] |
| BP-002 | [System] | [Alternative] | 48h | [Beschreibung] |
| BP-003 | [System] | [Alternative] | 72h | [Beschreibung] |

---

## 7. Recovery-Priorisierung

### Priorisierte Recovery-Sequenz

```
Phase 1 (0-1h):    IT-Infrastruktur → Netzwerk → Authentication
Phase 2 (1-4h):    BP-001 → BP-002 → Kommunikation
Phase 3 (4-24h):   BP-003 → SP-002 → Reporting
Phase 4 (24-72h):  BP-004 → BP-005 → Archivierung
```

### Recovery-Matrix

| Priorität | Prozess | RTO | Abhängigkeiten | Recovery Team |
|-----------|---------|-----|----------------|---------------|
| P1 | SP-001 (IT Infra) | 30min | - | IT Ops |
| P2 | BP-001 | 1h | SP-001 | IT + Business |
| P3 | BP-002 | 4h | SP-001, BP-001 | IT + Business |
| P4 | SP-002 | 4h | SP-001 | IT |
| P5 | BP-003 | 8h | SP-001 | Business |

---

## 8. Gap-Analyse

### Aktuelle Capabilities vs. Anforderungen

| Prozess | RTO-Anforderung | Aktuelle Capability | Gap | Maßnahme |
|---------|-----------------|---------------------|-----|----------|
| BP-001 | 1h | 4h | -3h | DR-Site implementieren |
| BP-002 | 4h | 8h | -4h | Backup-Optimierung |
| BP-003 | 24h | 24h | 0 | - |
| SP-001 | 30min | 1h | -30min | HA-Cluster |

### Investitionsbedarf

| Maßnahme | Kosten (einmalig) | Kosten (jährlich) | Priorität |
|----------|-------------------|-------------------|-----------|
| DR-Site | [€] | [€] | Kritisch |
| HA-Cluster | [€] | [€] | Hoch |
| Backup-Optimierung | [€] | [€] | Mittel |

---

## 9. Empfehlungen

### Sofortmaßnahmen (0-30 Tage)

- [ ] [Maßnahme 1]
- [ ] [Maßnahme 2]
- [ ] [Maßnahme 3]

### Kurzfristige Maßnahmen (30-90 Tage)

- [ ] [Maßnahme 4]
- [ ] [Maßnahme 5]

### Mittelfristige Maßnahmen (90-180 Tage)

- [ ] [Maßnahme 6]
- [ ] [Maßnahme 7]

---

## 10. Genehmigung

| Rolle | Name | Datum | Unterschrift |
|-------|------|-------|--------------|
| BIA-Ersteller | [Name] | [Datum] | _______________ |
| Business Owner | [Name] | [Datum] | _______________ |
| IT-Leitung | [Name] | [Datum] | _______________ |
| Management | [Name] | [Datum] | _______________ |

---

## Anhänge

### A. Interviewte Stakeholder

| Name | Rolle | Datum | Themen |
|------|-------|-------|--------|
| [Name] | [Rolle] | [Datum] | [Themen] |

### B. Datenquellen

| Quelle | Beschreibung |
|--------|--------------|
| Asset-Inventar | IT-System-Liste |
| Organigramm | Abteilungsstruktur |
| SLAs | Service Level Agreements |

### C. Änderungshistorie

| Version | Datum | Autor | Änderungen |
|---------|-------|-------|------------|
| 1.0 | [Datum] | [Name] | Initiale Erstellung |
