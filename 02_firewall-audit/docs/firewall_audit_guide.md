# Firewall Audit Guide – Durchführung und Bewertung

Dieses Dokument beschreibt den Ablauf zur Durchführung eines Firewall Rule Audits anhand einer strukturierten Checkliste. Ziel ist es, sicherzustellen, dass Firewall-Regeln nachvollziehbar, risikobewertet und mit den Anforderungen an Netzwerkzugangskontrollen gemäß ISO/IEC 27001 und NIST CSF übereinstimmen.

---

## 1. Zielsetzung

- Identifikation potenziell riskanter oder unklarer Firewall-Regeln
- Kategorisierung von Regelrisiken (High / Medium / Low)
- Dokumentation für interne Audits oder externe Prüfungen
- Ableitung von Maßnahmen zur Härtung der Netzwerksicherheitskonfiguration

---

## 2. Eingesetzte Werkzeuge

| Tool                | Zweck                                 |
|---------------------|----------------------------------------|
| Google Sheets / Excel | Audit-Checkliste, Bewertung, Filterung |
| VS Code / Obsidian  | Dokumentation in Markdown               |
| draw.io (optional)  | Netzwerk- und Zonenvisualisierung       |
| PDF-Export          | Generierung des finalen Audit-Reports   |

---

## 3. Auditstruktur

Die Audit-Checkliste enthält folgende Spalten:

| Spalte                | Beschreibung                                                       |
|------------------------|---------------------------------------------------------------------|
| Rule ID               | Eindeutige Kennung der Regel (z. B. FW-001)                        |
| Beschreibung          | Zweck und Inhalt der Regel (z. B. „Allow HTTP from DMZ to Web“)    |
| Quell-/Ziel-IP        | Netzbereich oder Host, auf den sich die Regel bezieht             |
| Port/Protokoll        | z. B. TCP/80, UDP/53, ICMP                                         |
| Richtung              | Eingehend / Ausgehend / Intern                                     |
| Risiko (H/M/L)        | Einschätzung nach Risiko-Matrix (siehe unten)                     |
| Empfehlung            | Verbesserungsvorschlag (z. B. Einschränkung, Logging, Abschaltung) |
| Freigabe/Review       | Datum und Name der prüfenden Person                                |

---

## 4. Risikobewertung

Die Risikobewertung erfolgt anhand einer einfachen Matrix:

| Impact  | Likelihood | Ergebnis (Risk Level) |
|---------|------------|------------------------|
| Hoch    | Hoch       | Hoch                   |
| Hoch    | Mittel     | Hoch                   |
| Mittel  | Hoch       | Hoch                   |
| Mittel  | Mittel     | Mittel                 |
| Niedrig | Hoch       | Mittel                 |
| Hoch    | Niedrig    | Mittel                 |
| Mittel  | Niedrig    | Niedrig                |
| Niedrig | Mittel     | Niedrig                |
| Niedrig | Niedrig    | Niedrig                |

**Definitionen:**

- **Impact**: Potenzielle Auswirkung im Falle eines Missbrauchs  
- **Likelihood**: Wie wahrscheinlich ist es, dass die Regel ausgenutzt wird?

---

## 5. Typische Risikofaktoren

- **ANY**-Regeln ohne Einschränkungen
- Offen gelassene Admin-Ports (z. B. RDP, SSH)
- Regeln mit Public Source und Allow ALL
- Duplikate / überlappende Regeln ohne Dokumentation
- Fehlende Kommentierung oder Review-Datum

---

## 6. Vorgehen

1. **Regelwerk exportieren oder manuell übernehmen**
2. **Checkliste ausfüllen:** Jede Regel mit Risiko bewerten
3. **Empfehlungen eintragen:** z. B. Blockieren, Logging aktivieren, Zeitfenster
4. **Review durch zweite Person:** Eintrag mit Name + Datum
5. **Report erstellen:** PDF mit Übersicht + Maßnahmenliste

---

## 7. Mapping auf Standards

| Framework     | Referenzbereich                  |
|---------------|----------------------------------|
| ISO/IEC 27001 | A.13.1.1 – Network Controls      |
| NIST CSF      | PR.AC-5 – Netzwerkzugriffssteuerung<br>DE.CM-7 – Sicherheitsüberwachung |

---

## 8. Optional: Visualisierung

Nutze draw.io oder diagrams.net zur Darstellung der Netzwerkzonen:

- DMZ / Extern / Intern
- Firewall-Regeln als Pfeile
- Legende: erlaubte/abgelehnte Kommunikation

---

## 9. Ergebnis

Am Ende des Audits liegt eine dokumentierte, risikobewertete und begründete Liste aller Firewall-Regeln vor. Diese kann zur Verbesserung der Netzwerksicherheit sowie zur Vorbereitung auf externe Audits (ISO 27001, TISAX, BSI-Grundschutz) verwendet werden.

---

**Letzte Aktualisierung:** 2025-07-25  
**Autor:** gw-ai-security
