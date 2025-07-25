# Mapping ISO/IEC 27001 & NIST CSF – Firewall Rule Audit

Diese Datei zeigt die Zuordnung relevanter Controls aus ISO/IEC 27001 und dem NIST Cybersecurity Framework (CSF) im Kontext der Bewertung von Firewall-Regelwerken (Projekt 2).

---

## Ziel des Mappings

Das Mapping dient der Nachvollziehbarkeit, wie die eingesetzten Checklisten, Dokumentationen und Reports regulatorische Anforderungen abdecken.

---

## Vergleichstabelle

| Thema                            | ISO/IEC 27001:2013 / 2022         | NIST CSF                          | Umsetzung im Projekt 2                      |
|----------------------------------|------------------------------------|------------------------------------|----------------------------------------------|
| Netzwerkzugang kontrollieren     | A.13.1.1 – Network Controls         | PR.AC-5 – Network Access Control   | Bewertung aller Regeln nach Herkunft/Ziel     |
| Regelmäßige Überprüfung           | A.18.2.2 – Compliance Evaluation    | ID.GV-3 – Policies in Place        | Review-Feld + periodische Auditstruktur       |
| Schutz vor unautorisierten Zugriffen | A.9.1 – Access Control Policies     | PR.AC-1 – Identities Authenticated | Empfohlene Maßnahmen z. B. Einschränkung ANY  |
| Detektion ungewöhnlicher Zugriffe | A.12.4.1 – Event Logging            | DE.CM-7 – Monitor Network Activity | Logging-Empfehlungen in der Checkliste       |
| Dokumentation & Nachweisführung  | A.7.5 – Documented Information      | RS.CO-1 – Coordination with Stakeholders | Audit Guide + PDF-Export + Mapping           |

---

## Quellen

- [ISO/IEC 27001:2022 Übersicht](https://www.iso.org/standard/27001)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- Referenzmodell basiert auf Projektstruktur aus `firewall_audit_guide.md` und `README.md`

---

## Hinweise

Dieses Mapping ist nicht normersetzend, sondern dient der internen Dokumentation und Prüfungsvorbereitung.  
Es kann für ISO-Audits, TISAX-Vorbereitung oder interne Kontrollsysteme (IKS) verwendet und erweitert werden.
