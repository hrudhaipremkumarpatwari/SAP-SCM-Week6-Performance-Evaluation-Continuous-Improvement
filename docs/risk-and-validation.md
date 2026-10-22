# Risk Register and Validation Plan

The checks below are proposals for a controlled validation cycle. They are not results of a production SAP test run.

## 1. Principal risks and controls

| Risk | Potential impact | Proposed control / response | Owner |
|---|---|---|---|
| KPI definitions differ between teams | Inconsistent performance comparisons | Publish data dictionary, numerator/denominator, exclusions, units, calendar, owner, and version | Supply-chain process owner |
| Stale refresh or incomplete data | Dashboard appears current when events are missing | Show last-refresh timestamp and completeness status; alert on stale or partial loads | Reporting / integration support |
| Wrong material, location, or unit conversion | Misstated stock, demand, or output | Validate master data and conversion rules; use controlled exception queue | Master-data steward |
| Blocked/inspection stock counted as usable | Inventory coverage overstated | Separate unrestricted, blocked, and quality-inspection stock | Inventory / quality |
| Supplier dates not updated | Production plan uses obsolete supply assumptions | Confirm PO dates; escalate late/short deliveries; review supplier OTIF weekly | Procurement |
| Forecast error hidden by aggregate | High-volume SKUs mask local shortages | Review WAPE by product and location; segment stable and intermittent demand | Demand planner |
| Utilization too near capacity | Less recovery margin after breakdown or demand spike | Monitor load against available capacity; model downtime and changeover | Production planner |
| Cost reduction degrades service | Lower transport spend creates late or partial delivery | Balance cost per tonne with OTIF, fill rate and damage/expedite rates | Transport and finance |
| Scrap/expiry persists | Financial loss and waste | Review shelf-life, lot age, FEFO, forecast, batch size, quality holds | Quality / warehouse |
| Critical exceptions remain unowned | Slow response and recurring incidents | Severity, named owner, due time, age, escalation, and closure evidence | Control-tower lead |
| Duplicate or inconsistent source/target records | Bad KPI rollups and repeated transactions | Duplicate-safe keys, retry rules, reconciliation samples | Integration support |
| Improvement benefits overstated | Business case cannot be defended | Define baselines, counterfactual, benefit formula, data source, approval and tracking period | Finance / improvement lead |

## 2. Twelve proposed validation tests

| ID | Test | Expected evidence |
|---|---|---|
| VT-01 | Customer OTIF formula and edge cases | On-time complete, late complete, on-time partial, and changed promise cases handled consistently |
| VT-02 | Forecast accuracy / WAPE | Recomputed error and denominator agree with approved reporting logic |
| VT-03 | Volume fill rate | Demand and shipped tonnes reconcile; April 95.4% and September 98.0% match the simulated table |
| VT-04 | Inventory days of supply | Only usable stock included; blocked and inspection stock excluded |
| VT-05 | Cost per shipped tonne | Cost scope and shipped-tonne period/unit align; April ₹6,800/t and September ₹6,150/t reproduce |
| VT-06 | Capacity utilization | Resource calendar, changeovers, available hours, and downtime use one consistent basis |
| VT-07 | Supplier OTIF | Promised/confirmed dates, received quantity, and acceptance status are treated consistently |
| VT-08 | Master-data validation | Invalid material, site, or unit mapping generates a visible, assigned exception |
| VT-09 | Data freshness | Simulated stale refresh is flagged with timestamp and an owner/alert |
| VT-10 | Threshold alert | KPI breach or shortage creates correct severity, owner, and due time |
| VT-11 | Duplicate/retry behavior | Replaying an identical event does not produce duplicate business results |
| VT-12 | End-to-end reconciliation | Source, operational report, and dashboard sample quantities/statuses match or have traceable open issues |

## 3. Test execution record template

For a real test cycle, record: test ID, environment, SAP product/version, test date, preconditions, source document, test steps, expected result, actual result, evidence link, pass/fail, defect ID, owner, retest date, and closure approval. Do not describe the proposed tests as executed unless evidence exists.

## 4. Governance

- Daily exception review: focus on items that threaten shipment, production, quality or safety.
- Weekly operations review: discuss supplier OTIF, demand forecast, capacity, stock coverage and dispatch.
- Monthly scorecard: confirm data freshness, KPI definition, target variance and owner action.
- Quarterly governance review: approve changes to definitions, thresholds, source logic, and reporting access.

## 5. Limitations

All risks and tests are illustrative. Actual data lineage, reporting features, interfaces, refresh schedules, and roles must be confirmed for the SAP solution landscape and release in use. Dashboard figures in the report are simulated and must not be cited as actual operating results.
