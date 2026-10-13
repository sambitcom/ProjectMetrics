# ETS 2702: Scrum Master Metrics and Release Forecast

## Planning baseline

This guide keeps the ETS 2702 structure and uses a new planning snapshot: **3 completed spillover stories**. The earlier test guide's illustrative 21 verified stories are not used as delivery progress here.

| Item | Baseline |
|---|---:|
| Component epics | 5 |
| Stories / FRs per component epic | 5 |
| Unique stories and functional requirements | 25 |
| Must FRs per component epic | 4 |
| Must / Should requirements | 20 / 5 |
| Story points per FR and its linked story | 3 |
| Total scope | 25 × 3 = 75 points |
| Must scope | 20 × 3 = 60 points |
| Testable tasks | 25 × 10 = 250 |
| Must verification / automation tasks | 20 × 10 = 200 |
| Team size | 5 members |
| Team velocity | 10 completed points per one-week sprint |
| Completed spillover stories | 3 stories = 9 points |

**One team serves all 5 component epics.** Velocity 10 belongs to the whole team; do not multiply it by 5 members or 5 epics. The 5 solution epics remain linked views of the same stories and do not add another 75 points.

**One FR maps to one 3-point story.** Its 10 testable tasks are included in the story estimate; they are not 10 additional 3-point stories. The estimate and velocity must include the agreed Definition of Done, including all required verification and automation of Must requirements. Otherwise this predicts feature implementation only and additional release work must be estimated.

**Completed spillover assumption:** US-01, US-02 and US-06 are Must stories carried over from an earlier sprint and now Done. Their 9 points are already included in the 75-point release scope. Remove them once from remaining work. They are not 3 stories still waiting to be finished.

The example uses exactly 4 Must and 1 Should per epic. A fifth Must expands the mandatory scope. No release start date or deadline was supplied, so forecasts are expressed as weeks from the next planning point.

## Component-level baseline

| Component epic | Total stories | Total points | Done stories | Done points | Remaining points | Remaining Must stories | Remaining Must points |
|---|---:|---:|---:|---:|---:|---:|---:|
| CMP-1 Registration | 5 | 15 | 2 | 6 | 9 | 2 | 6 |
| CMP-2 Session Management | 5 | 15 | 1 | 3 | 12 | 3 | 9 |
| CMP-3 Mobility | 5 | 15 | 0 | 0 | 15 | 4 | 12 |
| CMP-4 Paging | 5 | 15 | 0 | 0 | 15 | 4 | 12 |
| CMP-5 Monitoring | 5 | 15 | 0 | 0 | 15 | 4 | 12 |
| ETS 2702 total | 25 | 75 | 3 | 9 | 66 | 17 | 51 |

The sample placement of the 3 completed stories is an assumption, not reported project data. Adjust it to your actual story IDs.

## 1. Release progress and remaining scope

**Release completion = Done points ÷ Total release points × 100.**

ETS 2702 completion = **9 ÷ 75 × 100 = 12%**. Remaining work = **75 − 9 = 66 points**, or **22 stories**.

**Must completion = Done Must points ÷ Total Must points × 100 = 9 ÷ 60 × 100 = 15%.** Remaining Must work = **60 − 9 = 51 points**, or **17 stories**.

At component level, CMP-1 completion is **6 ÷ 15 × 100 = 40%**. CMP-2 is **3 ÷ 15 × 100 = 20%**. The other epics are 0%. Count points only when the story is Done under the agreed Definition of Done.

## 2. Team velocity

**Actual sprint velocity = Sum of points of stories becoming Done during that sprint.**

**Average velocity = Total Done points across selected completed sprints ÷ Number of those sprints.**

For illustration only, sprint velocities of 9, 12 and 9 give **(9 + 12 + 9) ÷ 3 = 10 points/sprint**. Your supplied velocity is 10; no actual history was provided to verify its stability.

Credit a carried-over story once, in the sprint where it becomes Done. If the 3 completed spillover stories became Done in the current sprint, they contribute 9 points to that sprint's velocity. If they finished before it, they contribute only to release progress, not current sprint velocity. Partial tasks do not earn partial story velocity.

Velocity supports forecasting for this team. Do not use it to rank individual members or compare teams with different estimation scales.

## 3. Story throughput and weekly planning

**Story throughput = Number of stories becoming Done per sprint.**

All stories are 3 points. Average point velocity suggests **10 ÷ 3 = 3.33 stories/week** over time. Actual stories are indivisible and must be Done to count.

If 10 points is treated as a firm weekly planning limit, plan **floor(10 ÷ 3) = 3 whole stories**, or **9 points/week**. One point of numerical headroom is not proof of idle capacity: dependencies, maintenance and support still consume time.

A historical average of 10 is not itself a hard capacity limit. Some sprints may finish 4 stories (12 points). This is why the average-velocity forecast and conservative whole-story plan differ.

## 4. ETS 2702 release prediction

**Average-velocity forecast = Round remaining points ÷ Velocity upward to a whole sprint.**

