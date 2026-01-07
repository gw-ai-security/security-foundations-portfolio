# GRC Architecture – Framework-Übersicht

## GRC Framework Architektur

```mermaid
flowchart TB
    subgraph External["External Environment"]
        REG[Regulators<br>ISO, GDPR, AI Act]
        STAKE[Stakeholders<br>Board, Investors]
        THREAT[Threat Landscape<br>Risks, Vulnerabilities]
    end
    
    subgraph GRC["GRC Framework"]
        subgraph GOV["GOVERNANCE"]
            POL[Policies &<br>Standards]
            ROLE[Roles &<br>Responsibilities]
            OVER[Oversight &<br>Accountability]
        end
        
        subgraph RISK["RISK MANAGEMENT"]
            RA[Risk<br>Assessment]
            RR[Risk<br>Register]
            RT[Risk<br>Treatment]
            RM[Risk<br>Monitoring]
        end
        
        subgraph COMP["COMPLIANCE"]
            CTRL[Controls<br>Framework]
            AUD[Audit &<br>Assessment]
            REP[Reporting &<br>Evidence]
        end
    end
    
    subgraph OPS["Operational Layer"]
        SEC[Security<br>Operations]
        IT[IT<br>Operations]
        BUS[Business<br>Operations]
        BC[Business<br>Continuity]
    end
    
    REG --> COMP
    STAKE --> GOV
    THREAT --> RISK
    
    GOV --> RISK
    GOV --> COMP
    RISK --> COMP
    
    COMP --> OPS
    RISK --> OPS
    GOV --> OPS
```

---

## GRC Integration Model

```
┌─────────────────────────────────────────────────────────────────────┐
│                         BOARD / EXECUTIVE                            │
│                    Strategic Direction & Oversight                   │
└───────────────────────────────┬─────────────────────────────────────┘
                                │
┌───────────────────────────────┴─────────────────────────────────────┐
│                          GRC COMMITTEE                               │
│              CISO • CFO • CLO • CRO • DPO • Audit                   │
└───────────────────────────────┬─────────────────────────────────────┘
                                │
        ┌───────────────────────┼───────────────────────┐
        │                       │                       │
        ▼                       ▼                       ▼
┌───────────────┐       ┌───────────────┐       ┌───────────────┐
│  GOVERNANCE   │       │     RISK      │       │  COMPLIANCE   │
│               │       │               │       │               │
│ • Policies    │◄─────►│ • Risk Mgmt   │◄─────►│ • ISO 27001   │
│ • Standards   │       │ • KRIs        │       │ • GDPR        │
│ • Procedures  │       │ • BIA         │       │ • AI Act      │
│ • Committees  │       │ • BCDR        │       │ • Audits      │
└───────┬───────┘       └───────┬───────┘       └───────┬───────┘
        │                       │                       │
        └───────────────────────┼───────────────────────┘
                                │
┌───────────────────────────────┴─────────────────────────────────────┐
│                         GRC PLATFORM                                 │
│        Risk Register • Control Library • Audit Management            │
│        Document Repository • KPI Dashboard • Reporting               │
└───────────────────────────────┬─────────────────────────────────────┘
                                │
┌───────────────────────────────┴─────────────────────────────────────┐
│                      OPERATIONAL SYSTEMS                             │
│   SIEM • Vuln Mgmt • IAM • CMDB • Ticketing • Training • DR         │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Three Lines Model

```mermaid
flowchart LR
    subgraph L1["1st Line: Operations"]
        OP1[Business Units]
        OP2[IT Operations]
        OP3[Security Ops]
    end
    
    subgraph L2["2nd Line: Oversight"]
        OV1[Risk Management]
        OV2[Compliance]
        OV3[Information Security]
    end
    
    subgraph L3["3rd Line: Assurance"]
        AS1[Internal Audit]
        AS2[External Audit]
    end
    
    GOV[Governing Body / Board]
    
    GOV --> L1
    GOV --> L2
    GOV --> L3
    
    L1 --> L2
    L2 --> L3
```

### Verantwortlichkeiten

| Line | Rolle | Verantwortung |
|------|-------|---------------|
| **1st Line** | Business/IT Operations | Risiken identifizieren & managen, Controls implementieren |
| **2nd Line** | Risk, Compliance, Security | Überwachung, Beratung, Standards setzen |
| **3rd Line** | Internal/External Audit | Unabhängige Prüfung, Assurance |

---

## Control Framework Integration

```mermaid
flowchart TD
    subgraph Standards["Standards & Regulations"]
        ISO[ISO 27001:2022]
        GDPR[GDPR]
        AI[EU AI Act]
        NIST[NIST CSF]
    end
    
    subgraph Controls["Unified Control Framework"]
        ACC[Access Control]
        CRY[Cryptography]
        OPS[Operations Security]
        INC[Incident Management]
        BC[Business Continuity]
        COM[Compliance]
    end
    
    subgraph Evidence["Evidence & Documentation"]
        POL2[Policies]
        PROC[Procedures]
        REC[Records]
        REP2[Reports]
    end
    
    ISO --> Controls
    GDPR --> Controls
    AI --> Controls
    NIST --> Controls
    
    Controls --> Evidence
