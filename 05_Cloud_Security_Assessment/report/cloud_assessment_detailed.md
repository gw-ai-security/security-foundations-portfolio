# Cloud Security Assessment – Detailed Report

## Scope
Das Assessment umfasst AWS und Azure Free Tier Accounts. Bewertet wurden IAM, Storage, Netzwerk und Logging.

---

## Findings

### 1. AWS S3 Buckets
- **Beschreibung:** Mehrere S3 Buckets sind öffentlich zugänglich.
- **Risiko:** Hoch
- **Standard-Bezug:** ISO 27017 12.1.5, NIST CSF PR.DS-1
- **Empfehlung:** Public Access blockieren, Logging aktivieren.

### 2. Azure IAM (Identitäten & Zugriffe)
- **Beschreibung:** Mehrere Benutzer ohne MFA im Azure AD.
- **Risiko:** Hoch
- **Standard-Bezug:** ISO 27017 9.2.3, NIST CSF PR.AC-6, GDPR Art. 32
- **Empfehlung:** MFA erzwingen, Least Privilege Prinzip anwenden.

### 3. Netzwerksicherheit (AWS/Azure)
- **Beschreibung:** RDP (3389) offen für 0.0.0.0/0.
- **Risiko:** Hoch
- **Standard-Bezug:** ISO 27017 13.1.1, NIST CSF PR.AC-5
- **Empfehlung:** Nur Zugriff via VPN oder Bastion Host.

### 4. Monitoring
- **Beschreibung:** CloudTrail (AWS) und Azure Monitor sind nicht aktiviert.
- **Risiko:** Mittel
- **Standard-Bezug:** ISO 27017 12.4.1, NIST CSF DE.CM-1
- **Empfehlung:** Logging und Monitoring aktivieren, SIEM-Anbindung prüfen.

### 5. Verschlüsselung
- **Beschreibung:** Einige Datenbanken und Volumes sind unverschlüsselt.
- **Risiko:** Mittel
- **Standard-Bezug:** ISO 27017 10.1, NIST CSF PR.DS-2, GDPR Art. 32
- **Empfehlung:** Verschlüsselung by default aktivieren, Schlüsselverwaltung über KMS/Azure Key Vault.

---

## Risk Matrix
| Bereich         | Risiko  | Bewertung |
|-----------------|---------|-----------|
| S3 Buckets      | Public Access | Hoch |
| Azure IAM       | Benutzer ohne MFA | Hoch |
| Netzwerksicherheit | Offene Ports | Hoch |
| Monitoring      | Kein Logging | Mittel |
| Verschlüsselung | Nicht aktiviert | Mittel |

---

## Compliance Mapping
- **ISO 27017:** Cloud Security Controls (IAM, Storage, Monitoring)  
- **NIST CSF:** PR.AC, PR.DS, DE.CM  
- **CIS Benchmarks:** AWS Foundations, Azure Baseline  
- **GDPR:** Art. 32 Sicherheit der Verarbeitung  

---

## Empfehlungen (Priorisiert)
1. MFA für alle Benutzer erzwingen.  
2. Public Access in S3/Blob Storage blockieren.  
3. Security Groups restriktiver konfigurieren.  
4. Zentrales Logging aktivieren.  
5. Verschlüsselung für alle Datenbanken und Volumes aktivieren.  

---

## Fazit
Das Assessment zeigt zentrale Schwachstellen im Bereich IAM, Storage und Monitoring.  
Mit den vorgeschlagenen Maßnahmen können die Risiken signifikant reduziert und Compliance-Anforderungen erfüllt werden.
