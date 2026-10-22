# KPI Analysis and Management Dictionary

This document reproduces the main simulated dataset and KPI logic used in the Week 6 Word report. Every monthly value is an illustrative learning assumption, not live SAP output or verified company performance.

## 1. Six-month dataset

See the machine-readable copy at ../data/simulated-kpi-dataset.csv. Values below are transcribed from the final report.

| Metric | Unit | Apr | May | Jun | Jul | Aug | Sep |
|---|---|---:|---:|---:|---:|---:|---:|
| Actual demand | tonnes | 520 | 535 | 548 | 575 | 590 | 610 |
| Shipped volume | tonnes | 496 | 513 | 530 | 559 | 578 | 598 |
| Volume fill rate | % | 95.4 | 95.9 | 96.7 | 97.2 | 98.0 | 98.0 |
| Customer OTIF | % | 86.0 | 87.5 | 88.0 | 90.0 | 91.2 | 93.0 |
| Forecast accuracy (1−WAPE) | % | 81.0 | 82.5 | 84.0 | 85.5 | 87.0 | 88.5 |
| Production schedule adherence | % | 82.0 | 83.5 | 85.0 | 87.0 | 89.0 | 91.0 |
| Supplier OTIF | % | 78.0 | 80.0 | 82.0 | 84.0 | 87.0 | 89.0 |
| Inventory days of supply | days | 34 | 33 | 32 | 31 | 29 | 27 |
| Logistics cost per shipped tonne | INR/tonne | 6800 | 6720 | 6590 | 6460 | 6320 | 6150 |
| Median critical-exception resolution | hours | 16 | 14 | 13 | 10.5 | 8 | 6 |
| Packaging shortage incidents | count/month | 9 | 8 | 7 | 6 | 4 | 3 |
| Packaging capacity utilization | % | 88 | 89 | 90 | 91 | 91 | 92 |
| Scrap / expiry rate | % | 3.8 | 3.7 | 3.6 | 3.4 | 3.2 | 3.0 |
| Data reconciliation accuracy | % | 96.0 | 97.0 | 97.8 | 98.5 | 99.0 | 99.4 |

## 2. KPI dictionary and proposed thresholds

Targets are illustrative management thresholds for this scenario, not universal benchmarks.

| KPI | Calculation / definition | Proposed target | Management use |
|---|---|---|---|
| Customer OTIF | Orders delivered on time and in full ÷ total orders due × 100 | ≥95% | Combined service-date and completeness outcome |
| Forecast accuracy | (1 − WAPE) × 100, where WAPE = sum of absolute forecast error ÷ sum of actual demand | ≥90% | Demand-planning quality and supply stability |
| Production schedule adherence | Operations completed as planned ÷ scheduled operations due × 100 | ≥92% | Schedule reliability and production execution |
| Supplier OTIF | Supplier delivery lines complete and on time ÷ supplier lines due × 100 | ≥95% | Procurement reliability |
| Inventory days of supply | Usable stock ÷ average daily demand | 25–30 days | Balance stock-out exposure and excess |
| Logistics cost per tonne | In-scope logistics cost ÷ shipped tonnes | ≤₹6,460/t | Cost-to-serve and transport performance |
| Critical-exception resolution | Median time from exception logging to verified business closure | ≤4 hours | Responsiveness to high-impact problems |
| Packaging shortage incidents | Count of events where packaging unavailability blocks planned production | ≤2/month | Component availability and lost production |
| Packaging resource utilization | Scheduled production load ÷ available resource capacity × 100 | 85–92% band | Capacity loading with reasonable buffer |
| Scrap / expiry rate | Scrap and expired volume ÷ produced volume × 100 | ≤2.5% | Waste, quality, shelf-life, and cost |
| Data reconciliation accuracy | Matched source/target document-quantity-status samples ÷ samples checked × 100 | ≥99.5% | Trustworthiness of integrated reporting |
| Volume fill rate | Shipped tonnes ÷ demand tonnes × 100 | ≥98% | Quantity fulfillment, distinct from OTIF |

## 3. Trend interpretation

- Customer OTIF improves from 86.0% to 93.0% (+7.0 percentage points) but remains two points below the proposed target.
- Forecast accuracy rises from 81.0% to 88.5% (+7.5 points) and remains 1.5 points below target.
- Schedule adherence rises from 82.0% to 91.0% (+9 points) and remains one point below target.
- Supplier OTIF rises from 78.0% to 89.0% (+11 points), still six points below target and a likely upstream focus area.
- Inventory falls from 34 to 27 days and ends inside the scenario's 25–30 day range. The reduction should be reviewed alongside fill rate and shortage incidents to ensure that lower stock is not undermining service.
- Logistics cost per tonne falls by INR 650. Calculation: (6,800 − 6,150) ÷ 6,800 × 100 ≈ 9.6%.
- Median exception resolution falls from 16 to 6 hours, but is still two hours over the proposed four-hour maximum.
- Packaging shortages fall from nine to three per month but are still above the two-event target.
- Utilization rises to 92%, the upper boundary of the proposed band; additional loading without better reliability could reduce recovery room.
- Scrap/expiry improves from 3.8% to 3.0% but misses the 2.5% threshold.
- Data reconciliation accuracy reaches 99.4%, just under the 99.5% target.

These changes show direction within the simulated period. A trend alone does not establish that an initiative caused the improvement; the proposed experiments, baselines, and validation checks should be used to test whether changes persist.

## 4. Reporting design

A practical KPI view should display the current period, prior-period value, trend, target, variance, refresh timestamp, data-quality flag, owner, and next action. Use a consistent fiscal calendar, unit, currency, and numerator/denominator definition. Customer OTIF must not be substituted for volume fill rate; they measure different outcomes.

In a legacy SAP APO deployment, planning books and key figures can support planning-oriented views, while the Plan Monitor can compare planning objects, versions, and periods. For another SAP ERP/S/4HANA landscape, use the reporting and analytics components actually deployed. SAP IBP custom alerts are relevant only where the applicable IBP applications are deployed.

## 5. Suggested review cadence

- Daily: critical shortages, late supplier confirmations, exceptions, and at-risk orders.
- Weekly: forecast deviations, resource loading, production adherence, supplier reliability, and upcoming demand peaks.
- Monthly: scorecard, target gaps, logistics unit cost, scrap/expiry, and data reconciliation.
- Quarterly: validate KPI definitions, owners, targets, data lineage, and whether improvement actions should be standardized, adjusted, or stopped.