- Must scope: **51 ÷ 10 = 5.1 → 6 one-week sprints**.
- Full scope: **66 ÷ 10 = 6.6 → 7 one-week sprints**.

**Conservative whole-story forecast = Round remaining stories ÷ Planned whole stories per sprint upward.**

- Must scope: **17 ÷ 3 = 5.67 → 6 weeks**.
- Full scope: **22 ÷ 3 = 7.33 → 8 weeks**.

**Planning conclusion:** Target **Must completion in 6 weeks** and plan **full scope in 8 weeks** if weekly commitments stay within 10 points and every story is 3 points. The 7-week full-scope point forecast needs at least one 4-story sprint: 6 sprints × 3 stories + 1 sprint × 4 stories = 22. That is a 12-point sprint and must be feasible for the team.

Must completion is a candidate milestone. Shipping only Must scope requires agreement to defer the 5 Should requirements and completion of all release criteria. Cross-component integration, security, defects, deployment or acceptance work outside story estimates must be added before treating this as a release-ready date.

## 5. An eight-week Must-first plan

This is an illustrative sequence, not a prescribed Sprint Goal. Select a coherent goal and reorder stories when dependencies or business value require it.

| Week | Planned delivery | Stories | Points | Cumulative release Done points | Remaining release points |
|---|---|---:|---:|---:|---:|
| Baseline | 3 spillover stories already Done | 3 | 9 | 9 | 66 |
| 1 | CMP-1: 2 Must; CMP-2: 1 Must | 3 | 9 | 18 | 57 |
| 2 | CMP-2: 2 Must; CMP-3: 1 Must | 3 | 9 | 27 | 48 |
| 3 | CMP-3: 3 Must | 3 | 9 | 36 | 39 |
| 4 | CMP-4: 3 Must | 3 | 9 | 45 | 30 |
| 5 | CMP-4: 1 Must; CMP-5: 2 Must | 3 | 9 | 54 | 21 |
| 6 | CMP-5: 2 Must; CMP-1: 1 Should | 3 | 9 | 63 | 12 |
| 7 | CMP-2, CMP-3, CMP-4: 1 Should each | 3 | 9 | 72 | 3 |
| 8 | CMP-5: 1 Should | 1 | 3 | 75 | 0 |

All 20 Must requirements, including the 3 already Done, complete by week 6 in this plan. Each Done Must story must include automation of its 10 required tasks. Stories become Done at sprint end in this simple plan; no partial credit is assumed.

## 6. Sprint delivery predictability

**Commitment completion = Points Done from the original Sprint Backlog ÷ Original committed points × 100.**

Example: the team originally selects 3 stories worth 9 points. Two finish (6 points) and one remains incomplete. **Completion = 6 ÷ 9 × 100 = 66.7%.** Actual velocity is 6 if no other stories became Done.

If an additional 3-point story is added and completed, actual velocity is 9, but original commitment completion remains 66.7%. Keep original commitment, added work and removed work separate. This percentage is not a substitute for assessing whether the Sprint Goal was achieved.

## 7. Spillover

**Spillover stories = Originally committed stories not Done at sprint end.**

**Spillover rate = Incomplete originally committed points ÷ Original committed points × 100.**

For 3 committed stories (9 points), with 2 Done and 1 unfinished, spillover is **1 story / 3 points**, and **3 ÷ 9 × 100 = 33.3%**.

Your 3 completed spillover stories have **zero remaining points**. Their earlier sprint spillover rate cannot be calculated without that sprint's original committed scope. Review why they carried over: oversized work, unclear requirements, review queues, dependencies or missing automation.

## 8. Sprint Goal success

**Sprint Goal success rate = Sprints achieving their agreed goal ÷ Sprints reviewed × 100.**

If 3 of 4 sprint goals were achieved, **3 ÷ 4 × 100 = 75%**. This is an illustrative example; your actual goal history is not supplied. Assess the goal outcome in the Sprint Review even when some optional backlog items remain incomplete.

## 9. Burndown and burnup

**Release burndown = Total remaining release points at each checkpoint.** Start at 66 points after the completed stories. The conservative planned sequence is **66, 57, 48, 39, 30, 21, 12, 3, 0**.

**Release burnup = Cumulative Done points versus total scope.** The planned Done sequence is **9, 18, 27, 36, 45, 54, 63, 72, 75**, against scope of 75 points. Show the scope line separately so new requirements are visible.

Example: after week 2, 27 points are Done. If 2 new 3-point FRs enter scope, total scope becomes **75 + 6 = 81** and remaining work becomes **81 − 27 = 54**, not 48. At velocity 10, remaining forecast becomes **54 ÷ 10 → 6 sprints**. With a 3-story weekly limit, 18 remaining stories need **6 weeks**.

For a 9-point sprint over 5 working days, an ideal daily line drops **9 ÷ 5 = 1.8 points/day**. Actual story-point burndown may be step-shaped because points burn only when stories become Done. Track task progress separately without inflating story velocity.

