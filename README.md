# SAP SCM Week 6 — Performance Evaluation and Continuous Improvement

**Final internship assessment | Deccan Harvest Foods Pvt. Ltd. (fictional) | April–September 2026 simulated period**

## Six-Assessment Portfolio Navigation

This assessment is part of my six-assessment SAP SCM internship portfolio. The series is structured as one connected learning journey from network planning through performance improvement.

| Week | Assessment | Repository |
|---|---|---|
| 1 | Supply Chain Network Planning | [Open Week 1](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Supply-Chain-Network-Planning) |
| 2 | Master Data & Inventory Optimization | [Open Week 2](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Master-Data-Inventory-Optimization) |
| 3 | Logistics & Distribution Network Design | [Open Week 3](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Logistics-Distribution-Network-Design) |
| 4 | Production Planning & Scheduling Analysis | [Open Week 4](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Week4-Production-Planning-Scheduling-Analysis) |
| 5 | Supply Chain Integration & Collaboration | [Open Week 5](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Week5-Supply-Chain-Integration-Collaboration) |
| 6 | Performance Evaluation & Continuous Improvement | [Open Week 6](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Week6-Performance-Evaluation-Continuous-Improvement) |

**Central portfolio hub:** [SAP-SCM-Internship-Portfolio](https://github.com/hrudhaipremkumarpatwari/SAP-SCM-Internship-Portfolio) — the central index for the complete series.



This repository contains a KPI-based performance evaluation and continuous-improvement proposal for a fictional millet-based ready-to-cook food manufacturer. It brings together supply-chain themes from earlier assessments—demand, procurement, inventory, production scheduling, distribution, integration, and exception handling—into one review and improvement plan.

## Assessment objectives

- Define a balanced set of supply-chain KPIs and state how each should be calculated.
- Review six months of simulated performance and identify trends, target gaps, and risks.
- Explain how SAP SCM/APO reporting concepts and the relevant reporting tools in the deployed landscape can support monitoring.
- Translate analysis into actions, owners, review cadence, validation tests, and a 30/60/90-day improvement roadmap.
- Apply the Plan-Do-Check-Act (PDCA) cycle for continuous improvement.

## Headline findings from the simulation

| KPI | April | September | Direction / interpretation |
|---|---:|---:|---|
| Customer OTIF | 86.0% | 93.0% | Improved by 7 percentage points, but below proposed 95% target |
| Forecast accuracy | 81.0% | 88.5% | Improved by 7.5 points, still below proposed 90% target |
| Production schedule adherence | 82.0% | 91.0% | Improved by 9 points, slightly below proposed 92% target |
| Supplier OTIF | 78.0% | 89.0% | Improved by 11 points, but below proposed 95% target |
| Inventory days of supply | 34 days | 27 days | Moved into the proposed 25–30 day range |
| Logistics cost per shipped tonne | ₹6,800 | ₹6,150 | Reduced by ₹650/t, approximately 9.6% |
| Median critical-exception resolution | 16 hours | 6 hours | Improved, but remains above proposed ≤4-hour target |
| Packaging shortage incidents | 9/month | 3/month | Down by six incidents, still above proposed ≤2/month |
| Packaging resource utilization | 88% | 92% | At the upper edge of the proposed 85–92% control band |
| Scrap / expiry rate | 3.8% | 3.0% | Improving, but above proposed ≤2.5% target |
| Data reconciliation accuracy | 96.0% | 99.4% | Near the proposed ≥99.5% target |

The dataset is constructed for analysis and is not historical company data. The trend does not by itself prove that any one action caused the change.

## Repository structure

- **docs/** — final Word assessment, KPI definitions and results, risk and validation register, improvement roadmap, and copy-ready portal description.
- **data/** — simulated monthly KPI dataset as a CSV for reproducible charting and review.
- **diagrams/** — editable Mermaid workflows for performance monitoring and the PDCA cycle.
- **README.md** — project overview, headline findings, navigation, and scope.

## Files

1. [Final Word report](docs/SAP_SCM_Week6_Performance_Evaluation_Continuous_Improvement_Hrudhai_Final.docx)
2. [KPI analysis and dictionary](docs/kpi-analysis.md)
3. [Risk register and validation tests](docs/risk-and-validation.md)
4. [Continuous-improvement roadmap](docs/continuous-improvement-roadmap.md)
5. [Portal submission description](docs/portal-submission-description.md)
6. [Simulated monthly KPI dataset](data/simulated-kpi-dataset.csv)
7. [Performance monitoring flow](diagrams/performance-monitoring-flow.md)
8. [PDCA improvement cycle](diagrams/pdca-improvement-cycle.md)

## SAP monitoring context

The report explains planning books, key figures, KPI reporting, and the Plan Monitor in the relevant legacy SAP APO context. It discusses the appropriate source-system reporting and analytics layer for the actual ERP/S/4HANA landscape, and mentions SAP IBP custom alerts only where that product and the relevant applications are deployed. Feature availability and configuration must be confirmed for the organization's release and implementation.

## Scope and limitations

All company details, monthly KPI values, targets, trends, dashboard graphics, root-cause hypotheses, and benefit estimates are illustrative. This repository is a learning simulation and reporting/configuration blueprint. It does not claim that the KPIs were extracted from a live SAP system, that SAP configuration was executed, or that the proposed validation tests were run in production.

The proposed targets are internal scenario thresholds, not universal industry benchmarks or SAP standard values. For real use, confirm KPI scope, numerator, denominator, time window, currency, unit of measure, data source, owner, refresh time, and escalation rule before comparing performance.