```

---

## GRC Data Flow

```mermaid
sequenceDiagram
    participant BU as Business Unit
    participant RM as Risk Management
    participant COMP as Compliance
    participant AUD as Audit
    participant MGMT as Management
    
    BU->>RM: Risk Identification
    RM->>RM: Risk Assessment
    RM->>COMP: Control Requirements
    COMP->>BU: Control Implementation
    BU->>COMP: Control Evidence
    COMP->>AUD: Audit Readiness
    AUD->>AUD: Assessment
    AUD->>MGMT: Findings & Report
    MGMT->>RM: Risk Decisions
    RM->>BU: Treatment Actions
```

---

## GRC Maturity Model

```
Level 5 │ ████████████████████████████████████████ │ Optimized
        │ Continuous improvement, predictive       │
        │                                          │
Level 4 │ ██████████████████████████████          │ Managed
        │ Metrics-driven, quantitative             │
        │                    ▲                     │
Level 3 │ ████████████████████● Current Position  │ Defined
        │ Standardized, documented                 │
        │                                          │
Level 2 │ ████████████████                        │ Repeatable
        │ Basic processes, inconsistent            │
        │                                          │
Level 1 │ ████████                                │ Initial
        │ Ad-hoc, reactive                         │
        └──────────────────────────────────────────┘
```

### Maturity Assessment

| Domain | Current Level | Target | Gap |
|--------|---------------|--------|-----|
| Governance | 3 - Defined | 4 - Managed | +1 |
| Risk Management | 3 - Defined | 4 - Managed | +1 |
| Compliance | 4 - Managed | 4 - Managed | 0 |
| BC/DR | 2 - Repeatable | 3 - Defined | +1 |
| Reporting | 3 - Defined | 4 - Managed | +1 |

---

## KPI Dashboard Architektur

```
┌─────────────────────────────────────────────────────────────────────┐
│                       EXECUTIVE DASHBOARD                            │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐   │
│  │  Risk   │  │  Vuln   │  │Incident │  │Compliance│ │ Access  │   │
│  │  Score  │  │  Trend  │  │  Rate   │  │  Status │  │  KPIs   │   │
│  │   65    │  │   ↓     │  │   12    │  │   92%   │  │   91%   │   │
│  │   🟢    │  │   🟡    │  │   🟢    │  │   🟢    │  │   🟡    │   │
│  └─────────┘  └─────────┘  └─────────┘  └─────────┘  └─────────┘   │
└─────────────────────────────────────────────────────────────────────┘
                                │
        ┌───────────────────────┼───────────────────────┐
        │                       │                       │
        ▼                       ▼                       ▼
┌───────────────┐       ┌───────────────┐       ┌───────────────┐
│ Risk Register │       │   Control     │       │    Audit      │
│               │       │   Library     │       │  Findings     │
│ 7 active      │       │ 114 controls  │       │ 3 open        │
│ risks         │       │ mapped        │       │ findings      │
└───────────────┘       └───────────────┘       └───────────────┘
```

---

## Tool Integration

```mermaid
flowchart LR
    subgraph Sources["Data Sources"]
        SIEM[SIEM]
        VULN[Vulnerability<br>Scanner]
        IAM[IAM<br>System]
        TICK[Ticketing<br>System]
    end
    
    subgraph GRC["GRC Platform"]
        DASH[Dashboard]
        RISK[Risk<br>Module]
        CTRL[Control<br>Module]
        REP[Reporting]
    end
    
    subgraph Output["Outputs"]
        EXEC[Executive<br>Reports]
        AUD2[Audit<br>Evidence]
        KPI[KPI<br>Dashboard]
    end
    
    Sources --> GRC
    GRC --> Output
```

---

## Weiterführende Ressourcen

| Ressource | Link |
|-----------|------|
| ISACA COBIT | https://www.isaca.org/resources/cobit |
| IIA Three Lines Model | https://www.theiia.org/en/content/articles/global-knowledge-brief/2020/july/the-iias-three-lines-model/ |
| NIST CSF | https://www.nist.gov/cyberframework |
| ISO 27001 | https://www.iso.org/standard/27001 |
