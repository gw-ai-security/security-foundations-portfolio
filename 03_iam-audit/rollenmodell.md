## IAM Rollenmodell – SecureBank AG (Mermaid-Diagramm)

```mermaid
graph TD
    %% Hauptrolle (Executive)
    CEO[CEO<br/>(delegiert Rollen)]

    %% Unterrollen
    IT_Admin[IT_Admin<br/>(Admin auf AD & Netzwerke)]
    HR_Admin[HR_Admin<br/>(Zugriff auf HR-Daten)]
    Finance_Manager[Finance_Manager<br/>(Verantwortung Finanzen)]

    %% Hierarchische Verbindungen
    CEO --> IT_Admin
    CEO --> HR_Admin
    CEO --> Finance_Manager

    %% Stildefinition
    classDef executive fill:#dae8fc,stroke:#000,color:#000;
    classDef it fill:#d5e8d4,stroke:#000,color:#000;
    classDef hr fill:#ffe6cc,stroke:#000,color:#000;
    classDef finance fill:#f8cecc,stroke:#000,color:#000;

    %% Stil-Zuweisung
    class CEO executive;
    class IT_Admin it;
    class HR_Admin hr;
    class Finance_Manager finance;
```
