# Praktische Übungen – Cloud Security Assessment

Diese Übungen helfen dir, die theoretischen Konzepte des Cloud Security Assessments praktisch anzuwenden.

---

## Übung 1: Shared Responsibility Model anwenden

### Aufgabenstellung

Ordne die folgenden Sicherheitsaspekte dem richtigen Verantwortlichen zu (Provider/Kunde/Geteilt):

| Sicherheitsaspekt | IaaS | PaaS | SaaS |
|-------------------|------|------|------|
| Physische Datacenter-Sicherheit | ? | ? | ? |
| Betriebssystem-Patches | ? | ? | ? |
| Netzwerk-Firewall-Regeln | ? | ? | ? |
| Benutzerverwaltung (IAM) | ? | ? | ? |
| Datenverschlüsselung | ? | ? | ? |
| Backup-Strategie | ? | ? | ? |

### Musterlösung

| Sicherheitsaspekt | IaaS | PaaS | SaaS |
|-------------------|------|------|------|
| Physische Datacenter-Sicherheit | Provider | Provider | Provider |
| Betriebssystem-Patches | **Kunde** | Provider | Provider |
| Netzwerk-Firewall-Regeln | **Kunde** | Geteilt | Provider |
| Benutzerverwaltung (IAM) | **Kunde** | **Kunde** | **Kunde** |
| Datenverschlüsselung | **Kunde** | Geteilt | Geteilt |
| Backup-Strategie | **Kunde** | **Kunde** | Geteilt |

**Key Learning:** Der Kunde ist IMMER für seine Daten und Identitäten verantwortlich!

---

## Übung 2: CIS Benchmark Findings bewerten

### Aufgabenstellung

Du erhältst folgende Findings aus einem Prowler-Scan. Bewerte jedes Finding:

| ID | Finding | Akzeptabel? | Risiko | Empfehlung |
|----|---------|-------------|--------|------------|
| 1 | Root Account ohne MFA | ? | ? | ? |
| 2 | S3 Bucket mit SSE-S3 Encryption | ? | ? | ? |
| 3 | Security Group: SSH von 0.0.0.0/0 | ? | ? | ? |
| 4 | CloudTrail aktiviert (alle Regionen) | ? | ? | ? |
| 5 | IAM User mit Passwort > 90 Tage | ? | ? | ? |

### Musterlösung

| ID | Finding | Akzeptabel? | Risiko | Empfehlung |
|----|---------|-------------|--------|------------|
| 1 | Root Account ohne MFA | ❌ Nein | **Kritisch** | MFA sofort aktivieren |
| 2 | S3 Bucket mit SSE-S3 Encryption | ✅ Ja | - | Best Practice erfüllt |
| 3 | Security Group: SSH von 0.0.0.0/0 | ❌ Nein | **Hoch** | Auf VPN-IP einschränken |
| 4 | CloudTrail aktiviert | ✅ Ja | - | Best Practice erfüllt |
| 5 | IAM User Passwort > 90 Tage | ❌ Nein | **Mittel** | Password Rotation Policy |

---

## Übung 3: Cloud-Risiko-Matrix erstellen

### Aufgabenstellung

Erstelle eine Risiko-Matrix für folgende Cloud-Findings:

**Findings:**
1. Öffentlich zugänglicher S3 Bucket mit Kundendaten
2. RDS Instance ohne Encryption at Rest
3. IAM User mit AdministratorAccess Policy
4. Fehlendes VPC Flow Logging
5. Lambda Function ohne Environment Encryption

Bewerte nach: Impact (Hoch/Mittel/Niedrig) × Likelihood (Hoch/Mittel/Niedrig)

### Musterlösung

| Finding | Impact | Likelihood | Risiko | Begründung |
|---------|--------|------------|--------|------------|
| S3 Public mit Kundendaten | **Hoch** | **Hoch** | **Kritisch** | Direkter DSGVO-Verstoß, öffentlich auffindbar |
| RDS ohne Encryption | **Hoch** | Mittel | **Hoch** | Compliance-Verstoß, aber intern |
| IAM AdministratorAccess | **Hoch** | Mittel | **Hoch** | Blast Radius bei Kompromittierung |
| Fehlendes VPC Flow Logging | Mittel | Niedrig | **Mittel** | Erschwert Forensik |
| Lambda ohne Env Encryption | Mittel | Niedrig | **Mittel** | Secrets könnten exposed sein |

**Priorisierung:** S3 > RDS/IAM > Logging > Lambda

---

## Übung 4: Compliance-Mapping

### Aufgabenstellung

Ordne die folgenden AWS-Maßnahmen den entsprechenden Standards zu:

| Maßnahme | ISO 27017 | CIS AWS | NIST CSF |
|----------|-----------|---------|----------|
| S3 Block Public Access | ? | ? | ? |
| CloudTrail Multi-Region | ? | ? | ? |
| MFA für Root Account | ? | ? | ? |
| VPC Flow Logs | ? | ? | ? |
| RDS Encryption | ? | ? | ? |

