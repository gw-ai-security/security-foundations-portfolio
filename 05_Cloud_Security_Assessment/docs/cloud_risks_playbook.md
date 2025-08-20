# Cloud Risks Playbook – Projekt 5: Cloud Security Assessment Framework

Dieses Playbook beschreibt die häufigsten Risiken in Cloud-Umgebungen (AWS & Azure), ihre Ursachen, Auswirkungen und Gegenmaßnahmen.  
Es dient als praktisches Nachschlagewerk für Audits, Security Reviews und Incident Response.

---

## Struktur
Jedes Risiko wird nach folgendem Schema beschrieben:
- **Beschreibung** – Was ist das Risiko?  
- **Ursache** – Wie entsteht es?  
- **Auswirkung** – Welche Folgen ergeben sich für Vertraulichkeit, Integrität, Verfügbarkeit?  
- **Relevante Standards** – ISO 27017, NIST CSF, CIS Benchmarks, GDPR  
- **Gegenmaßnahmen** – Welche Kontrollen/Best Practices helfen?  

---

## Risiko 1: Öffentlich zugängliche Speicher (S3 Bucket / Azure Blob)
- **Beschreibung:** Cloud-Speichercontainer sind öffentlich lesbar oder beschreibbar.  
- **Ursache:** Fehlkonfiguration von Zugriffskontrollen, Nutzung von „Public Access“.  
- **Auswirkung:** Datenverlust, Datenschutzverletzungen (GDPR Art. 32), Reputationsschäden.  
- **Relevante Standards:**  
  - ISO 27017: 12.1.5, 18.1.4  
  - NIST CSF: PR.DS-1, PR.AC-3  
  - CIS AWS/Azure Benchmarks: Storage Controls  
- **Gegenmaßnahmen:**  
  - Standardmäßig „Block Public Access“ aktivieren  
  - Zugriffe via IAM-Rollen einschränken  
  - Logging & Monitoring aktivieren  

---

## Risiko 2: Überprivilegierte IAM-Rollen
- **Beschreibung:** Benutzer oder Systeme haben zu weitreichende Berechtigungen (z. B. Administratorrechte).  
- **Ursache:** Nutzung von „*:*“ Policies oder Sammelrollen.  
- **Auswirkung:** Erhöhtes Risiko für Missbrauch, Insider Threats und Angriffe.  
- **Relevante Standards:**  
  - ISO 27017: 9.2.3, 9.4.1  
  - NIST CSF: PR.AC-4, PR.AC-6  
  - CIS Benchmarks: IAM Policy Controls  
- **Gegenmaßnahmen:**  
  - Prinzip „Least Privilege“ anwenden  
  - Regelmäßige Access Reviews  
  - MFA aktivieren  

---

## Risiko 3: Offene Netzwerkports (0.0.0.0/0)
- **Beschreibung:** Dienste wie RDP, SSH oder Datenbanken sind weltweit ohne Einschränkungen erreichbar.  
- **Ursache:** Falsch konfigurierte Security Groups / NSGs.  
- **Auswirkung:** Direkte Angriffsfläche, Risiko von Brute-Force- und Exploit-Angriffen.  
- **Relevante Standards:**  
  - ISO 27017: 13.1.1  
  - NIST CSF: PR.AC-5, DE.CM-7  
  - CIS Benchmarks: Network Controls  
- **Gegenmaßnahmen:**  
  - Zugriff nur über VPN/Bastion Hosts  
  - IP-Whitelisting implementieren  
  - Intrusion Detection/Prevention Systeme einsetzen  

---

## Risiko 4: Fehlendes Logging & Monitoring
- **Beschreibung:** Aktivitäten in Cloud-Diensten werden nicht oder unzureichend protokolliert.  
- **Ursache:** CloudTrail (AWS) oder Azure Monitor ist deaktiviert oder unvollständig konfiguriert.  
- **Auswirkung:** Angriffe oder Datenabflüsse werden nicht erkannt; erschwerte Forensik.  
- **Relevante Standards:**  
  - ISO 27017: 12.4.1, 12.4.3  
  - NIST CSF: DE.CM-1, DE.CM-7  
  - CIS Benchmarks: Logging & Monitoring  
- **Gegenmaßnahmen:**  
  - Aktivierung von CloudTrail / Azure Monitor  
  - Zentrales Log-Management (SIEM) implementieren  
  - Alerts auf kritische Events konfigurieren  

---

## Risiko 5: Fehlende Verschlüsselung
- **Beschreibung:** Daten werden unverschlüsselt gespeichert oder übertragen.  
- **Ursache:** Default-Einstellungen nicht angepasst, fehlende TLS/SSL-Konfiguration.  
- **Auswirkung:** Datenschutzverletzungen, Abfangen sensibler Daten.  
- **Relevante Standards:**  
  - ISO 27017: 10.1, 10.2  
  - NIST CSF: PR.DS-2, PR.DS-5  
  - GDPR: Art. 32 (Sicherheit der Verarbeitung)  
- **Gegenmaßnahmen:**  
  - Standardmäßig serverseitige Verschlüsselung aktivieren  
  - TLS 1.2+ erzwingen  
  - Schlüsselmanagement via KMS/Azure Key Vault nutzen  

---

## Risiko 6: Shadow IT in der Cloud
- **Beschreibung:** Unkontrollierte Nutzung von Cloud-Diensten außerhalb des offiziellen IT-Bereichs.  
- **Ursache:** Eigenständige Kontoerstellung durch Fachbereiche.  
- **Auswirkung:** Keine zentrale Kontrolle, Compliance-Verstöße, Datenlecks.  
- **Relevante Standards:**  
  - ISO 27017: 6.2.1, 12.1.3  
  - NIST CSF: ID.AM-1, PR.AC-1  
- **Gegenmaßnahmen:**  
  - Cloud-Governance-Prozesse etablieren  
  - Zentrales Cloud Account Management  
  - Awareness-Programme für Mitarbeiter  

---

## Nutzung im Projekt
Dieses Playbook wird als Teil des Projekts genutzt, um:  
- Risiken zu identifizieren und zu bewerten  
- Controls auf ISO/NIST/CIS zu mappen  
- Empfehlungen für Audit- und Management-Reports abzuleiten  
