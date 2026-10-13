# ETS 2702 Release — Test Metrics and Worked Example

## Release scope

| Scope item | Calculation | ETS 2702 baseline |
|---|---|---:|
| Solution-level epics | Given | 5 |
| Component-level epics | Given | 5 |
| Unique user stories | 5 component epics × 5 stories | 25 |
| Functional requirements | 5 component epics × 5 FRs | 25 |
| Must requirements | 5 component epics × 4 Must FRs | 20 |
| Remaining requirements | 25 − 20 | 5 |
| Testable tasks | 25 stories × 10 tasks | 250 |
| Must testable tasks | 20 Must FRs × 10 tasks | 200 |

**Scope assumption:** The 5 solution epics and 5 component epics are linked views of the same 25 stories. SOL-1 maps to CMP-1, and so on. Each pair shares 5 unique story IDs. If each level has its own independent set of 25 stories, there would instead be 50 stories and 500 tasks. This workbook uses your stated total of 25.

**Traceability assumption:** Each of the 5 stories in a component epic maps to one of its 5 functional requirements, with 10 agreed verification tasks per story/requirement. Real many-to-many mappings need explicit links and deduplication. A testable task is a verification item; it is not necessarily a separate test case.

**MoSCoW baseline:** You specified a minimum of 4 Must requirements per component epic. This example uses exactly 4 Must and 1 Should per epic. That gives 20 Must; if the fifth requirement is also Must, the automation target expands. Could and Won’t are available classifications but none are assigned in this baseline.

## One component epic explained

CMP-1 contains 5 FRs and 5 stories. Its linked solution epic is SOL-1.

| Requirement | Story | MoSCoW | Testable tasks | Automation obligation |
|---|---|---|---:|---|
| FR-01 | US-01 | Must | 10 | Automate all 10 |
| FR-02 | US-02 | Must | 10 | Automate all 10 |
| FR-03 | US-03 | Must | 10 | Automate all 10 |
| FR-04 | US-04 | Must | 10 | Automate all 10 |
| FR-05 | US-05 | Should | 10 | Outside mandatory automation scope |

Per component epic: **50 testable tasks**, of which **40 belong to Must requirements**. The Should requirement remains part of the test baseline even though it is outside the Must automation obligation. The five component areas are example labels: Registration, Session Management, Mobility, Paging and Monitoring.

## 1. MoSCoW scope compliance

**Must requirements per component epic = Count of FRs classified Must in that epic.**

CMP-1 has 4 Must out of 5 FRs. It meets the minimum of 4. The same applies to all 5 epics, so **5 of 5 epics meet the minimum**.

**Release Must share = Must FRs ÷ Total FRs × 100 = 20 ÷ 25 × 100 = 80%.** This is scope composition, not quality or completion.

## 2. Requirements test coverage

For ETS 2702, count an FR as fully covered when **all its 10 agreed verification tasks have relevant tests designed**. A single test link is insufficient under this rule.

**Requirement coverage = Fully covered FRs ÷ In-scope FRs × 100.**

In the sample, FR-25 has tests for only 5 of its 10 tasks. The other 24 FRs have all 10 covered. **Coverage = 24 ÷ 25 × 100 = 96%.**

FR-25 is Should. All 20 Must FRs have their tests designed. **Must requirement coverage = 20 ÷ 20 × 100 = 100%.**

**Task coverage = Tasks with tests ÷ Total testable tasks × 100 = 245 ÷ 250 × 100 = 98%.**

These percentages differ because one counts whole requirements and the other counts individual verification items.

## 3. Mandatory automation coverage

Your target is **automation of every Must requirement**. Count a Must FR as fully automated only when all 10 agreed tasks have tests designed and usable automation implemented. Automation does not mean the latest execution passed.

**Must task automation coverage = Automated Must tasks ÷ All Must tasks × 100.**

**Must requirement automation coverage = Fully automated Must FRs ÷ Total Must FRs × 100.**

