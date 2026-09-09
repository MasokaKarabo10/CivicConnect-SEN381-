# 1. Constraints Analysis & Architectural Trade-offs (Wonderpark Estates)

## 1.1 Core Engineering Constraints Baseline

| Constraint Type | Formal Statement | Engineering Implication |
| :--- | :--- | :--- |
| **Schedule** | The project must progress through four predefined SEN381 milestones within a fixed academic delivery window; no deadline extensions are possible. | Wonderpark Estates' scope must be sized strictly to what three student engineers can design, verify, test, and document per milestone. The team must resist scope creep beyond the core residential-complex ticketing baseline. |
| **Cost & Resources** | Zero software procurement budget; the team must rely exclusively on free or community hosting, database, and CI/CD service tiers. | Must rigorously document free-tier operational limits (memory caps, compute throttling, execution quotas) and project the true operational expenditure if Wonderpark Estates were to deploy commercially. |
| **Quality** | Core Non-Functional Requirements (usability, auditability, reliability) must be measurable and verifiable, not merely claimed. | Acceptance criteria defined in Person A's baseline must remain quantifiable (e.g., deterministic status transitions, exact response latency thresholds) so they can be validated via automated test suites in Milestone 3. |
| **Security** | Security is a lifecycle-wide constraint enforced from the beginning throughout , not an operational add-on. | Requirements must explicitly flag where residents' unit numbers, contact numbers, and maintenance records appear (NFR-002) so that Milestone 2 architecture incorporates boundary validation and authorization models from day one. |
| **Scope** | Committed scope must be baselined in PED v1.0; no informal or unrecorded feature expansion is permitted. | Any requirement or capability proposed after baseline sign-off (e.g., third-party contractor dispatch engines, multi-tenancy) mandates a formal Engineering Change Request with trade-off impact analysis. |

---

## 1.2 System Trade-Off Analysis

* **Deliberate Scope Exclusion:** Wonderpark Estates' CivicConnect deployment deliberately excludes integrated levy/payment processing and multi-tenant estate management.

* **Constraint Interaction:** *Schedule & Team Capacity Security Attack Surface & Verification Rigor*
* **Defensible Engineering Rationale:** 
  > Both payment gateways and multi-tenant isolation materially expand the system's security surface (financial regulatory compliance, complex tenant-isolation bugs) and schedule risk beyond what three engineers can control, test, and defend within the SEN381 timeline. A smaller, fully controlled, and rigorously verified engineering baseline demonstrates significantly higher software engineering maturity than a bloated, defect-prone application.