# Product Development Test Metrics

A calculation guide for Test Managers and Test Leads. All values are fictional examples for a 4G/5G product.

## Using the Excel workbook

1. Update amber cells on **Inputs** and **Telecom**.
2. The **Dashboard** calculates the core results automatically. Formula cells should remain unchanged.
3. Keep the same release, candidate, scope and reporting window for each numerator and denominator.
4. A zero denominator returns `n.a.` rather than a misleading 0%. Excel percentage formatting multiplies the displayed fraction by 100; do not multiply it again in the formula.
5. Example text is a fixed worked example and will not change when inputs change.

The example uses candidate snapshot **13 October 2026**, weekly flow **5–11 October 2026**, and a separate 30-day post-release observation window for escaped defects.

## Core metrics and worked calculations

### 1. Requirements coverage

- **Example:** 114 / 120 = 95%.
- **Excel cell:** Dashboard!B6
- **Excel formula:** `=IF('Inputs'!B6=0,"n.a.",'Inputs'!B7/'Inputs'!B6)`
- **Used by:** Both. Linked coverage; inspect critical gaps.

### 2. Critical requirements passed

- **Example:** 27 / 30 = 90%.
- **Excel cell:** Dashboard!B7
- **Excel formula:** `=IF('Inputs'!B8=0,"n.a.",'Inputs'!B9/'Inputs'!B8)`
- **Used by:** Both. 3 critical requirements remain unproven.

### 3. Executed tests

- **Example:** 380 + 40 = 420.
- **Excel cell:** Dashboard!B8
- **Excel formula:** `=SUM('Inputs'!B11:'Inputs'!B12)`
- **Used by:** Lead. Passed + failed only.

### 4. Execution progress

- **Example:** 420 / 500 = 84%.
- **Excel cell:** Dashboard!B9
- **Excel formula:** `=IF('Inputs'!B10=0,"n.a.",B8/'Inputs'!B10)`
- **Used by:** Lead. Blocked and not run stay outside executed.

### 5. Test pass rate

- **Example:** 380 / 420 = 90.5%.
- **Excel cell:** Dashboard!B10
- **Excel formula:** `=IF(B8=0,"n.a.",'Inputs'!B11/B8)`
- **Used by:** Both. Inspect severity of failures.

### 6. Blocked tests

- **Example:** 30 blocked tests.
- **Excel cell:** Dashboard!B11
- **Excel formula:** `='Inputs'!B13`
- **Used by:** Lead. Investigate environment / dependency delays.

### 7. Tests not run

- **Example:** 50 tests not run.
- **Excel cell:** Dashboard!B12
- **Excel formula:** `='Inputs'!B14`
- **Used by:** Lead. Identify untested product areas.

### 8. Open critical defects

- **Example:** 1 critical defect.
- **Excel cell:** Dashboard!B13
- **Excel formula:** `='Inputs'!B15`
- **Used by:** Both. Review customer impact and workaround.

### 9. Open high defects

- **Example:** 5 high defects.
- **Excel cell:** Dashboard!B14
- **Excel formula:** `='Inputs'!B16`
- **Used by:** Both. Review before release.

### 10. Total open defects

- **Example:** 1 + 5 + 12 + 8 = 26.
- **Excel cell:** Dashboard!B15
- **Excel formula:** `=SUM('Inputs'!B15:'Inputs'!B18)`
- **Used by:** Both. Break down by feature and owner.

### 11. Weekly backlog change

- **Example:** 18 - 24 = -6.
- **Excel cell:** Dashboard!B16
- **Excel formula:** `='Inputs'!B19-'Inputs'!B20`
- **Used by:** Both. Negative means shrinking; assumes no reopens.

### 12. Average serious defect age (days)

- **Example:** 54 / 6 = 9 days.
- **Excel cell:** Dashboard!B17
- **Excel formula:** `=IF(SUM('Inputs'!B15:'Inputs'!B16)=0,"n.a.",'Inputs'!B21/SUM('Inputs'!B15:'Inputs'!B16))`
- **Used by:** Both. Calendar age of open critical/high defects.

### 13. Serious defects aged >7 days

- **Example:** 2 defects.
- **Excel cell:** Dashboard!B18
- **Excel formula:** `='Inputs'!B22`
- **Used by:** Both. Prioritize long-standing serious defects.

### 14. Escaped defects (30-day window)

- **Example:** 5 defects.
- **Excel cell:** Dashboard!B19
- **Excel formula:** `='Inputs'!B24`
- **Used by:** Manager. Released R1; separate from candidate snapshot.

### 15. Defect escape rate

- **Example:** 5 / (95 + 5) = 5%.
- **Excel cell:** Dashboard!B20
- **Excel formula:** `=IF(SUM('Inputs'!B23:'Inputs'!B24)=0,"n.a.",'Inputs'!B24/SUM('Inputs'!B23:'Inputs'!B24))`
- **Used by:** Manager. Same release and fixed observation window.