| Component epic | Must FRs | Fully automated Must FRs | Automated Must tasks | Requirement coverage | Task coverage |
|---|---:|---:|---:|---:|---:|
| CMP-1 | 4 | 4 | 40 / 40 | 100% | 100% |
| CMP-2 | 4 | 4 | 40 / 40 | 100% | 100% |
| CMP-3 | 4 | 4 | 40 / 40 | 100% | 100% |
| CMP-4 | 4 | 3 | 35 / 40 | 75% | 87.5% |
| CMP-5 | 4 | 2 | 20 / 40 | 50% | 50% |
| Release | 20 | 17 | 175 / 200 | 85% | 87.5% |

FR-19 has only 5 of 10 tasks automated. FR-22 and FR-23 have none automated. Therefore **17 ÷ 20 × 100 = 85%** of Must requirements are fully automated, while **175 ÷ 200 × 100 = 87.5%** of Must tasks are automated.

The target is **not met**. Automate the remaining **25 Must tasks across 3 Must FRs**: 5 in FR-19, 10 in FR-22 and 10 in FR-23. Automating Should tasks would not close this Must gap.

## 4. Test execution progress

Sample latest outcomes for the 250 tasks: **227 passed, 3 failed, 5 blocked and 15 not run**.

**Executed tasks = Passed + Failed = 227 + 3 = 230.**

**Execution progress = Executed ÷ Total tasks × 100 = 230 ÷ 250 × 100 = 92%.**

**Pass rate = Passed ÷ Executed × 100 = 227 ÷ 230 × 100 = 98.7%.**

Blocked and not-run items are outside the executed denominator. Use one latest applicable result per task on the selected release candidate; do not add repeat runs to the task count.

## 5. Verified Must requirements and user stories

An FR or story is verified when **all its 10 required tasks have tests designed and have passed**.

FR-19 has 7 passed and 3 failed tasks. FR-22 has 5 passed and 5 blocked tasks. FR-23 has 10 not-run tasks. These 3 Must requirements are not verified.

**Verified Must rate = Fully verified Must FRs ÷ Total Must FRs × 100 = 17 ÷ 20 × 100 = 85%.**

FR-25 also remains unverified because 5 of its tasks are not run and lack designed tests. **Verified stories = 21 of 25 = 84%.**

Automation completion and functional verification are separate: a fully automated test can fail, and a manually executed test can pass. Story verification here concerns these test tasks; full Definition of Done may include additional work.

## 6. Solution-level reporting

SOL-4 reads the status of its linked component epic CMP-4. It has 5 stories, 4 Must FRs, 3 fully automated Must FRs and 3 fully verified Must FRs. Its Must automation and verification rates are both **3 ÷ 4 × 100 = 75%** in this sample.

Report release totals using the 25 unique story IDs and 25 unique FR IDs. Do not add solution totals to component totals. A shared scope view does not create another 250 tasks. Cross-component integration tests can be added separately when their actual scope is specified.

## How to use the workbook

- **Release:** calculated scope, coverage, automation and execution metrics.
- **Epics:** the 5 solution/component pairs and their Must progress.
- **Requirements:** 25 FRs, MoSCoW classifications, story links and calculated status.
- **Stories:** 25 unique stories with 10 expected tasks each.
- **Tasks:** 250 verification items. Update amber fields for test design, automation and latest result.

The baseline structure is fixed for this example. Requirement and task IDs carry traceability. Keep the row-to-requirement links intact when updating; do not independently reorder source rows. When the priority of an FR changes, its task priority and the Must automation population update automatically. If you add stories or tasks, extend the formulas and ranges.

Task labels are placeholders for actual acceptance-criteria checks. Replace them with your checks, such as positive, negative, boundary and recovery behavior. Automation Yes means implemented and usable in the agreed pipeline, not merely planned. Input checks flag automation or pass/fail results recorded without a designed test.

## What the Test Lead and Test Manager conclude

The sample has **100% test design coverage for Must requirements**, but mandatory automation is only **85% complete at requirement level**. Three Must requirements remain unverified. The Test Lead addresses the 25 missing automation items and the failed, blocked and not-run tasks. The Test Manager reviews those Must gaps with their owners before accepting the release. The **98.7% task pass rate alone does not establish readiness**.
