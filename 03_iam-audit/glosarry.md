# Glossar – Identity & Access Management (IAM)

Dieses Glossar enthält zentrale Begriffe und Abkürzungen, die im Rahmen des IAM-Audit-Projekts verwendet werden. Ziel ist es, ein einheitliches Begriffsverständnis für Projektarbeit, Audit-Dokumentation und Interviews sicherzustellen.

---

## Grundbegriffe

| Begriff | Definition |
|--------|------------|
| **IAM (Identity & Access Management)** | Systematische Verwaltung von Benutzeridentitäten und deren Zugriffsrechten auf Systeme, Anwendungen und Daten. Ziel: Verfügbarkeit, Integrität und Vertraulichkeit. |
| **Identität** | Repräsentation eines Benutzers oder Systems innerhalb eines IT-Ökosystems, z. B. Benutzerkonto, Service Account. |
| **Zugriffsrecht** | Konkrete Berechtigung, eine bestimmte Ressource zu nutzen (z. B. „Lesen“, „Schreiben“, „Admin“). |
| **Rolle** | Bündelung mehrerer Zugriffsrechte für eine bestimmte Funktion oder Abteilung (z. B. „HR_Assistant“). |
| **Berechtigungsmatrix / Rechtematrix** | Tabelle zur Darstellung, welche Rollen/Personen welche Zugriffe auf Systeme haben. |
| **Access Review** | Regelmäßige Überprüfung aller bestehenden Zugriffsrechte im Unternehmen. Auditpflichtig. |
| **Rezertifizierung** | Bestätigung, dass bestehende Rechte weiterhin benötigt und gerechtfertigt sind. |
| **Least Privilege** | Prinzip, dass Benutzer nur die minimal erforderlichen Rechte erhalten dürfen. |
| **Need-to-Know** | Zugriff nur auf Informationen, die für die jeweilige Tätigkeit zwingend notwendig sind. |

---

## Technische & organisatorische Konzepte

| Begriff | Definition |
|--------|------------|
| **RBAC (Role-Based Access Control)** | Zugriffskontrollmodell, bei dem Rechte an Rollen gebunden sind, nicht direkt an Benutzer. |
| **SoD (Separation of Duties)** | Kritische Funktionen (z. B. Zahlung erfassen und freigeben) müssen getrennt vergeben werden. |
| **Privileged Account** | Konto mit erweiterten oder administrativen Rechten. Risikoquelle bei Missbrauch. |
| **Service Account** | Technisches Konto, das von Systemen oder Diensten verwendet wird (z. B. für Backup, Monitoring). |
| **Provisionierung** | Prozess der initialen Rechtevergabe an neue Benutzer. |
| **Deprovisionierung** | Entfernen aller Rechte nach Ausscheiden oder Rollenwechsel eines Benutzers. |
| **Onboarding/Offboarding** | IT-relevanter Prozess beim Eintritt bzw. Austritt von Mitarbeitenden. |
| **Audit Trail** | Nachvollziehbare Protokollierung von Zugriffen und Änderungen an Rechten. |

---

## Normen & Regulatorik

| Begriff / Abkürzung | Bedeutung |
|---------------------|-----------|
| **ISO/IEC 27001:2022** | Internationaler Standard für Informationssicherheitsmanagement (ISMS). Abschnitt A.9 behandelt Access Control. |
| **DSGVO (GDPR)** | EU-Datenschutzgrundverordnung. Art. 5(1)(f) und Art. 32 fordern Zugriffsschutz. |
| **A.9.x.y** | Konkrete Kontrollen aus Anhang A von ISO/IEC 27001 zu Benutzerverwaltung und Zugriffskontrolle. |
| **Art. 32 DSGVO** | Sicherheitsanforderungen an die Verarbeitung personenbezogener Daten, inkl. Zugriffskontrolle. |
| **Art. 5(1)(f) DSGVO** | Integrität und Vertraulichkeit als Grundprinzip der Datenverarbeitung. |

---

## Tools & Formate

| Begriff | Bedeutung |
|--------|-----------|
| **draw.io / diagrams.net** | Open-Source-Tool zur Erstellung von Architektur- und Rollenmodellen. |
| **Google Sheets / LibreOffice Calc** | Tabellenprogramme zur Erstellung der Rechtematrix. |
| **Markdown (.md)** | Leichtgewichtiges Format zur strukturierten Textdokumentation. |
| **PDF** | Format für revisionssichere Berichte und Audit-Dokumentation. |
| **VS Code / Obsidian** | Editor zur Bearbeitung von Markdown-Dateien im Security-Kontext. |

---

## Bewertung & Risiko

| Begriff | Bedeutung |
|--------|-----------|
| **Risikobewertung** | Einschätzung des Schadenspotenzials bei missbräuchlichem Zugriff. |
| **Risikokategorien** | Hoch / Mittel / Niedrig – je nach Vertraulichkeit, Integrität, Kritikalität. |
| **Kompensation** | Technische oder organisatorische Maßnahmen zur Risikominderung. |
| **Role Explosion** | Problem bei zu vielen Einzelrollen, was Management & Audits erschwert. |
| **Toxic Combination** | Kombination von Rechten, die gemeinsam ein hohes Risiko darstellen (z. B. Zahlung erfassen + freigeben). |

---

## Nützlich für Interviews & Audits

| Frage | Mögliche Antwort |
|-------|------------------|
| „Wie stellen Sie sicher, dass nur autorisierte Personen Zugriff auf sensible Daten haben?“ | Durch rollenbasierte Zugriffskontrolle (RBAC), regelmäßig dokumentierte Access Reviews und das Prinzip „Least Privilege“. |
| „Wie dokumentieren Sie kritische Adminrechte?“ | Über privilegierte Kontenlisten, Rechtematrix, Audit-Trail und jährliche Rezertifizierung. |
| „Wie erfolgt die Rücknahme von Rechten nach Austritt?“ | Automatisierte Deprovisionierung im Rahmen des Offboarding-Prozesses mit IT-Checkliste. |

---

## Empfehlung zur Nutzung

Diese Datei kann projektübergreifend verwendet werden (z. B. GRC Dashboard, Cloud Assessment, IR Playbook).  
Einbindung in jedes Projektverzeichnis als `glossary.md` ist empfohlen.

