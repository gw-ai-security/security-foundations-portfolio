# Access Review Guide – SecureBank AG

## Ziel

Dieser Leitfaden beschreibt die Durchführung eines Access Reviews auf Rollen- und Berechtigungsebene in einer Organisation. Er dient zur Vorbereitung interner Audits, Rezertifizierungen und zur Sicherstellung von DSGVO- und ISO-27001-Konformität.

---

## 1. Definition: Was ist ein Access Review?

Ein **Access Review** ist eine periodische Überprüfung aller vergebenen Zugriffsrechte im Unternehmen. Ziel ist es, überflüssige oder risikoreiche Berechtigungen zu erkennen, dokumentieren und ggf. zu entziehen.

Typische Fragen:
- Wer hat Zugriff auf welche Systeme?
- Ist der Zugriff noch gerechtfertigt?
- Bestehen „Toxic Combinations“ oder SoD-Verletzungen?
- Ist die Dokumentation vollständig und nachvollziehbar?

---

## 2. Rechtliche & normative Grundlage

| Norm / Gesetz   | Abschnitt                          | Relevanz                    |
|----------------|------------------------------------|-----------------------------|
| ISO/IEC 27001   | A.9.2.5 – Review of User Access     | Pflicht zur regelmäßigen Überprüfung |
| DSGVO           | Art. 32 – Sicherheit der Verarbeitung | Zugriffsschutz für personenbezogene Daten |

---

## 3. Ablauf eines Access Reviews

### Schritt 1: Rollen und Systeme identifizieren
- Liste aller produktiven Systeme und Applikationen
- Zuordnung zu Verantwortlichen („System Owner“)
- Klar definierte Rollenbeschreibung

### Schritt 2: Datenextraktion
- Export aller aktiven Benutzerkonten inkl. Rollen/Zugriffsrechten
- Ideal: CSV oder Excel-Format, gruppiert nach System

### Schritt 3: Sichtung und Bewertung
- Durch Verantwortliche der Fachbereiche
- Fokus auf:
  - Berechtigungen, die nicht mehr benötigt werden
  - Zu hohe Rechte (z. B. Admin statt Lesen)
  - Dubletten, ungenutzte Konten, verwaiste Zugänge

### Schritt 4: Dokumentation der Ergebnisse
- Für jedes System: Tabelle mit Bewertung und Kommentar
- Klassifizierung: Behalten / Entziehen / Prüfen
- Ergänzung um Risikoeinstufung (hoch/mittel/niedrig)

### Schritt 5: Maßnahmenableitung
- Unnötige Rechte entziehen
- Rezertifizierung durch Vorgesetzte oder Systemverantwortliche
- Protokollierung der Änderungen

---

## 4. Rechtematrix als Hilfsmittel

Zur Durchführung und Dokumentation wird eine **Rechtematrix** verwendet:

| Benutzerrolle     | System A (Lesen) | System A (Admin) | HR-Daten | Risikoklasse |
|------------------|------------------|------------------|----------|--------------|
| HR_Assistant      | X                |                  | Ja       | Niedrig      |
| IT_Admin          | X                | X                | Nein     | Hoch         |

→ Diese Matrix sollte regelmäßig gepflegt, versioniert und durch einen **Access Owner** freigegeben werden.

---

## 5. Best Practices

- Reviews **quartalsweise oder halbjährlich** durchführen
- Ergebnisse versionieren und revisionssicher ablegen (z. B. als PDF)
- **Jede Änderung dokumentieren** (Audit-Trail, Freigabe)
- Verantwortlichkeiten klar regeln (z. B. HR prüft HR-Rechte)
- Technische und organisatorische Maßnahmen verknüpfen

---

## 6. Typische Schwachstellen

- Verwaiste Konten (z. B. ehemalige Mitarbeitende)
- Nicht dokumentierte Adminrechte
- Dubletten durch Systemmigrationen
- Unvollständige Rechtematrix
- Keine Eskalationsmatrix bei Auffälligkeiten

---

## 7. Beispielhafte Tools

| Zweck              | Tool-Empfehlung           |
|-------------------|---------------------------|
| Rechtematrix       | Google Sheets, LibreOffice Calc |
| Diagramm Rollenmodell | draw.io (diagrams.net)     |
| Dokumentation      | Markdown, VS Code, Obsidian  |
| Export für Audit   | PDF aus LibreOffice/Obsidian |

---

## 8. Fazit

Ein strukturierter Access Review ist ein zentraler Bestandteil jedes ISMS (Information Security Management System). Er verhindert unnötige Risiken, erhöht die Compliance und schützt personenbezogene Daten nach DSGVO.

**Ziel:**  
→ Nur berechtigte Personen haben Zugriff auf notwendige Daten – nicht mehr, nicht weniger.