### 16. Regression execution progress

- **Example:** 190 / 200 = 95%.
- **Excel cell:** Dashboard!B21
- **Excel formula:** `=IF('Inputs'!B25=0,"n.a.",SUM('Inputs'!B26:'Inputs'!B27)/'Inputs'!B25)`
- **Used by:** Lead. Pass + fail divided by required regression.

### 17. Regression passed / required

- **Example:** 180 / 200 = 90%.
- **Excel cell:** Dashboard!B22
- **Excel formula:** `=IF('Inputs'!B25=0,"n.a.",'Inputs'!B26/'Inputs'!B25)`
- **Used by:** Lead. Completion and quality against full scope.

### 18. Automation coverage

- **Example:** 280 / 400 = 70%.
- **Excel cell:** Dashboard!B23
- **Excel formula:** `=IF('Inputs'!B30=0,"n.a.",'Inputs'!B31/'Inputs'!B30)`
- **Used by:** Both. Use eligible scope, not all tests.

### 19. Flaky test rate

- **Example:** 14 / 280 = 5%.
- **Excel cell:** Dashboard!B24
- **Excel formula:** `=IF('Inputs'!B31=0,"n.a.",'Inputs'!B32/'Inputs'!B31)`
- **Used by:** Lead. Inconsistent results without product changes.

### 20. Lost testing capacity

- **Example:** 16 / 360 = 4.4%.
- **Excel cell:** Dashboard!B25
- **Excel formula:** `=IF('Inputs'!B34=0,"n.a.",'Inputs'!B33/'Inputs'!B34)`
- **Used by:** Lead. Same team, week and person-hour unit.

### 21. Critical scenarios unproven

- **Example:** 3 scenarios.
- **Excel cell:** Dashboard!B26
- **Excel formula:** `='Inputs'!B35`
- **Used by:** Manager. Untested or failed; avoid duplicate counting.

### 22. Unmet non-functional targets

- **Example:** 1 target missed.
- **Excel cell:** Dashboard!B27
- **Excel formula:** `='Inputs'!B36`
- **Used by:** Manager. Performance, reliability or security target.

### 23. Unaccepted release risks

- **Example:** 2 risk register entries.
- **Excel cell:** Dashboard!B28
- **Excel formula:** `='Inputs'!B37`
- **Used by:** Manager. Review individually; counts can overlap.

## Input mapping

| Input | Excel cell | Sample value | Scope |
|---|---|---:|---|
| Total testable requirements | Inputs!B6 | 120 | Current release |
| Requirements with linked tests | Inputs!B7 | 114 | Distinct requirements, not test count |
| Critical requirements | Inputs!B8 | 30 | Current release |
| Critical requirements tested and passed | Inputs!B9 | 27 | All required tests passed |
| Planned tests | Inputs!B10 | 500 | Latest outcome per test on current candidate |
| Passed tests | Inputs!B11 | 380 | Latest result |
| Failed tests | Inputs!B12 | 40 | Latest result |
| Blocked tests | Inputs!B13 | 30 | Excluded from executed denominator |
| Not run tests | Inputs!B14 | 50 | Excluded from executed denominator |
| Open critical defects | Inputs!B15 | 1 | As of reporting date |
| Open high defects | Inputs!B16 | 5 | As of reporting date |
| Open medium defects | Inputs!B17 | 12 | As of reporting date |
| Open low defects | Inputs!B18 | 8 | As of reporting date |
| New defects this week | Inputs!B19 | 18 | Distinct valid defects |
| Closed defects this week | Inputs!B20 | 24 | Verified closures |
| Open critical/high total age (days) | Inputs!B21 | 54 | Sum of ages of the 6 open serious defects |
| Open critical/high older than 7 days | Inputs!B22 | 2 | Age >7 calendar days |
| Pre-release defects in released version | Inputs!B23 | 95 | Same released version as escaped defects |
| Escaped defects within 30 days | Inputs!B24 | 5 | Distinct confirmed defects in that version |
| Required regression tests | Inputs!B25 | 200 | Current release candidate |
| Passed regression tests | Inputs!B26 | 180 | Latest outcomes |
| Failed regression tests | Inputs!B27 | 10 | Latest outcomes |
| Blocked regression tests | Inputs!B28 | 5 | Latest outcomes |
| Not run regression tests | Inputs!B29 | 5 | Latest outcomes |
| Automation-eligible tests | Inputs!B30 | 400 | Agreed scope |
| Automated tests | Inputs!B31 | 280 | Subset of eligible tests |
| Flaky tests observed | Inputs!B32 | 14 | Among 280 automated tests in 10-run window |
| Lost testing hours | Inputs!B33 | 16 | Blocked time, summed person-hours |
| Available testing hours | Inputs!B34 | 360 | Same week and team |
| Critical scenarios untested or failed | Inputs!B35 | 3 | Distinct critical scenarios |
| Unmet non-functional targets | Inputs!B36 | 1 | Count of agreed targets missed |
| Unaccepted release risks | Inputs!B37 | 2 | Risk register entries awaiting acceptance/action |

