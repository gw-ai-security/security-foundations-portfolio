## IAM Rollenmodell – SecureBank AG 
---

```mermaid
graph TD
    %% Rollen-Definitionen
    CEO["CEO\ndelegiert Rollen"]
    IT_Admin["IT_Admin\nAdmin auf AD & Netzwerke"]
    HR_Admin["HR_Admin\nZugriff auf HR-Daten"]
    Finance_Manager["Finance_Manager\nVerantwortung Finanzen"]

    %% Beziehungen / Hierarchie
    CEO --> IT_Admin
    CEO --> HR_Admin
    CEO --> Finance_Manager


```
