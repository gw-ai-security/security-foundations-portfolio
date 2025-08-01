## IAM Rollenmodell – SecureBank AG (Mermaid)

```mermaid
graph TD
    %% Rollen
    CEO["CEO<br>delegiert Rollen"]
    IT_Admin["IT_Admin<br>Admin auf AD & Netzwerke"]
    HR_Admin["HR_Admin<br>Zugriff auf HR-Daten"]
    Finance_Manager["Finance_Manager\nVerantwortung Finanzen"]

    %% Beziehungen
    CEO --> IT_Admin
    CEO --> HR_Admin
    CEO --> Finance_Manager

    %% Farbklassen (werden ggf. von GitHub ignoriert, lokal oder in Live-Editor nutzbar)
    classDef executive fill=#dae8fc,stroke=#000,color=#000;
    classDef it fill=#d5e8d4,stroke=#000,color=#000;
    classDef hr fill=#ffe6cc,stroke=#000,color=#000;
    classDef finance fill=#f8cecc,stroke=#000,color=#000;

    class CEO executive;
    class IT_Admin it;
    class HR_Admin hr;
    class Finance_Manager finance;

```
