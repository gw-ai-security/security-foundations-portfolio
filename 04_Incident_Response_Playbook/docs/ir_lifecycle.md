# Incident Response Lifecycle (NIST SP 800-61r2)

Dieses Dokument beschreibt den vollständigen Lebenszyklus eines Incident-Response-Prozesses nach **NIST SP 800-61 Revision 2**.  
Der Lifecycle stellt sicher, dass Sicherheitsvorfälle strukturiert, nachvollziehbar und effizient behandelt werden.

---

## 1. Preparation (Vorbereitung)
- Aufbau von Incident-Response-Richtlinien und -Prozessen
- Definition von Rollen & Verantwortlichkeiten (CISO, SOC, IT-Admin, HR, Legal)
- Bereitstellung von Tools: SIEM, Ticketing, Forensik-Tools, Kommunikationskanäle
- Durchführung von Awareness-Schulungen & Tabletop-Übungen
- Sicherstellung rechtlicher Rahmenbedingungen (ISO 27001 A.16, DSGVO Art. 33)

**Ziel:** Organisation ist auf Sicherheitsvorfälle vorbereitet und handlungsfähig.

---

## 2. Detection & Analysis (Erkennung & Analyse)
- Monitoring von Logs, SIEM-Alarmen, IDS/IPS, Endpoint-Alerts
- Ersteinschätzung: False Positive oder echter Incident?
- Klassifizierung nach **Severity** (High / Medium / Low)
- Identifikation der betroffenen Systeme, Daten, Benutzer
- Dokumentation von Timeline, Indikatoren & Angriffspfad

**Ziel:** Schnelles Erkennen und präzises Einordnen eines Vorfalls.

---

## 3. Containment (Eindämmung)
- Kurzfristige Maßnahmen: Isolierung infizierter Systeme, Blockierung von IPs/Benutzern
- Mittelfristige Maßnahmen: Segmentierung von Netzwerken, Passwort-Rücksetzungen
- Abwägung: Business Continuity vs. Risikominimierung
- Dokumentation der getroffenen Schritte

**Ziel:** Schaden begrenzen, bevor weitere Systeme oder Daten kompromittiert werden.

---

## 4. Eradication (Beseitigung)
- Entfernung von Malware, Backdoors, kompromittierten Accounts
- Forensische Analyse der Root Cause (z. B. Schwachstelle im System)
- Implementierung von Fixes/Patches
- Validierung, dass Bedrohung vollständig entfernt wurde

**Ziel:** Ursachen nachhaltig beseitigen, keine erneute Kompromittierung.

---

## 5. Recovery (Wiederherstellung)
- Wiederherstellung betroffener Systeme aus Backups
- Überwachung der Systeme auf erneute Anomalien
- Schrittweise Rückkehr zum Normalbetrieb
- Kommunikation mit Stakeholdern und ggf. Behörden

**Ziel:** Sichere Rückkehr in den Regelbetrieb, ohne Restrisiken zu übersehen.

---

## 6. Lessons Learned (Nachbereitung)
- Durchführung einer **Post-Incident-Analyse**
- Bewertung der Effektivität von Prozessen & Eskalationswegen
- Anpassung von Playbooks, Policies und Trainings
- Erstellung eines Lessons-Learned-Reports für Management & Audit
- Ableitung von KPIs (Time-to-Detect, Time-to-Respond, Impact)

**Ziel:** Kontinuierliche Verbesserung der Security-Organisation und Vermeidung wiederkehrender Fehler.

---

## Übersicht: Incident Response Lifecycle
1. Preparation  
2. Detection & Analysis  
3. Containment  
4. Eradication  
5. Recovery  
6. Lessons Learned  

---

## Quellen & Standards
- NIST SP 800-61r2 – Computer Security Incident Handling Guide  
- ISO/IEC 27001:2017 – A.16 Information Security Incident Management  
- DSGVO Art. 33 – Meldepflicht bei Datenschutzverletzungen  
- SANS Institute – Incident Handler’s Handbook  

---
