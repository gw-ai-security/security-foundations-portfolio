# Compliance Mapping – ISO 27017, CIS Benchmarks, NIST CSF, GDPR

Dieses Dokument ordnet die im Cloud Security Assessment identifizierten Risiken den relevanten Normen, Frameworks und Benchmarks zu.  
Es dient als Audit-Nachweis und unterstützt die Ableitung von Maßnahmen.

---

## Struktur
- **Finding** – Beschreibung des Risikos  
- **ISO/IEC 27017 Control** – Cloud-spezifische Sicherheitsanforderungen  
- **CIS Benchmark** – AWS/Azure Best Practices  
- **NIST CSF** – Abbildung auf Funktionen/Kategorien  
- **GDPR** – Bezug zu europäischen Datenschutzanforderungen  

---

## Mapping-Tabelle

| Finding                          | ISO/IEC 27017             | CIS Benchmark (AWS/Azure)                 | NIST CSF            | GDPR |
|----------------------------------|---------------------------|-------------------------------------------|---------------------|------|
| Öffentliche S3 Buckets / Blob    | 12.1.5, 18.1.4             | AWS 2.1, Azure 3.1 (Storage Accounts)     | PR.DS-1, PR.AC-3    | Art. 32 |
| IAM-Benutzer ohne MFA            | 9.2.3, 9.4.1               | AWS 1.14, Azure 1.1 (MFA Policies)        | PR.AC-6, PR.AC-7    | Art. 32 |
| Offene Ports (0.0.0.0/0)         | 13.1.1                     | AWS 4.1, Azure 7.2 (NSG Rules)            | PR.AC-5, DE.CM-7    | Art. 32 |
| Fehlendes Logging (CloudTrail / Azure Monitor) | 12.4.1, 12.4.3        | AWS 2.5, Azure 2.1 (Activity Logs)        | DE.CM-1, DE.CM-7    | Art. 30, Art. 32 |
| Unverschlüsselte Datenbanken / Volumes | 10.1, 10.2             | AWS 2.2, Azure 3.4 (Encryption Enabled)   | PR.DS-2, PR.DS-5    | Art. 32 |
| Shadow IT in der Cloud           | 6.2.1, 12.1.3              | Allgemeine Governance Controls            | ID.AM-1, PR.AC-1    | Art. 5, Art. 28 |

---

## Erläuterungen

- **ISO/IEC 27017**  
  Cloud-spezifische Erweiterung der ISO 27001, relevant für Access Control, Datenverschlüsselung, Logging und Governance.  

- **CIS Benchmarks**  
  Detaillierte Härtungsleitfäden für AWS und Azure. Beispiele: MFA für IAM, Verschlüsselung für Storage, Logging aktivieren.  

- **NIST CSF**  
  - **PR.AC (Protect – Access Control)**: Kontrolle von Zugängen und Identitäten  
  - **PR.DS (Protect – Data Security)**: Schutz von Daten in Ruhe und in Bewegung  
  - **DE.CM (Detect – Continuous Monitoring)**: Kontinuierliche Überwachung  
  - **ID.AM (Identify – Asset Management)**: Inventarisierung und Governance  

- **GDPR**  
  - **Art. 28:** Anforderungen an Auftragsverarbeiter (Cloud Provider)  
  - **Art. 30:** Verzeichnis von Verarbeitungstätigkeiten (Logging)  
  - **Art. 32:** Sicherheit der Verarbeitung (z. B. Verschlüsselung, MFA, Zugriffskontrolle)  

---

## Fazit
Das Mapping zeigt, dass die identifizierten Risiken nicht nur technische Schwachstellen sind, sondern **direkt auf internationale Standards und rechtliche Anforderungen** einzahlen.  
Dieses Dokument kann als **Audit-Artefakt** verwendet werden, um Compliance-Readiness nachzuweisen.
