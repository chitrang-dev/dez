```mermaid
graph TD

subgraph Data Input
    OrgData[Org Data]
    DataSources[Boards / Articles / Market + Data Source]
    ClearAligned[Clear Aligned]
end

subgraph MDM
    Veeva[View / Veeva / Network MDM]
end

subgraph Vault
    Vault[Veeva Vault CRM]
    EDW[EDW]
end

subgraph Users
    Marketing[Marketing]
    Reporting[Reporting / Dashboards]
    SalesReps[Sales Reps]
    MSLs[MSLs]
end

Concur[Concur]

OrgData --> DataSources --> Veeva
ClearAligned --> Veeva
Veeva --> Concur
Veeva --> Vault
Vault --> EDW
EDW --> Reporting
EDW --> Marketing
Vault --> SalesReps
Vault --> MSLs
```
