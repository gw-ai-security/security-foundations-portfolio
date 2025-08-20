# Eskalationsmatrix – Mermaid-Diagramm

Nachfolgend die Eskalations- und Kommunikationswege als Mermaid-Visualisierung.  
Die Darstellung entspricht dem draw.io-Diagramm: SOC Analyst → IT‑Admin → HR → Legal/Datenschutz, plus direkte Eskalation an CISO/Management.

```mermaid
flowchart LR
    %% Knoten
    SOC[SOC Analyst]
    ITA[IT-Admin]
    HR[HR]
    LEG[Legal / Datenschutz]
    CISO[CISO / Management]

    %% Hauptfluss
    SOC --> ITA --> HR --> LEG
    SOC --> CISO
    LEG --> CISO

    %% Stildefinitionen
    classDef soc fill:#dae8fc,stroke:#6c8ebf,color:#000,stroke-width:1px;
    classDef it fill:#ffe6cc,stroke:#d79b00,color:#000,stroke-width:1px;
    classDef hr fill:#d5e8d4,stroke:#82b366,color:#000,stroke-width:1px;
    classDef legal fill:#f8cecc,stroke:#b85450,color:#000,stroke-width:1px;
    classDef ciso fill:#e1d5e7,stroke:#9673a6,color:#000,stroke-width:1px;

    class SOC soc;
    class ITA it;
    class HR hr;
    class LEG legal;
    class CISO ciso;
```

## Hinweise zur Nutzung
- In GitHub wird das Mermaid-Diagramm direkt gerendert, wenn Mermaid aktiviert ist (Standard).
- Alternativ kann der Code in Tools wie Mermaid Live Editor eingefügt werden.
