# CIA-Trias –Erklärung

Die CIA-Trias ist ein fundamentales Modell der Informationssicherheit. Sie beschreibt drei zentrale Schutzziele: Vertraulichkeit, Integrität und Verfügbarkeit. Diese Werte bilden die Grundlage jeder sicherheitsrelevanten Entscheidung in der IT.

---

## 1. Confidentiality (Vertraulichkeit)

- **Definition:**  
  Vertraulichkeit bedeutet, dass Informationen nur von berechtigten Personen eingesehen oder genutzt werden dürfen. Unbefugter Zugriff muss durch technische oder organisatorische Maßnahmen verhindert werden.

- **Beispiel aus dem Alltag:**  
  Ein verschlossener Briefkasten stellt sicher, dass nur der Empfänger den Brief lesen kann – nicht der Postbote oder Nachbar.

- **Beispiel aus der IT:**  
  Zugriff auf eine Kundendatenbank ist nur für Mitarbeitende mit entsprechender Rolle im CRM-System möglich. Andere Nutzer erhalten eine Fehlermeldung oder sehen gar keine Daten.

---

## 2. Integrity (Integrität)

- **Definition:**  
  Integrität bedeutet, dass Informationen vollständig und unverändert vorliegen. Daten dürfen nur durch autorisierte Prozesse geändert werden und müssen vor Manipulation geschützt sein.

- **Beispiel aus dem Alltag:**  
  Eine offizielle Urkunde darf nicht nachträglich verändert werden. Jede nachträgliche Änderung würde ihren rechtlichen Wert zerstören.

- **Beispiel aus der IT:**  
  Eine digitale Signatur stellt sicher, dass ein übermitteltes PDF-Dokument seit dem Versand nicht verändert wurde. Jede Änderung würde die Signatur ungültig machen.

---

## 3. Availability (Verfügbarkeit)

- **Definition:**  
  Verfügbarkeit bedeutet, dass Systeme und Informationen für autorisierte Nutzer zum benötigten Zeitpunkt zugänglich sind. Technische Ausfälle, Angriffe oder Überlastungen dürfen den Zugriff nicht verhindern.

- **Beispiel aus dem Alltag:**  
  Ein Bankautomat muss jederzeit funktionieren, wenn Kundinnen und Kunden Geld abheben wollen. Ein Ausfall führt zu Frustration und Einschränkungen.

- **Beispiel aus der IT:**  
  Ein Online-Shop setzt redundante Server ein, damit auch bei einem Hardware-Ausfall der Webshop weiterhin erreichbar bleibt. So wird die ständige Verfügbarkeit sichergestellt.

---
## 4. Zusammenhang der Werte

- **Wie hängen die drei Werte zusammen?**  
  Die drei Schutzziele der CIA-Trias – Vertraulichkeit, Integrität und Verfügbarkeit – ergänzen sich gegenseitig und bilden zusammen die Basis für Informationssicherheit. In vielen Systemen müssen sie gleichzeitig gewährleistet sein, um Daten zuverlässig, korrekt und geschützt bereitzustellen. Keiner der Werte steht isoliert – ihre Wechselwirkungen bestimmen die Qualität der Sicherheitsarchitektur.

- **Was passiert, wenn einer verletzt wird?**  
  Wird einer der Werte kompromittiert, ist die gesamte Informationssicherheit gefährdet.  
  - **Verlust der Vertraulichkeit** kann zu Datenschutzverletzungen, Wirtschaftsspionage oder Reputationsschäden führen.  
  - **Verlust der Integrität** kann zu fehlerhaften Entscheidungen führen, da Daten manipuliert oder verfälscht wurden.  
  - **Verlust der Verfügbarkeit** kann Prozesse lahmlegen, z. B. durch Ransomware oder DoS-Angriffe.

- **Typische Konflikte (z. B. Verfügbarkeit vs. Vertraulichkeit):**  
  Sicherheitsmaßnahmen zur Steigerung eines Werts können andere Werte beeinträchtigen. Ein klassisches Beispiel ist der Konflikt zwischen Verfügbarkeit und Vertraulichkeit:  
  - Ein stark abgesichertes System mit Mehrfaktor-Authentifizierung und Netzsegmentierung erhöht die Vertraulichkeit, kann aber die Verfügbarkeit für Benutzer senken – z. B. bei Notfällen oder Systemausfällen.  
  - Umgekehrt kann eine sehr offene Architektur (z. B. öffentliche APIs ohne Authentifizierung) zwar die Verfügbarkeit erhöhen, aber die Vertraulichkeit und Integrität gefährden.

  Daher ist ein ausgewogenes Sicherheitsdesign erforderlich, das alle drei Werte situationsgerecht priorisiert.
