# Praktische Übungen – Security Foundations

Diese Übungen helfen dir, die theoretischen Konzepte der IT-Security Foundations praktisch anzuwenden und zu vertiefen. Jede Übung enthält klare Aufgabenstellungen, erwartete Ergebnisse und Lernziele.

---

## Übung 1: CIA-Trias Analyse

### Lernziel
Verstehen, wie die drei Schutzziele (Confidentiality, Integrity, Availability) in realen Szenarien zusammenwirken.

### Aufgabenstellung

**Szenario:** Du bist Security-Berater für ein mittelständisches Unternehmen mit 200 Mitarbeitern. Das Unternehmen betreibt:
- Ein CRM-System mit Kundendaten
- Eine E-Commerce-Plattform
- Ein internes Wiki für Mitarbeiter

**Aufgabe:**
1. Erstelle für jedes System eine CIA-Bewertung (Hoch/Mittel/Niedrig)
2. Begründe deine Einschätzung
3. Identifiziere potenzielle Konflikte zwischen den Schutzzielen

### Erwartetes Ergebnis

| System | Confidentiality | Integrity | Availability | Begründung |
|--------|-----------------|-----------|--------------|------------|
| CRM | Hoch | Hoch | Mittel | Kundendaten sind sensibel (DSGVO), müssen korrekt sein |
| E-Commerce | Mittel | Hoch | Hoch | Transaktionen müssen korrekt sein, Shop muss verfügbar sein |
| Wiki | Niedrig | Mittel | Niedrig | Interne Infos, aber keine kritischen Daten |

### Reflexionsfragen
- Welches Schutzziel hat in deinem Unternehmen höchste Priorität?
- Wie würde sich die Bewertung ändern, wenn das Wiki auch externe Partner nutzen?

---

## Übung 2: STRIDE Threat Modeling

### Lernziel
Anwendung des STRIDE-Modells zur systematischen Bedrohungsanalyse.

### Aufgabenstellung

**Szenario:** Analysiere eine einfache Webanwendung mit folgenden Komponenten:
- Login-Seite mit Username/Passwort
- Benutzerprofil-Seite
- REST-API für mobile App
- Datenbank mit Benutzerdaten

**Aufgabe:**
Identifiziere für jede STRIDE-Kategorie mindestens eine konkrete Bedrohung:

| STRIDE-Kategorie | Bedrohung | Betroffene Komponente | Gegenmaßnahme |
|------------------|-----------|----------------------|---------------|
| **S**poofing | ? | ? | ? |
| **T**ampering | ? | ? | ? |
| **R**epudiation | ? | ? | ? |
| **I**nformation Disclosure | ? | ? | ? |
| **D**enial of Service | ? | ? | ? |
| **E**levation of Privilege | ? | ? | ? |

### Musterlösung

| STRIDE | Bedrohung | Komponente | Gegenmaßnahme |
|--------|-----------|------------|---------------|
| Spoofing | Angreifer gibt sich als legitimer User aus | Login-Seite | MFA, Account Lockout |
| Tampering | SQL Injection verändert Datenbankeinträge | REST-API | Input Validation, Prepared Statements |
| Repudiation | User bestreitet Transaktion | Profil-Seite | Audit Logging, digitale Signaturen |
| Info Disclosure | Passwörter im Klartext in Logs | API | Logging-Policy, Maskierung |
| DoS | Brute-Force Angriff auf Login | Login-Seite | Rate Limiting, CAPTCHA |
| Elevation | Normaler User greift auf Admin-Funktionen zu | API | RBAC, Session Management |

---

## Übung 3: DREAD Risikobewertung

### Lernziel
Quantitative Risikobewertung mit dem DREAD-Modell.

### Aufgabenstellung

Bewerte die folgenden Schwachstellen nach DREAD (Skala 1-10):

**Schwachstelle A:** SQL Injection in der Login-Funktion
**Schwachstelle B:** Fehlendes HTTPS auf der Profilseite
**Schwachstelle C:** Veraltete JavaScript-Bibliothek (jQuery 2.x)

### Bewertungsmatrix

| Kriterium | Schwachstelle A | Schwachstelle B | Schwachstelle C |
|-----------|-----------------|-----------------|-----------------|
| **D**amage Potential | ? | ? | ? |
| **R**eproducibility | ? | ? | ? |
| **E**xploitability | ? | ? | ? |
| **A**ffected Users | ? | ? | ? |
| **D**iscoverability | ? | ? | ? |
| **Gesamt (Durchschnitt)** | ? | ? | ? |

### Musterlösung

