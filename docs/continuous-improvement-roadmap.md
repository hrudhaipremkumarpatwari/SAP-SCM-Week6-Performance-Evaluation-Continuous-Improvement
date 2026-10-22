# Continuous-Improvement Roadmap

This roadmap converts the report's simulated results into staged actions. Proposed dates are relative to the start of an implementation; the work should be reprioritized after confirming actual baselines and ownership.

## Priority gaps at the end of the simulated period

| Area | September simulation | Proposed target | Recommended focus |
|---|---:|---:|---|
| Customer OTIF | 93.0% | ≥95% | Review late/partial orders by root cause and delivery lane |
| Forecast accuracy | 88.5% | ≥90% | Measure WAPE by product/location; address bias and exceptional demand |
| Production schedule adherence | 91.0% | ≥92% | Protect frozen horizon and validate finite capacity / changeover assumptions |
| Supplier OTIF | 89.0% | ≥95% | Review confirmations, supplier reliability and critical components |
| Inventory cover | 27 days | 25–30 days | Preserve service while removing excess and stale inventory |
| Logistics cost per tonne | ₹6,150 | ≤₹6,460 | Sustain saving while verifying OTIF and fill rate |
| Critical-exception resolution | 6 hours | ≤4 hours | Set severity, owner, response target, ageing alert and closure evidence |
| Packaging shortages | 3/month | ≤2/month | Review reorder parameters, supplier commitments, and shortage causes |
| Packaging utilization | 92% | 85–92% band | Maintain capacity buffer and test disruption recovery |
| Scrap / expiry | 3.0% | ≤2.5% | Track lot age, FEFO, shelf life, quality holds, and batch size |
| Reconciliation accuracy | 99.4% | ≥99.5% | Resolve recurring object/unit/status mismatches |

## Days 1–30 — Establish the baseline and controls

1. Approve KPI dictionary: formula, numerator/denominator, exclusions, time zone, units, currency, period, source and accountable owner.
2. Reconcile a sample of orders, demand forecasts, supplier lines, usable stock, production confirmations, deliveries and logistics costs.
3. Launch daily critical-exception huddles with one owner and due time per issue.
4. Review suppliers for packaging and other production-critical materials; establish acknowledgement and escalation rules.
5. Validate resource calendars, changeover times, availability and inventory status definitions.
6. Confirm dashboard freshness and create a baseline for OTIF, shortages, unit logistics cost, exceptions, scrap and reconciliation accuracy.

**Deliverables:** signed KPI data dictionary, source-to-dashboard reconciliation, owner matrix, baseline scorecard, and prioritized issue log.

## Days 31–60 — Pilot targeted interventions

1. Segment forecast error by SKU/location and review bias and intermittent-demand products.
2. Pilot supplier confirmation and escalation for the highest-impact materials.
3. Review safety stock, reorder point, lead time, MOQ, lot sizing and unit conversion for packaging materials.
4. Test finite-capacity schedule adherence, frozen time fences, setup sequence and disruption scenario.
5. Introduce exception ageing, severity thresholds, and alerts only after validating data freshness and routing.
6. Run the twelve proposed validation cases in a controlled environment and record actual evidence.

**Deliverables:** corrected master data, pilot action results, test evidence, updated procedures, and measured before/after KPIs.

## Days 61–90 — Evaluate, standardize and scale

1. Compare pilot metrics with the baseline using the same definitions and time window.
2. Check for unintended consequences: lower inventory alongside shortages, lower cost alongside OTIF deterioration, or higher utilization alongside downtime.
3. Standardize successful interventions through approved work instructions and role training.
4. Expand only the validated changes to additional products, suppliers, or locations.
5. Review unresolved red KPIs with accountable leaders and agree the next cycle.
6. Retain evidence of decisions, refresh times, calculation changes, data defects, and exception closure.

**Deliverables:** signed post-pilot review, standardized process, scaled roadmap, and next-quarter improvement backlog.

## PDCA application

- **Plan:** choose a measurable problem, define the baseline, owner, hypothesis, target and timeframe.
- **Do:** change one controlled process or parameter and document approvals.
- **Check:** compare the same KPI definition against the baseline; inspect data quality and side effects.
- **Act:** standardize if effective, adjust if mixed, or roll back if the results are negative.

A KPI trend is not evidence of causality on its own. Root-cause claims should be tested with event logs, matched periods, process data, and documented evidence.