### Musterlösung

| Maßnahme | ISO 27017 | CIS AWS v1.5 | NIST CSF |
|----------|-----------|--------------|----------|
| S3 Block Public Access | 12.1.5, 18.1.4 | CIS 2.1.5 | PR.DS-1 |
| CloudTrail Multi-Region | 12.4.1 | CIS 3.1 | DE.CM-1 |
| MFA für Root Account | 9.2.3 | CIS 1.5 | PR.AC-7 |
| VPC Flow Logs | 12.4.3 | CIS 3.9 | DE.CM-7 |
| RDS Encryption | 10.1, 10.2 | CIS 2.3.1 | PR.DS-2 |

---

## Übung 5: Assessment Report schreiben

### Aufgabenstellung

Schreibe eine Executive Summary (max. 200 Wörter) für folgendes Assessment-Ergebnis:

**Kontext:** AWS Production Account einer E-Commerce-Firma
- Gescannte Ressourcen: 150 (EC2, S3, RDS, Lambda)
- Kritische Findings: 3
- Hohe Findings: 8
- Mittlere Findings: 15
- Wichtigstes Finding: S3 Bucket mit Kundendaten öffentlich

### Musterlösung

```markdown
## Executive Summary – Cloud Security Assessment

**Datum:** [Datum]
**Scope:** AWS Production Account (150 Ressourcen)

### Gesamtbewertung: KRITISCH

Das Assessment zeigt **erhebliche Sicherheitsrisiken** mit direkter DSGVO-Relevanz.

### Key Findings
- **3 kritische Findings**, davon 1 öffentlicher S3 Bucket mit Kundendaten
- **8 hohe Findings** (IAM Überprivilegierung, fehlende MFA)
- Compliance-Verstöße gegen ISO 27017 und CIS AWS Benchmark

### Top-Risiko: Datenexposition
Ein S3 Bucket mit Kundendaten ist öffentlich zugänglich. Dies stellt einen
unmittelbaren **DSGVO Art. 32 Verstoß** dar und erfordert sofortige Maßnahmen.

### Sofortmaßnahmen (24h)
1. S3 Public Access blockieren
2. Betroffene Kundendaten identifizieren
3. DSGVO-Meldepflicht prüfen (72h-Frist!)

### Kurzfristig (7 Tage)
1. MFA für alle IAM User aktivieren
2. IAM Policies nach Least Privilege überarbeiten

### Compliance-Status
- ISO 27017: **Nicht konform**
- CIS AWS v1.5: 65% erfüllt
- NIST CSF: Verbesserungsbedarf

**Risiko-Level:** Kritisch
**Empfehlung:** Sofortige Maßnahmenumsetzung erforderlich
```

---

## Übung 6: Hands-on Lab (Optional)

### Aufgabenstellung

Wenn du Zugang zu einem AWS Free Tier Account hast:

1. **Setup:** Erstelle einen S3 Bucket mit Default-Einstellungen
2. **Check:** Prüfe mit AWS CLI, ob Public Access blockiert ist
3. **Fix:** Aktiviere "Block all public access"
4. **Verify:** Prüfe erneut und dokumentiere

**Befehle:**

```bash
# Bucket erstellen
aws s3api create-bucket --bucket mein-test-bucket-12345 --region eu-central-1 --create-bucket-configuration LocationConstraint=eu-central-1

# Public Access Status prüfen
aws s3api get-public-access-block --bucket mein-test-bucket-12345

# Public Access blockieren
aws s3api put-public-access-block --bucket mein-test-bucket-12345 --public-access-block-configuration "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=true,RestrictPublicBuckets=true"

# Aufräumen
aws s3api delete-bucket --bucket mein-test-bucket-12345
```

---

## Checkliste zur Selbstbewertung

Nach Abschluss aller Übungen solltest du:

- [ ] Das Shared Responsibility Model für IaaS/PaaS/SaaS erklären können
- [ ] CIS Benchmark Findings bewerten und priorisieren können
- [ ] Eine Cloud-Risiko-Matrix erstellen können
- [ ] Findings auf ISO 27017, CIS und NIST CSF mappen können
- [ ] Einen Executive Summary für ein Cloud Assessment schreiben können
- [ ] Grundlegende AWS CLI Security-Befehle ausführen können

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| AWS Well-Architected Security | https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/ |
| Azure Security Benchmark | https://docs.microsoft.com/en-us/security/benchmark/azure/ |
| CIS Benchmarks | https://www.cisecurity.org/cis-benchmarks |
| Prowler | https://github.com/prowler-cloud/prowler |

---

> **Tipp:** Dokumentiere deine Lab-Ergebnisse als Screenshot-Portfolio!
