# Incident Response Template

Dieses Template dient als standardisierte Handlungsanleitung für Incident Response Fälle.  
Es ist auf Basis von **NIST SP 800-61r2**, **ISO/IEC 27001 A.16** und **DSGVO Art. 33** entwickelt.

---

## 1. Basisinformationen
- **Incident-ID:** [IR-YYYY-NNN]  
- **Datum/Uhrzeit Entdeckung:** [TT.MM.JJJJ hh:mm]  
- **Gemeldet durch:** [Name, Abteilung]  
- **Erstkontakt SOC:** [Ja / Nein, Zeit]  

---

## 2. Incident-Klassifikation
- **Typ:** [Phishing, Ransomware, Insider Threat, Malware, etc.]  
- **Severity-Level:** [Critical / High / Medium / Low]  
- **Betroffene Systeme:** [Server, Endgeräte, Datenbanken, Cloud-Systeme]  
- **Betroffene Daten:** [personenbezogene Daten, kritische Geschäftsdaten]  

---

## 3. Detection & Analysis
- **Indikatoren:** [Alerts, Logs, User-Meldungen]  
- **Beschreibung der ersten Beobachtungen:**  
- **Klassifikation nach Severity Matrix:**  
- **Eskalationsweg:** [SOC → IT-Admin → CISO → Legal/DSB]  

---

## 4. Containment
- **Kurzfristige Maßnahmen:** [System-Isolation, Account-Sperrung, Blockierung]  
- **Mittelfristige Maßnahmen:** [Passwort-Reset, Segmentierung, Monitoring]  
- **Langfristige Maßnahmen:** [Awareness, Prozessanpassung]  
- **Datum/Uhrzeit:**  
- **Verantwortliche Person:**  

---

## 5. Eradication
- **Ursache identifiziert?** [Ja / Nein, Beschreibung]  
- **Entfernte Malware/Backdoors:**  
- **Technische Maßnahmen:** [Patching, Neuinstallation]  
- **Validierung abgeschlossen:** [Ja / Nein]  

---

## 6. Recovery
- **Wiederherstellung aus Backups:** [Ja / Nein, Details]  
- **Monitoring nach Wiederherstellung:**  
- **Systeme wieder im Produktivbetrieb:** [Ja / Nein, Datum/Uhrzeit]  
- **Business Impact behoben:** [Ja / Nein]  

---

## 7. Kommunikation & Reporting
- **Interne Eskalation:** [SOC, IT-Admin, CISO, HR, Legal/DSB]  
- **Externe Kommunikation:** [Behörden, Kunden, Partner]  
- **DSGVO-Meldung erforderlich:** [Ja / Nein]  
- **Falls Ja:** Datum/Uhrzeit der Meldung an Behörde:  
- **Interne Kommunikation:** [Awareness, Lessons Learned Meeting]  

---

## 8. Lessons Learned (Kurzfassung)
- **Positive Aspekte:** [z. B. schnelle Detection, klare Eskalation]  
- **Negative Aspekte:** [z. B. unklare Zuständigkeiten, Verzögerungen]  
- **Verbesserungsvorschläge:** [z. B. MFA einführen, Logging verstärken]  

---

## 9. Abschluss & Freigabe
- **Bearbeiter:** [Name, Abteilung, Datum]  
- **Review durch CISO:** [Name, Datum, Unterschrift]  
- **Review durch DSB:** [Name, Datum, Unterschrift]  
- **Status:** [Behoben / Monitoring / Offen]  

---