| Kriterium | SQL Injection | Fehlendes HTTPS | Veraltetes jQuery |
|-----------|---------------|-----------------|-------------------|
| Damage | 10 | 6 | 4 |
| Reproducibility | 9 | 10 | 3 |
| Exploitability | 7 | 8 | 2 |
| Affected Users | 10 | 8 | 5 |
| Discoverability | 6 | 9 | 7 |
| **Gesamt** | **8.4** | **8.2** | **4.2** |

**Priorisierung:** SQL Injection > HTTPS > jQuery

---

## Übung 4: Framework-Mapping

### Lernziel
Verstehen, wie verschiedene Security-Frameworks zusammenhängen.

### Aufgabenstellung

Ordne die folgenden Sicherheitsmaßnahmen den entsprechenden Framework-Controls zu:

| Maßnahme | ISO 27001 Control | NIST CSF Function | DSGVO Artikel |
|----------|-------------------|-------------------|---------------|
| Passwort-Policy implementieren | ? | ? | ? |
| Backup-System einrichten | ? | ? | ? |
| Security Awareness Training | ? | ? | ? |
| Incident Response Plan | ? | ? | ? |
| Datenverschlüsselung | ? | ? | ? |

### Musterlösung

| Maßnahme | ISO 27001 | NIST CSF | DSGVO |
|----------|-----------|----------|-------|
| Passwort-Policy | A.9.4.3 | PR.AC-1 | Art. 32 |
| Backup-System | A.12.3.1 | PR.IP-4 | Art. 32 |
| Security Awareness | A.7.2.2 | PR.AT-1 | Art. 39 |
| Incident Response | A.16.1 | RS.RP-1 | Art. 33 |
| Datenverschlüsselung | A.10.1.1 | PR.DS-1 | Art. 32 |

---

## Übung 5: Praxisprojekt – Mini Security Assessment

### Lernziel
Durchführung eines strukturierten Security Assessments.

### Aufgabenstellung

Führe ein Mini-Security-Assessment für eine selbst gewählte Anwendung durch (z.B. dein E-Mail-Provider, ein Open-Source-Projekt, eine Testumgebung).

**Schritte:**

1. **Asset-Identifikation**
   - Welche Daten werden verarbeitet?
   - Welche Systeme sind beteiligt?

2. **CIA-Bewertung**
   - Wie wichtig ist C, I, A für dieses System?

3. **Threat Modeling (STRIDE)**
   - Identifiziere 3-5 relevante Bedrohungen

4. **Risikobewertung (DREAD)**
   - Bewerte die Top-3-Bedrohungen

5. **Empfehlungen**
   - Formuliere 3 konkrete Verbesserungsvorschläge

### Dokumentationsvorlage

```markdown
# Mini Security Assessment Report

## 1. Executive Summary
[Kurze Zusammenfassung der wichtigsten Findings]

## 2. Scope
- System: [Name]
- Datum: [YYYY-MM-DD]
- Assessor: [Dein Name]

## 3. Asset-Inventar
| Asset | Typ | Kritikalität |
|-------|-----|--------------|
| ... | ... | ... |

## 4. CIA-Bewertung
| Schutzziel | Bewertung | Begründung |
|------------|-----------|------------|
| Confidentiality | ... | ... |
| Integrity | ... | ... |
| Availability | ... | ... |

## 5. Bedrohungsanalyse (STRIDE)
[Tabelle mit identifizierten Bedrohungen]

## 6. Risikobewertung (DREAD)
[Tabelle mit Risikoscores]

## 7. Empfehlungen
1. [Empfehlung 1]
2. [Empfehlung 2]
3. [Empfehlung 3]

## 8. Anhang
[Zusätzliche Informationen]
```

---

## Checkliste zur Selbstbewertung

Nach Abschluss aller Übungen solltest du folgende Fragen mit "Ja" beantworten können:

- [ ] Ich kann die CIA-Trias erklären und auf reale Systeme anwenden
- [ ] Ich verstehe alle sechs STRIDE-Kategorien und kann Beispiele nennen
- [ ] Ich kann eine DREAD-Bewertung durchführen und Risiken priorisieren
- [ ] Ich kenne die Grundzüge von ISO 27001, NIST CSF und DSGVO
- [ ] Ich kann ein einfaches Threat Model erstellen
- [ ] Ich kann Security-Maßnahmen auf Framework-Controls mappen

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| OWASP Threat Modeling | https://owasp.org/www-community/Threat_Modeling |
| Microsoft STRIDE | https://docs.microsoft.com/en-us/azure/security/develop/threat-modeling-tool |
| NIST Learning Resources | https://www.nist.gov/cyberframework/learning |
| BSI IT-Grundschutz | https://www.bsi.bund.de/grundschutz |

---

> **Tipp:** Dokumentiere deine Lösungen in einem separaten Markdown-File. So hast du einen Nachweis deiner praktischen Arbeit für dein Portfolio!
