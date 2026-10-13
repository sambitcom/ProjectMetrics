# ETS 2702: Solution-Level Project and Delivery Manager Metrics

## 1. Release Model & Baseline Overview

This dashboard covers **5 parallel solution teams** delivering across 5 component epics linked 1:1 with solution epics.

| Item | Per Solution Team | ETS 2702 Total |
|---|---:|---:|
| Solution Epics | 1 | 5 |
| Linked Component Epics | 1 | 5 |
| Team Members | 5 | 25 |
| Weekly Team Velocity | 10 points | 50 points (Nominal Aggregate) |
| Total Scope | 15 points (5 FRs) | 75 points (25 FRs) |
| Must Scope | 12 points (4 FRs) | 60 points (20 FRs) |
| Should Scope | 3 points (1 FR) | 15 points (5 FRs) |
| Completed Baseline Spillover | Varies | 9 points (3 Must FRs) |

---

## 2. Baseline Status Across Solution Teams

| Solution Team / Epic | Linked Component | Full Points | Done Stories | Done Points | Remaining Full Points | Remaining Must Points |
|---|---|---:|---:|---:|---:|---:|
| **Team 1 / SOL-1** | CMP-1 | 15 | 1 | 3 | 12 | 9 |
| **Team 2 / SOL-2** | CMP-2 | 15 | 1 | 3 | 12 | 9 |
| **Team 3 / SOL-3** | CMP-3 | 15 | 1 | 3 | 12 | 9 |
| **Team 4 / SOL-4** | CMP-4 | 15 | 0 | 0 | 15 | 12 |
| **Team 5 / SOL-5** | CMP-5 | 15 | 0 | 0 | 15 | 12 |
| **Release Total** | **5 Components** | **75** | **3** | **9** | **66** | **51** |

---

## 3. Core Delivery Progress Metrics

* **Solution Epic Completion (%)**
  $$\text{Epic Completion} = \frac{\text{Done Points in Epic}}{\text{Total Points in Epic}} \times 100$$
  * **SOL-1, SOL-2, SOL-3:** $\frac{3}{15} \times 100 = \mathbf{20\%}$
  * **SOL-4, SOL-5:** $\frac{0}{15} \times 100 = \mathbf{0\%}$

* **Release Scope Completion (%)**
  $$\text{Release Completion} = \frac{\text{Total Unique Done Points}}{\text{Total Unique Release Scope}} \times 100 = \frac{9}{75} \times 100 = \mathbf{12\%}$$

* **Must Scope Completion (%)**
  $$\text{Must Completion} = \frac{\text{Done Must Points}}{\text{Total Must Scope}} \times 100 = \frac{9}{60} \times 100 = \mathbf{15\%}$$

---

## 4. Forecasting & Parallel Execution Milestones

* **Team Forecast Formula:** $\lceil \frac{\text{Remaining Team Points}}{\text{Team Velocity}} \rceil$
* **Release Team-Work Milestone:** $\max(\text{Team Forecasts})$

### Per-Team Milestones (at 10 pts/week velocity)

| Team | Remaining Must Points | Must Forecast | Remaining Full Points | Full Forecast |
|---|---:|---:|---:|---:|
| **Team 1** | 9 | 1 week | 12 | 2 weeks |
| **Team 2** | 9 | 1 week | 12 | 2 weeks |
| **Team 3** | 9 | 1 week | 12 | 2 weeks |
| **Team 4** | 12 | 2 weeks | 15 | 2 weeks |
| **Team 5** | 12 | 2 weeks | 15 | 2 weeks |

* **Must Team-Work Milestone:** $\max(1, 1, 1, 2, 2) = \mathbf{2\text{ weeks}}$
* **Full Scope Team-Work Milestone:** $\max(2, 2, 2, 2, 2) = \mathbf{2\text{ weeks}}$

---

## 5. Forecast Sensitivity Analysis

| Velocity per Team | Nominal Aggregate | Must Team-Work Forecast | Full Team-Work Forecast |
|---|---:|---:|---:|
| **7 pts/week (Slower)** | 35 pts/wk | 2 weeks | 3 weeks |
| **10 pts/week (Baseline)** | 50 pts/wk | 2 weeks | 2 weeks |
| **13 pts/week (Faster)** | 65 pts/wk | 1 week | 2 weeks |

---

## 6. Solution Integration & Release Gates

$$\text{Release-Ready Forecast} = \text{Latest Team Milestone} + \sum (\text{Sequential Release Gate Weeks})$$

* **Solution Acceptance Coverage (%):** $\frac{\text{Agreed Solution Scenarios with Tests}}{\text{Total Agreed Solution Scenarios}} \times 100$
* **Solution Verified Rate (%):** $\frac{\text{Passing Solution Scenarios}}{\text{Total Agreed Solution Scenarios}} \times 100$
* **Mandatory Automation Coverage (%):** $\frac{\text{Fully Automated Must FRs}}{\text{Total Must FRs}} \times 100$
  * **Baseline:** $\frac{3}{20} \times 100 = \mathbf{15\%}$
  * **Target:** $\mathbf{100\%}$ prior to release.

---

## 7. Delivery Manager Weekly Dashboard Summary

| Metric | Baseline / Target | Delivery Manager Focus / Action Item |
|---|---|---|
| **Release Completion** | 12% (9 / 75 pts) | Track unique story IDs through both solution and component views. |
| **Must Completion** | 15% (9 / 60 pts) | Protect Must priority items over Should scope. |
| **Critical Bottlenecks** | Teams 4 & 5 (12 Must pts left) | Focus cross-team dependency removal on Teams 4 and 5. |
| **Must Automation** | 15% baseline $\rightarrow$ 100% target | Enforce mandatory Definition of Done (Code + Test + Automation). |
| **Release Gates** | Unestimated (Default) | Agree on post-development integration duration to determine final release date. |