## Telecom calculations

| Metric | Calculation example | Excel result cell | Formula |
|---|---|---|---|
| Registration success rate | 99800 / 100000 = 99.80% | Telecom!D6 | `=IF(C6=0,"n.a.",B6/C6)` |
| PDU session success rate | 98500 / 100000 = 98.50% | Telecom!D7 | `=IF(C7=0,"n.a.",B7/C7)` |
| Target UE scale reached | 95000 / 100000 = 95.0% | Telecom!D8 | `=IF(C8=0,"n.a.",B8/C8)` |
| Procedure throughput (per second) | 900000 / 600 = 1500.0 | Telecom!D9 | `=IF(C9=0,"n.a.",B9/C9)` |
| Packet loss rate | 2500 / 1000000 = 0.25% | Telecom!D10 | `=IF(C10=0,"n.a.",B10/C10)` |
| XDR completeness | 997000 / 1000000 = 99.70% | Telecom!D11 | `=IF(C11=0,"n.a.",B11/C11)` |
| CP/UP correlation rate | 98000 / 100000 = 98.00% | Telecom!D12 | `=IF(C12=0,"n.a.",B12/C12)` |
| Unexpected session drop rate | 100 / 100000 = 0.10% | Telecom!D13 | `=IF(C13=0,"n.a.",B13/C13)` |
| Recovery time (seconds) | 85 / 60 = 141.7% | Telecom!D14 | `=IF(C14=0,"n.a.",B14/C14)` |
| Latency p95 (ms) | 120 / 100 = 120.0% | Telecom!D15 | `=IF(C15=0,"n.a.",B15/C15)` |
| Memory growth (MB/hour) | 240 / 24 = 10.0 | Telecom!D16 | `=IF(C16=0,"n.a.",B16/C16)` |

Registration and PDU success rates use separate attempt populations. Count retries consistently. A scale ratio of 95% says the run reached 95,000 concurrent UEs; it does not prove quality at 100,000 UEs. Throughput here measures procedures/s, not packets/s or bit/s. Recovery at 85/60 = 141.7% and p95 at 120/100 = 120% both exceed their maximum targets.

### Calculating p95 from raw latency samples

With numeric latency samples in cells B2:B101, use `=PERCENTILE.INC(B2:B101,0.95)` in Excel, then enter the measured result in Telecom!B15. For 20 sorted samples of 10, 20, ..., 200 ms, inclusive p95 is **190.5 ms** (interpolation at rank 19.05). The workbook receives p95 as an input because raw latency samples were not supplied.

### Defect age example

Use `=ReportingDate-OpenedDate` for each open defect, with real Excel dates. If the reporting date is 13 Oct 2026 and opened date is 3 Oct 2026, age is 10 calendar days. Serious defect ages of 2, 4, 6, 7, 15 and 20 days total 54 days, average 9 days, with 2 defects older than 7 days. Closed defects are excluded.

## Reading the results

- Requirements coverage measures linkage. Critical requirements passed measures evidence of working behavior.
- Executed means passed plus failed. Blocked and not-run tests remain visible outside the executed denominator. Use the latest outcome once per test on the chosen candidate.
- Weekly backlog change is new minus verified closed defects. Add reopened defects and account for invalidated/duplicate defects if those flows exist in your process.
- Escape rate is escaped / (pre-release + escaped), using distinct confirmed defects from the same released version and a stated post-release window. The count can increase as the observation window grows.
- Regression readiness needs execution, passed/required, failure severity and the remaining blocked/not-run scope together.
- Flaky rate uses distinct flaky tests among the automated test population in a defined 10-run window. Infrastructure failures should be identified separately.
- Lost capacity uses person-hours on both sides. Do not divide team person-hours by machine elapsed hours.
- Release risk is reviewed through separate counts and actual risk entries. Do not add overlapping critical scenarios, defects and risk entries into an invented score. Record owner, impact, mitigation and acceptance for each risk.
- Project-specific release criteria should be agreed with stakeholders. There is no universal pass-rate threshold that establishes readiness.

## Weekly review

The Test Lead checks failures, blocked testing, regression, automation reliability and defect ownership daily. The Test Manager reviews critical coverage, defect severity and age, escaped defects, performance targets and unresolved release risks with stakeholders. Retain each weekly snapshot to compare trends.