## 10. Flow: cycle time, aging and blocked work

**Cycle time = Done timestamp − Started timestamp**, using a consistent calendar- or working-day convention. A story started Monday and finished Thursday has 3 elapsed calendar days if timestamps are at the same time of day.

**Work-item age = Today/reporting timestamp − Started timestamp** for unfinished work. Investigate aging stories instead of waiting until sprint end.

**Blocked time rate = Blocked elapsed working time ÷ Total elapsed working cycle time × 100.** A story spends 1 blocked working day in a 4-working-day cycle: **1 ÷ 4 × 100 = 25%**. This measures delay, not team person-hours.

Actual timestamps were not provided, so these metrics cannot yet be calculated for ETS 2702. Track story ID, component epic, start, blocked/unblocked events and Done date. Use these to investigate dependency queues and review bottlenecks.

## 11. Team availability and capacity

Five members do not guarantee the same capacity every week. Use person-days to understand availability; story points are not hours.

Assuming a 5-working-day sprint, gross availability is **5 members × 5 days = 25 person-days**. If there are 5 person-days of leave, availability is **20 person-days**, or **20 ÷ 25 × 100 = 80%**.

A rough planning adjustment is **10 historical points × 80% = 8 points** for that sprint. With 3-point stories and an 8-point planning limit, select at most **2 stories / 6 points**. This is an approximation, not a reliable linear productivity law; skill coverage and dependencies matter. Count meetings, support and leave consistently with the historical velocity baseline.

## 12. Must automation as a Definition of Done measure

**Must automation coverage = Fully automated Must FRs ÷ All 20 Must FRs × 100.**

At this planning baseline, the 3 Done Must stories imply **3 fully automated Must FRs / 20 = 15%**, and **30 / 200 = 15%** of mandatory automation tasks are complete. This assumes the Done label includes mandatory automation; it is not an observation from the earlier test snapshot.

At the end of week 6, the plan requires **20 / 20 = 100%** Must requirement automation and **200 / 200 = 100%** mandatory automation-task completion. If a story passes manual testing but mandatory automation remains incomplete, it is not Done under this agreed rule and does not contribute velocity.

## 13. Forecast sensitivity

The following are scenarios, not statistical confidence intervals. Actual history is needed for a probabilistic forecast.

| Team velocity, points/week | Must: point forecast (51 points) | Full: point forecast (66 points) | Whole stories/week under that planning limit | Must: whole-story plan (17 stories) | Full: whole-story plan (22 stories) |
|---|---:|---:|---:|---:|---:|
| 7 | 8 weeks | 10 weeks | 2 | 9 weeks | 11 weeks |
| 10 | 6 weeks | 7 weeks | 3 | 6 weeks | 8 weeks |
| 13 | 4 weeks | 6 weeks | 4 | 5 weeks | 6 weeks |

**Point forecast = Round remaining points ÷ Scenario velocity upward.**

**Whole-story plan = Round remaining stories ÷ floor(Scenario velocity ÷ 3) upward.**

If a target deadline allows only 5 weeks, Must delivery needs **51 ÷ 5 = 10.2 average points/week** and full delivery needs **66 ÷ 5 = 13.2 average points/week**. A uniform whole-story weekly limit would require 4 stories / 12 points for Must and 5 stories / 15 points for full scope. These are required rates, not a promise that the team can achieve them.

## If the completed stories are not all Must

Full remaining scope stays **66 points / 22 stories**. The Must forecast changes with the classification of the completed stories.

| Completed Must stories among the 3 Done | Remaining Must stories | Remaining Must points | Point forecast at 10 | Whole-story plan at 3/week |
|---|---:|---:|---:|---:|
| 3 | 17 | 51 | 6 weeks | 6 weeks |
| 2 | 18 | 54 | 6 weeks | 6 weeks |
| 1 | 19 | 57 | 6 weeks | 7 weeks |
| 0 | 20 | 60 | 6 weeks | 7 weeks |

## Weekly Scrum Master review

| Review item | Current planning baseline | Weekly action |
|---|---|---|
| Release scope / remaining points | 75 total / 66 remaining | Update Done and scope changes |
| Must scope / remaining points | 60 total / 51 remaining | Review priority and automation completeness |
| Actual velocity | Supplied reference is 10 | Record actual Done points once |
| Throughput | Conservative plan is 3 stories/week | Compare with actual Done stories |
| Commitment completion and spillover | Current sprint commitment not supplied | Capture original commitment and end outcome |
| Sprint Goal outcome | Not supplied | Assess the agreed goal in Review |
| Aging and blockers | Timestamps not supplied | Remove dependencies and queue delays |
| Team availability | 5-member team | Account for leave, support and skill coverage |
| Forecast | Must 6 weeks; full 7-point forecast / 8-week conservative plan | Reforecast from remaining work and observed delivery |

Use these metrics to improve planning and flow, rather than to pressure members to produce points. The forecast assumes stable scope, comparable estimates and no additional unestimated release work.
