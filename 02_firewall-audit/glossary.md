# Glossar – Firewall Audit (Projekt 2)

Dieses Glossar enthält die wichtigsten Begriffe rund um Firewall-Technologien, Netzwerksicherheit und Audit-Prozesse.

---

## A

### ACL (Access Control List)
Zugriffskontrollliste – eine geordnete Liste von Regeln, die festlegen, welcher Netzwerkverkehr erlaubt oder blockiert wird.

### Application Layer Firewall
Firewall, die auf OSI-Schicht 7 (Anwendungsschicht) arbeitet und Protokolle wie HTTP, FTP oder DNS analysieren kann.

### Audit Trail
Prüfpfad – chronologische Aufzeichnung aller Änderungen an Firewall-Regeln für Nachvollziehbarkeit und Compliance.

---

## B

### Bastion Host
Ein speziell gehärteter Server, der als einziger Zugangspunkt zwischen einem unsicheren und einem sicheren Netzwerk dient.

### Block Rule
Firewall-Regel, die Datenverkehr explizit ablehnt (DROP oder REJECT).

---

## C

### Chain
In iptables/nftables: Eine Sammlung von Regeln, die nacheinander abgearbeitet werden (z.B. INPUT, OUTPUT, FORWARD).

### Cleanup Rule
Abschlussregel am Ende eines Regelwerks, die allen nicht explizit erlaubten Verkehr blockiert ("Deny All" oder "Drop All").

### Connection Tracking (Stateful Inspection)
Verfolgung des Verbindungsstatus (NEW, ESTABLISHED, RELATED), um nur legitime Antwortpakete zuzulassen.

---

## D

### Default Deny
Sicherheitsprinzip: Alles, was nicht explizit erlaubt ist, wird blockiert. Best Practice für Firewall-Konfigurationen.

### DMZ (Demilitarized Zone)
Entmilitarisierte Zone – ein Netzwerksegment zwischen internem und externem Netzwerk für öffentlich zugängliche Dienste.

### DROP vs. REJECT
- **DROP**: Paket wird stillschweigend verworfen (keine Antwort)
- **REJECT**: Paket wird verworfen mit ICMP-Fehlermeldung an den Absender

---

## E

### Egress Filtering
Filterung des ausgehenden Netzwerkverkehrs – wichtig zur Verhinderung von Datenexfiltration und C2-Kommunikation.

### Explicit Deny
Eine Regel, die Verkehr ausdrücklich blockiert (im Gegensatz zu Implicit Deny durch Default-Regel).

---

## F

### Firewall Policy
Das Gesamtregelwerk einer Firewall, bestehend aus allen konfigurierten Regeln und deren Reihenfolge.

### Firewall Rule
Eine einzelne Anweisung, die festlegt, wie mit bestimmtem Netzwerkverkehr umgegangen werden soll.

### Five-Tuple
Die fünf Parameter zur Identifikation eines Netzwerkflusses:
1. Quell-IP
2. Ziel-IP
3. Quell-Port
4. Ziel-Port
5. Protokoll (TCP/UDP/ICMP)

---

## H

### High Availability (HA)
Hochverfügbarkeit – Firewall-Cluster mit automatischem Failover bei Ausfall eines Geräts.

### Host-based Firewall
Firewall, die auf einem einzelnen Host läuft und nur dessen Verkehr filtert (z.B. Windows Firewall, iptables).

---

## I

### Implicit Deny
Stillschweigende Ablehnung – alle Pakete, die keiner Regel entsprechen, werden automatisch blockiert.

### Ingress Filtering
Filterung des eingehenden Netzwerkverkehrs am Netzwerkperimeter.

### Interface
Netzwerkschnittstelle der Firewall (z.B. eth0, WAN, LAN, DMZ).

---

## L

### Least Privilege (Network)
Netzwerkzugriff nur auf die minimal notwendigen Dienste, Ports und Hosts beschränken.

### Log Rule
Regel, die Verkehr protokolliert, bevor sie ihn erlaubt oder blockiert – wichtig für Monitoring und Forensik.

---

## N

### NAT (Network Address Translation)
Adressübersetzung – Umschreibung von IP-Adressen beim Durchgang durch die Firewall.
- **SNAT**: Source NAT (ausgehend)
- **DNAT**: Destination NAT (eingehend, Port Forwarding)

