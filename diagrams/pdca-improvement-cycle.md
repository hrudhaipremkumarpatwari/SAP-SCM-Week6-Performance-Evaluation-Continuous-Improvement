# Plan–Do–Check–Act Continuous-Improvement Cycle

~~~mermaid
flowchart TD
    A[PLAN: define KPI gap, baseline, target and hypothesis] --> B[DO: run a controlled intervention with owner and due date]
    B --> C[CHECK: compare same KPI logic and period; validate data quality]
    C --> D{Target and guardrails met?}
    D -- Yes --> E[ACT: standardize approved method and train users]
    D -- Mixed --> F[Adjust assumptions or intervention and repeat]
    D -- No / harmful side effect --> G[Rollback or redesign; record lesson]
    E --> H[Update standard, controls and KPI dashboard]
    F --> A
    G --> A
    H --> I[Select next prioritized improvement]
    I --> A
~~~

## Example — packaging shortages

- **Plan:** baseline is three shortage incidents/month at the end of the simulated period; proposed target is two or fewer. Validate BOM usage, supplier confirmations, lead time, stock status and unit conversion.
- **Do:** pilot a controlled daily shortage review and exception ageing alert for critical packaging materials.
- **Check:** count only incidents using the approved definition; compare matched periods and review service, inventory and expedite cost for adverse side effects.
- **Act:** standardize the workflow only if the measured result is better and quality/customer-service guardrails remain acceptable.

The example is a proposed improvement experiment, not evidence that an actual operational intervention has been run.
