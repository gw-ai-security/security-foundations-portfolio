## IAM Rollenmodell – SecureBank AG 
---

```mermaid
graph TD
    %% Rollen-Definitionen
    CEO["CEO<br>delegiert Rollen"]
    IT_Admin["IT_Admin<br>Admin auf AD & Netzwerke"]
    HR_Admin["HR_Admin<br>Zugriff auf HR-Daten"]
    Finance_Manager["Finance_Manager<br>Verantwortung Finanzen"]

    %% Beziehungen / Hierarchie
    CEO --> IT_Admin
    CEO --> HR_Admin
    CEO --> Finance_Manager


```
