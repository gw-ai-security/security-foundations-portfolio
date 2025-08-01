# IAM Audit Report – SecureBank AG (Beispiel)

## 1. Audit-Ziel

Ziel des IAM Audits ist die systematische Bewertung aller Rollen und Zugriffsrechte innerhalb der SecureBank AG.  
Der Fokus liegt auf der Einhaltung des Least-Privilege-Prinzips, der Vermeidung von Rollenüberschneidungen und der Einhaltung regulatorischer Anforderungen (ISO/IEC 27001 A.9, DSGVO Art. 5 & 32).

---

## 2. Audit-Zeitraum

- Durchführung: 01.–05. August 2025  
- Betrachtete Systeme: Active Directory, HR-System, Finanzsysteme (ERP)

---

## 3. Rollenüberblick

| Rolle             | Beschreibung                          | Systeme                    | Risiko     |
|------------------|---------------------------------------|----------------------------|------------|
| CEO              | Strategische Verantwortung             | Zugriff auf Management-Reports | Hoch     |
| IT_Admin         | Vollzugriff auf AD, Netzwerk, Server   | Active Directory, Backup-Systeme | Hoch     |
| HR_Admin         | Verwaltung von Personaldaten           | HR-System                   | Mittel     |
| Finance_Manager  | Steuerung Finanzprozesse, Reporting    | ERP-System, Buchhaltung     | Mittel     |
| HR_Assistant     | Lesender Zugriff auf HR-Daten          | HR-System                   | Niedrig    |
| Finance_Clerk    | Rechnungsprüfung, keine Freigaben      | Buchhaltungssystem          | Niedrig    |

---

## 4. Feststellungen & Bewertungen

### 4.1. IT_Admin
- **Befund**: Aktive Admin-Rechte auf 5 Systemen, kein dokumentiertes Logging
- **Risiko**: Hoch – keine Trennung kritischer Funktionen, fehlende Dokumentation
- **Maßnahme**: Aufteilung in IT_ReadOnly und IT_Admin; Einführung von Admin-Logging

### 4.2. HR_Admin
- **Befund**: Lesende und schreibende Zugriffe auf personenbezogene Daten
- **Risiko**: Mittel – keine Rezertifizierung in den letzten 12 Monaten
- **Maßnahme**: Quartalsmäßiger Review, Aufbewahrung als PDF im Audit-Archiv

### 4.3. Finance_Manager
- **Befund**: Zugriff auf Zahlungen und Controlling-Berichte
- **Risiko**: Mittel – mögliche Trennung von Zahlungserfassung und -freigabe notwendig
- **Maßnahme**: Einführung von SoD-Kontrollen im ERP-System

---

## 5. Verstöße gegen Best Practices

| Verstoß                          | Referenz                | Bewertung   |
|----------------------------------|--------------------------|-------------|
| Kein regelmäßiger Access Review | ISO 27001 A.9.2.5        | Kritisch    |
| Veraltete Rechtematrix          | ISO 27001 A.9.1.1        | Hoch        |
| Verwaiste Konten                | DSGVO Art. 32            | Mittel      |

---

## 6. Empfohlene Maßnahmen

- Rechtematrix aktualisieren und versionieren (monatlich)
- Einführung automatisierter Access Reviews (Sheets-Formular + PDF-Protokoll)
- Definition von Rollenverantwortlichen (Access Owner pro System)
- Trennung von Rollen mit „Toxic Combinations“
- Logging & Monitoring bei privilegierten Konten einführen

---

## 7. Compliance Mapping (Auszug)

| Norm / Artikel       | Maßnahme / Zuordnung                    |
|----------------------|-----------------------------------------|
| ISO 27001 A.9.2.5    | Regelmäßiger Review durch Access Owner  |
| ISO 27001 A.9.2.3    | Management privilegierter Rechte        |
| DSGVO Art. 5(1)(f)   | Schutz vor unbefugtem Zugriff           |
| DSGVO Art. 32        | Zugriffskontrolle als TOM               |

---

## 8. Fazit

Das IAM Audit bei der SecureBank AG hat gezeigt, dass zentrale Rollen klar definiert sind, jedoch Verbesserungsbedarf bei der Aktualität und Nachvollziehbarkeit von Berechtigungen besteht.  
Durch strukturierte Access Reviews, klar dokumentierte Rollen und technische Kontrollmechanismen lässt sich die Compliance signifikant verbessern.

**Nächste Schritte:**
- Umsetzung der Maßnahmen innerhalb von 30 Tagen
- Re-Audit durch internes ISMS-Team in Q4/2025