### Network Segmentation
Aufteilung des Netzwerks in separate Segmente mit kontrollierten Übergängen (Firewalls).

### Next-Generation Firewall (NGFW)
Moderne Firewall mit erweiterter Funktionalität: Application Awareness, IPS, User Identity, SSL Inspection.

---

## O

### Object (Firewall Object)
Wiederverwendbare Definition für IPs, Netzwerke, Ports oder Dienste zur vereinfachten Regelerstellung.

### Orphan Rule
Verwaiste Regel – eine Regel, die keine Funktion mehr hat (z.B. Objekte gelöscht, Dienst abgeschaltet).

---

## P

### Packet Filtering
Grundlegende Firewall-Technik: Filterung basierend auf Header-Informationen (IP, Port, Protokoll).

### Permit Rule
Firewall-Regel, die Datenverkehr explizit erlaubt (ACCEPT/ALLOW).

### Policy Violation
Regelverstoß – eine Firewall-Regel, die gegen definierte Security-Policies verstößt.

### Port
Logische Adresse für Netzwerkdienste (0-65535). Well-known Ports: 0-1023.

---

## R

### Rule Base
Die Gesamtheit aller Firewall-Regeln in ihrer definierten Reihenfolge.

### Rule Order
Reihenfolge der Regeln – kritisch, da Firewalls meist "First Match" verwenden.

### Rule Ownership
Zuständigkeit für eine Regel – dokumentiert, wer die Regel beantragt hat und wer sie pflegt.

---

## S

### Shadow Rule
Schattenregel – eine Regel, die nie greift, weil eine vorherige Regel bereits den Verkehr abfängt.

### Stateful Firewall
Firewall, die den Verbindungsstatus verfolgt und nur legitime Antwortpakete durchlässt.

### Stateless Firewall
Firewall, die jedes Paket isoliert betrachtet, ohne Verbindungsstatus zu berücksichtigen.

---

## T

### Traffic Flow
Der Weg, den Netzwerkpakete durch die Firewall nehmen (z.B. WAN → DMZ → LAN).

### Transparent Firewall (Bridge Mode)
Firewall, die auf OSI-Schicht 2 arbeitet und keine IP-Adresse benötigt – unsichtbar für Endgeräte.

---

## U

### Unused Rule
Unbenutzte Regel – eine Regel, die in einem definierten Zeitraum keinen Traffic gematcht hat.

---

## V

### VLAN (Virtual LAN)
Virtuelles lokales Netzwerk – logische Segmentierung auf Schicht 2, oft in Kombination mit Firewall-Zonen.

### VPN Tunnel
Verschlüsselte Verbindung zwischen zwei Netzwerken oder einem Client und Netzwerk durch die Firewall.

---

## Z

### Zone
Logische Gruppierung von Netzwerkschnittstellen mit gleichem Sicherheitslevel (z.B. TRUST, UNTRUST, DMZ).

### Zone-based Firewall
Firewall-Architektur, bei der Regeln zwischen Zonen statt zwischen Interfaces definiert werden.

---

## Compliance-relevante Begriffe

| Begriff | Bedeutung | Relevanz |
|---------|-----------|----------|
| Change Management | Prozess zur kontrollierten Änderung von Firewall-Regeln | ISO 27001 A.12.1.2 |
| Rule Review | Regelmäßige Überprüfung des Regelwerks | ISO 27001 A.13.1.1 |
| Rule Documentation | Dokumentation von Zweck, Owner, Gültigkeit | Audit-Anforderung |
| Separation of Duties | Trennung von Beantragung, Genehmigung und Umsetzung | SOX, PCI-DSS |

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| NIST SP 800-41 (Firewall Guidelines) | https://csrc.nist.gov/publications/detail/sp/800-41/rev-1/final |
| CIS Benchmarks | https://www.cisecurity.org/cis-benchmarks |
| pfSense Documentation | https://docs.netgate.com/pfsense |
| iptables Tutorial | https://www.frozentux.net/iptables-tutorial |

---

> **Hinweis:** Dieses Glossar wird kontinuierlich erweitert und aktualisiert.
