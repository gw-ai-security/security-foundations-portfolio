# Praktische Übungen – Firewall Rule Audit

Diese Übungen helfen dir, die theoretischen Konzepte des Firewall-Audits praktisch anzuwenden. Jede Übung enthält Aufgabenstellung, Kontext und Musterlösung.

---

## Übung 1: Firewall-Regel analysieren

### Aufgabenstellung

Analysiere die folgende Firewall-Regel und bewerte sie hinsichtlich Risiko:

```
Rule-ID: FW-101
Source: ANY
Destination: 10.0.0.50 (Webserver)
Port: TCP/22 (SSH)
Action: ALLOW
Direction: Inbound
Comment: "SSH für Wartung"
```

**Aufgaben:**
1. Welches Risiko besteht bei dieser Regel?
2. Führe eine Risikobewertung durch (Impact × Likelihood)
3. Welche Empfehlung gibst du?

### Musterlösung

| Bewertungskriterium | Einschätzung |
|---------------------|--------------|
| **Risiko** | SSH-Zugang von "ANY" ermöglicht Brute-Force-Angriffe aus dem Internet |
| **Impact** | Hoch – Kompromittierung des Webservers möglich |
| **Likelihood** | Hoch – SSH-Brute-Force ist häufiger Angriffsvektor |
| **Risiko-Level** | **Hoch** |

**Empfehlung:**
- Quell-IP auf definierte Admin-Ranges einschränken (z.B. VPN-Subnetz)
- Alternativ: Bastion Host nutzen
- SSH-Key-Authentifizierung statt Passwort
- Fail2Ban oder Rate-Limiting implementieren
- Logging aktivieren

---

## Übung 2: Regelwerk bereinigen

### Aufgabenstellung

Folgendes Regelwerk enthält mehrere Probleme. Identifiziere und dokumentiere sie:

| Rule-ID | Source | Dest | Port | Action | Comment |
|---------|--------|------|------|--------|---------|
| FW-001 | ANY | ANY | ANY | ALLOW | "Temp für Test" |
| FW-002 | 10.0.1.0/24 | 10.0.2.10 | TCP/443 | ALLOW | "HTTPS zum Webserver" |
| FW-003 | 10.0.1.0/24 | 10.0.2.10 | TCP/443 | ALLOW | "" |
| FW-004 | ANY | 10.0.2.20 | TCP/3389 | ALLOW | "RDP für Admin" |
| FW-005 | 192.168.1.0/24 | ANY | ANY | ALLOW | "Alte Regel" |

### Musterlösung

| Rule-ID | Problem | Risiko | Empfehlung |
|---------|---------|--------|------------|
| FW-001 | ANY-ANY-ALLOW – vollständig offene Regel | **Kritisch** | Sofort entfernen oder stark einschränken |
| FW-002 | Korrekt konfiguriert | Niedrig | Behalten, Logging prüfen |
| FW-003 | Duplikat von FW-002, fehlender Kommentar | Niedrig | Entfernen (Duplikat) |
| FW-004 | RDP (3389) von ANY – hohes Angriffsrisiko | **Hoch** | Auf Admin-VPN einschränken |
| FW-005 | Breite Regel ohne klaren Zweck, "alte Regel" | Mittel | Prüfen und ggf. entfernen |

---

## Übung 3: Compliance-Mapping

### Aufgabenstellung

Ordne die folgenden Audit-Findings den entsprechenden ISO 27001:2022 Controls zu:

| Finding | ISO 27001:2022 Control |
|---------|------------------------|
| Firewall-Logs werden nicht zentral gespeichert | ? |
| Keine dokumentierte Änderungsprozedur für Regeln | ? |
| Admin-Zugang ohne MFA | ? |
| Netzwerke nicht segmentiert | ? |
| Regeln werden nie reviewed | ? |

### Musterlösung

| Finding | ISO 27001:2022 Control | Begründung |
|---------|------------------------|------------|
| Logs nicht zentral gespeichert | **A.8.15** (Logging) | Protokollierung von Ereignissen |
| Keine Änderungsprozedur | **A.8.9** (Configuration Management) | Kontrolle von Konfigurationsänderungen |
| Admin-Zugang ohne MFA | **A.5.17** (Authentication Information) | Sichere Authentifizierung |
| Netzwerke nicht segmentiert | **A.8.22** (Segregation in networks) | Netzwerksegmentierung |
| Regeln werden nie reviewed | **A.8.20** (Network Security) | Regelmäßige Überprüfung |

---

## Übung 4: Audit-Report erstellen

### Aufgabenstellung

Erstelle einen Mini-Audit-Report für folgendes Szenario:

