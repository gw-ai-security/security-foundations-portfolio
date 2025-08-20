# Incident Severity & Impact Matrix

Dieses Dokument beschreibt die Klassifikation von Sicherheitsvorfällen anhand von **Impact (Auswirkung)** und **Likelihood (Eintrittswahrscheinlichkeit)**.  
Die Matrix dient als Grundlage für Eskalationsentscheidungen, Priorisierung und Reporting im Incident Response Prozess.

---

## Bewertungsdimensionen

### Impact (Auswirkung)
- **High (H):** Kritische Systeme betroffen, Datenverlust oder DSGVO-Meldepflicht, geschäftskritische Prozesse unterbrochen
- **Medium (M):** Eingeschränkte Funktionsfähigkeit, sensible aber nicht kritische Systeme betroffen, temporäre Unterbrechung möglich
- **Low (L):** Geringe Beeinträchtigung, keine sensiblen Daten, minimale Unterbrechung

### Likelihood (Eintrittswahrscheinlichkeit)
- **High (H):** Sehr wahrscheinlich, Vorfall tritt häufig auf oder ist aktiv im Netzwerk sichtbar
- **Medium (M):** Möglich, bekannte Schwachstelle oder auffälliges Verhalten vorhanden
- **Low (L):** Unwahrscheinlich, nur theoretisch möglich oder durch starke Kontrollen abgedeckt

---

## Severity Matrix (Impact × Likelihood)

|                | **High Impact (H)**              | **Medium Impact (M)**            | **Low Impact (L)**             |
|----------------|----------------------------------|----------------------------------|--------------------------------|
| **High Likelihood (H)** | **Critical** – Sofortige Eskalation an CISO & Management, Incident Response Team aktivieren | **High** – Innerhalb von Stunden behandeln, SOC überwacht kontinuierlich | **Medium** – Monitoring intensivieren, innerhalb von 1-2 Tagen lösen |
| **Medium Likelihood (M)** | **High** – Innerhalb eines Tages eskalieren, Incident Response Team involvieren | **Medium** – Innerhalb von 2-3 Tagen lösen, Management informieren | **Low** – Dokumentieren, Monitoring fortführen |
| **Low Likelihood (L)** | **Medium** – Bewertung vornehmen, ggf. Incident Response vorbereiten | **Low** – Kein unmittelbarer Handlungsbedarf, regelmäßiges Monitoring | **Low** – Beobachten, dokumentieren |

---

## Severity Levels – Definitionen

- **Critical:** Akuter Notfall. Geschäftsunterbrechung oder gesetzliche Meldepflicht. Sofortige Eskalation an CISO, DSB, Management und ggf. Behörden.  
- **High:** Schwere Sicherheitsverletzung mit potenziell hohem Schaden. Innerhalb von Stunden bis maximal 24h behandeln.  
- **Medium:** Moderater Vorfall. Eingeschränkte Systeme oder temporäre Störungen. Behandlung innerhalb weniger Tage.  
- **Low:** Geringfügiger Vorfall. Beobachten, dokumentieren, Monitoring verstärken. Keine sofortige Eskalation nötig.  

---

## Beispiele für Klassifikation

- **Critical (H/H):** Ransomware-Angriff mit Verschlüsselung produktiver Systeme, personenbezogene Daten betroffen (DSGVO-Meldepflicht).  
- **High (H/M oder M/H):** Phishing-Angriff erfolgreich, Mitarbeiteraccount kompromittiert, Zugriff auf interne Systeme.  
- **Medium (M/M oder H/L):** Malware auf isoliertem Endgerät, keine lateral movement Hinweise.  
- **Low (L/M oder L/L):** Verdächtige Logins von extern, aber durch MFA blockiert, keine Datenexfiltration.  

---

## Quellen & Standards
- NIST SP 800-61r2 – *Computer Security Incident Handling Guide*  
- ISO/IEC 27001:2017 – A.16 *Information Security Incident Management*  
- ENISA Threat Landscape Report  
- DSGVO Art. 33 – *Meldepflicht bei Datenschutzverletzungen*  

---
