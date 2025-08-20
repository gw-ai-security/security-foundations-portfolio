# Glossary – Projekt 5: Cloud Security Assessment Framework

Dieses Glossar erklärt die zentralen Begriffe, Konzepte und Normen, die im Rahmen des Projekts verwendet werden.  
Es dient als Referenz für Audits, Reports und Interviews und ist direkt an **Cloud Security Standards** ausgerichtet.

---

## Cloud Security Grundlagen

**Shared Responsibility Model**  
Modell, das die Verantwortlichkeiten zwischen Cloud Service Provider (CSP) und Kunde aufteilt.  
- Provider: Sicherheit der Cloud (z. B. Infrastruktur, Hardware)  
- Kunde: Sicherheit in der Cloud (z. B. IAM, Daten, Konfigurationen)  

**IAM (Identity and Access Management)**  
Framework zur Verwaltung von Benutzeridentitäten und deren Berechtigungen in der Cloud.  
Zentrale Prinzipien: Least Privilege, Role-Based Access Control (RBAC), Multi-Factor Authentication (MFA).  

**Security Group / Network Security Group (NSG)**  
Virtuelle Firewall-Regeln, die in Cloud-Umgebungen (AWS/Azure) eingehenden und ausgehenden Traffic kontrollieren.  

**S3 Bucket (AWS) / Blob Storage (Azure)**  
Cloud-Speicherobjekte, die häufig falsch konfiguriert werden (z. B. öffentlich zugängliche Daten).  
Wichtige Maßnahmen: Verschlüsselung, Zugriffsbeschränkung, Logging.  

**Misconfiguration**  
Falsch oder unvollständig konfigurierte Systeme in Cloud-Umgebungen.  
Typische Beispiele: offene Ports, unverschlüsselte Daten, fehlende Monitoring-Mechanismen.  

---

## Frameworks & Standards

**ISO/IEC 27017**  
Internationale Norm für Cloud Security Controls. Ergänzt die allgemeine ISO 27001 um cloud-spezifische Sicherheitsmaßnahmen.  

**CIS Benchmarks**  
Best-Practice-Standards des Center for Internet Security (CIS).  
Definieren detaillierte Konfigurationsrichtlinien für AWS, Azure, Linux etc.  

**NIST Cybersecurity Framework (NIST CSF)**  
Rahmenwerk für Cybersicherheit mit 5 Kernfunktionen: Identify, Protect, Detect, Respond, Recover.  
Für Cloud Security besonders relevant:  
- PR.AC (Protect – Access Control)  
- PR.DS (Protect – Data Security)  
- DE.CM (Detect – Continuous Monitoring)  

**GDPR (Datenschutz-Grundverordnung)**  
Europäische Datenschutzrichtlinie. Im Cloud-Kontext relevant für:  
- Art. 28: Auftragsverarbeiter (CSP)  
- Art. 32: Sicherheit der Verarbeitung (z. B. Verschlüsselung, Zugriffskontrolle)  

---

## Risiko- und Audit-Begriffe

**Risk Assessment**  
Systematische Bewertung von Bedrohungen und Schwachstellen.  
Im Cloud-Kontext: Kombination aus Wahrscheinlichkeit (Likelihood) und Auswirkung (Impact).  

**Risk Matrix**  
Darstellung von Risiken nach Impact (hoch/mittel/niedrig) und Wahrscheinlichkeit. Grundlage für Management-Entscheidungen.  

**Least Privilege Principle**  
Sicherheitsprinzip, das vorsieht, dass Benutzer und Systeme nur die minimal notwendigen Rechte erhalten.  

**Separation of Duties (SoD)**  
Trennung kritischer Funktionen, um Missbrauch oder Fehler durch eine einzige Person zu verhindern. Beispiel: Ein Entwickler darf keinen Produktions-Deployment durchführen.  

**Compliance Mapping**  
Zuordnung von implementierten Kontrollen zu externen Normen und Standards (z. B. AWS Config Rule → ISO 27017 Control).  

---

## Tools & Methoden

**ScoutSuite**  
Open-Source-Tool für Multi-Cloud-Sicherheitsprüfungen. Nutzt API-Calls, um Konfigurationen zu analysieren.  

**Prowler**  
CLI-Tool für AWS Security Audits. Überprüft Konfigurationen gegen CIS Benchmarks.  

**draw.io / diagrams.net**  
Tool zur Visualisierung von Cloud-Architekturen, Netzwerkzonen und Sicherheitskontrollen.  

**Audit Trail**  
Nachvollziehbare Dokumentation aller durchgeführten Prüfungen und Ergebnisse. Wichtig für Revisionssicherheit.  

---

## Executive & Audit-Relevanz

**Management Summary**  
Verdichtete Darstellung von Risiken, Maßnahmen und Compliance-Erfüllung auf C-Level-Niveau.  

**Audit-Ready Documentation**  
Strukturierte, nachvollziehbare Dokumentation, die den Anforderungen von ISO, NIST und GDPR entspricht.  

**Cloud Compliance**  
Nachweis, dass Cloud-Dienste und deren Nutzung im Unternehmen mit geltenden Normen, Standards und gesetzlichen Anforderungen konform sind.  
