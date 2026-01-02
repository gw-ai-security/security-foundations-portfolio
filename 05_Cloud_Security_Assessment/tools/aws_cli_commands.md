# AWS CLI Security Commands – Referenz

Diese Dokumentation enthält praktische AWS CLI-Befehle für Cloud Security Assessments. Alle Befehle sind getestet und können direkt verwendet werden.

---

## Voraussetzungen

```bash
# AWS CLI installieren
pip install awscli

# Konfiguration prüfen
aws configure list

# Aktuelle Identität prüfen
aws sts get-caller-identity
```

---

## 1. IAM Security Checks

### 1.1 Credential Report

```bash
# Credential Report generieren
aws iam generate-credential-report

# Credential Report abrufen (Base64-kodiert)
aws iam get-credential-report --query 'Content' --output text | base64 -d > credential_report.csv
```

### 1.2 Access Keys Analyse

```bash
# Alle User mit Access Keys auflisten
aws iam list-users --query 'Users[*].[UserName]' --output text | while read user; do
    echo "=== $user ==="
    aws iam list-access-keys --user-name "$user" --query 'AccessKeyMetadata[*].[AccessKeyId,Status,CreateDate]' --output table
done
```

### 1.3 MFA Status

```bash
# User ohne MFA auflisten
aws iam list-users --query 'Users[*].UserName' --output text | while read user; do
    mfa=$(aws iam list-mfa-devices --user-name "$user" --query 'MFADevices' --output text)
    if [ -z "$mfa" ]; then
        echo "KEIN MFA: $user"
    fi
done
```

### 1.4 Password Policy

```bash
# Password Policy abrufen
aws iam get-account-password-policy --output table
```

---

## 2. S3 Security Checks

### 2.1 Public Buckets finden

```bash
# Alle Buckets auflisten
aws s3api list-buckets --query 'Buckets[*].Name' --output text

# Public Access Block Status pro Bucket
aws s3api list-buckets --query 'Buckets[*].Name' --output text | while read bucket; do
    echo "=== $bucket ==="
    aws s3api get-public-access-block --bucket "$bucket" 2>/dev/null || echo "KEIN PUBLIC ACCESS BLOCK!"
done
```

### 2.2 Encryption Status

```bash
# Encryption pro Bucket prüfen
aws s3api list-buckets --query 'Buckets[*].Name' --output text | while read bucket; do
    echo "=== $bucket ==="
    aws s3api get-bucket-encryption --bucket "$bucket" 2>/dev/null || echo "KEINE ENCRYPTION!"
done
```

---

## 3. EC2 & Network Security

### 3.1 Security Groups Analyse

```bash
# Security Groups mit 0.0.0.0/0 (SSH)
aws ec2 describe-security-groups \
    --filters "Name=ip-permission.from-port,Values=22" "Name=ip-permission.cidr,Values=0.0.0.0/0" \
    --query 'SecurityGroups[*].[GroupId,GroupName]' --output table

# Security Groups mit 0.0.0.0/0 (RDP)
aws ec2 describe-security-groups \
    --filters "Name=ip-permission.from-port,Values=3389" "Name=ip-permission.cidr,Values=0.0.0.0/0" \
    --query 'SecurityGroups[*].[GroupId,GroupName]' --output table
```

### 3.2 VPC Flow Logs

```bash
# Flow Logs Status pro VPC
aws ec2 describe-vpcs --query 'Vpcs[*].VpcId' --output text | while read vpc; do
    echo "=== $vpc ==="
    aws ec2 describe-flow-logs --filter "Name=resource-id,Values=$vpc" --query 'FlowLogs[*].[FlowLogId,FlowLogStatus]' --output table
done
```

### 3.3 EBS Encryption

```bash
# Unverschlüsselte EBS Volumes finden
aws ec2 describe-volumes \
    --filters "Name=encrypted,Values=false" \
    --query 'Volumes[*].[VolumeId,Size,State]' --output table

# Default EBS Encryption aktivieren (pro Region)
aws ec2 enable-ebs-encryption-by-default
```

---

## 4. CloudTrail & Logging

### 4.1 CloudTrail Status

```bash
# CloudTrail Trails auflisten
aws cloudtrail describe-trails --query 'trailList[*].[Name,S3BucketName,IsMultiRegionTrail,LogFileValidationEnabled]' --output table
```

### 4.2 GuardDuty

```bash
# GuardDuty Detector Status
aws guardduty list-detectors

# GuardDuty aktivieren
aws guardduty create-detector --enable --finding-publishing-frequency FIFTEEN_MINUTES
```

---

## 5. RDS Security

```bash
# RDS Instances ohne Encryption
aws rds describe-db-instances \
    --query 'DBInstances[?StorageEncrypted==`false`].[DBInstanceIdentifier,Engine]' --output table

# RDS Instances öffentlich zugänglich
aws rds describe-db-instances \
    --query 'DBInstances[?PubliclyAccessible==`true`].[DBInstanceIdentifier,Engine]' --output table
```

---

## 6. Automatisierte Security Scans

### 6.1 Prowler (Open Source)

```bash
# Prowler installieren
pip install prowler

# Vollständigen Scan ausführen
prowler aws

# Nur CIS Benchmark
prowler aws --compliance cis_1.5_aws
```

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| AWS CLI Reference | https://docs.aws.amazon.com/cli/latest/reference/ |
| Prowler | https://github.com/prowler-cloud/prowler |
| ScoutSuite | https://github.com/nccgroup/ScoutSuite |

---

> **Hinweis:** Diese Befehle erfordern entsprechende IAM-Berechtigungen.