**Kontext:** Du hast das Firewall-Regelwerk eines kleinen Unternehmens (50 Mitarbeiter) geprüft.
- Geprüfte Regeln: 25
- Gefundene Probleme: 3 kritisch, 5 mittel, 2 niedrig
- Wichtigstes Finding: SSH und RDP von ANY erlaubt

**Aufgabe:** Erstelle eine Executive Summary (max. 200 Wörter)

### Musterlösung

```markdown
## Executive Summary – Firewall Audit

**Datum:** [Datum]
**Scope:** 25 Firewall-Regeln, Perimeter-Firewall

### Gesamtbewertung
Das Firewall-Regelwerk weist **signifikante Sicherheitslücken** auf, die unmittelbares Handeln erfordern.

### Key Findings
- **3 kritische Findings:** Davon 2 offene Admin-Ports (SSH, RDP) aus dem Internet
- **5 mittlere Findings:** Fehlende Dokumentation, veraltete Regeln
- **2 niedrige Findings:** Optimierungspotenzial bei Logging

### Top-Risiken
1. SSH (Port 22) von ANY → Webserver: Brute-Force-Angriffe möglich
2. RDP (Port 3389) von ANY → Domain Controller: Kritischstes Finding

### Empfohlene Sofortmaßnahmen (72h)
1. SSH und RDP auf VPN-Subnetz einschränken
2. ANY-ANY-Regeln identifizieren und entfernen
3. Logging für alle kritischen Regeln aktivieren

### Compliance-Auswirkung
- ISO 27001 A.8.20 (Network Security): **Nicht erfüllt**
- NIST CSF PR.AC-5: **Teilweise erfüllt**

**Risiko-Level gesamt:** Hoch
**Empfehlung:** Maßnahmen innerhalb von 7 Tagen umsetzen
```

---

## Übung 5: Praxisprojekt – Eigenes Regelwerk

### Aufgabenstellung

Erstelle ein sicheres Firewall-Regelwerk für folgende Architektur:

**Szenario:**
- DMZ mit Webserver (10.0.1.10)
- Internes Netz mit Workstations (10.0.2.0/24)
- Datenbank-Server im internen Netz (10.0.2.50)
- Admin-Workstation (10.0.2.100)

**Anforderungen:**
1. Webserver soll HTTP/HTTPS aus dem Internet annehmen
2. Nur der Webserver darf mit der Datenbank kommunizieren (TCP/3306)
3. Admin-Workstation darf SSH zum Webserver
4. Interne Workstations dürfen ins Internet (HTTP/HTTPS)
5. Default Deny für alles andere

### Musterlösung

| Rule-ID | Source | Destination | Port | Action | Comment |
|---------|--------|-------------|------|--------|---------|
| FW-001 | ANY | 10.0.1.10 (Web) | TCP/80,443 | ALLOW | HTTP/HTTPS zum Webserver |
| FW-002 | 10.0.1.10 (Web) | 10.0.2.50 (DB) | TCP/3306 | ALLOW | Web → DB MySQL |
| FW-003 | 10.0.2.100 (Admin) | 10.0.1.10 (Web) | TCP/22 | ALLOW | Admin SSH zum Webserver |
| FW-004 | 10.0.2.0/24 | ANY | TCP/80,443 | ALLOW | Workstations → Internet |
| FW-005 | ANY | ANY | ANY | DROP | Default Deny (Cleanup Rule) |

**Best Practices beachtet:**
- ✅ Least Privilege Prinzip
- ✅ Explizite Regeln statt ANY
- ✅ Default Deny am Ende
- ✅ Dokumentierte Regeln

---

## Checkliste zur Selbstbewertung

Nach Abschluss aller Übungen solltest du folgende Fragen mit "Ja" beantworten können:

- [ ] Ich kann eine Firewall-Regel hinsichtlich Risiko bewerten
- [ ] Ich erkenne typische Schwachstellen in Regelwerken
- [ ] Ich kann ISO 27001 Controls auf Firewall-Findings mappen
- [ ] Ich kann einen Executive Summary für ein Audit schreiben
- [ ] Ich kann ein sicheres Regelwerk nach Best Practices erstellen

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| NIST SP 800-41 (Firewall Guidelines) | https://csrc.nist.gov/publications/detail/sp/800-41/rev-1/final |
| CIS Benchmark Firewall | https://www.cisecurity.org/cis-benchmarks |
| BSI IT-Grundschutz Netzwerk | https://www.bsi.bund.de/grundschutz |

---

> **Tipp:** Dokumentiere deine Lösungen in einem separaten Markdown-File als Nachweis für dein Portfolio!
