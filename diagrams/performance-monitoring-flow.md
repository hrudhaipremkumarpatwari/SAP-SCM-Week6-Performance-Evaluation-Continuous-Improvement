# Performance Monitoring and Reporting Flow

~~~mermaid
flowchart TD
    A[Source events and records] --> B[Demand, purchasing, inventory, production, delivery, cost]
    B --> C[Validate units, period, keys, status and completeness]
    C --> D{Data quality passes?}
    D -- No --> E[Create data exception with owner and due time]
    E --> F[Correct source / mapping and reconcile]
    F --> C
    D -- Yes --> G[Calculate governed KPI definitions]
    G --> H[Refresh scorecard and trend views]
    H --> I[Compare actual vs target and prior period]
    I --> J{Critical gap or stale data?}
    J -- Yes --> K[Assign root-cause investigation and countermeasure]
    J -- No --> L[Continue standard monitoring]
    K --> M[Track action, owner and due date]
    M --> N[Review result in weekly/monthly cadence]
    L --> N
    N --> O[Validate outcome and improve KPI/control design]
~~~

## Control principles

- Validate data completeness and refresh time before interpreting a metric.
- Show formula, target, owner, period, trend, variance and next action.
- Keep customer OTIF distinct from volume fill rate.
- Treat proposed alerts as useful only when severity, recipient, due time and closure evidence are defined.
- Choose reporting functionality to match the deployed SAP products and version.
