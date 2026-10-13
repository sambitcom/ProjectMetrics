# ETS 2702: Solution-Level Project and Delivery Metrics

## 1. Release model and assumptions

This guide uses **5 parallel solution teams**, rather than the single shared team in the earlier Scrum Master forecast. Each solution team owns one solution epic linked to one component epic. The solution and component levels share story IDs: they describe the same release scope, rather than two separate sets of stories.

| Item | Per solution team | ETS 2702 total |
|---|---:|---:|
| Solution epics | 1 | 5 |
| Linked component epics | 1 | 5 |
| Team members | 5 | 25 |
| Weekly team velocity | 10 points | 50 points of nominal aggregate velocity |
| User stories / linked FRs | 5 | 25 |
| Points per FR / story | 3 | Same estimation assumption |
| Full scope | 15 points | 75 points |
| Must requirements | 4 | 20 |
| Must scope | 12 points | 60 points |
| Should requirements | 1 | 5 |
| Testable tasks | 50 | 250 |
| Must verification and automation tasks | 40 | 200 |
| Sprint length | 1 week | Teams use aligned weekly sprints |

Exactly 4 Must and 1 Should FR are used per epic; your minimum allows the fifth FR to become Must. One FR maps to one story in this example. The 10 testable tasks are included in the 3-point story estimate, not added as extra stories or points.

**Completed spillover assumption:** 3 stories are already Done across the release, not per team. They are Must stories, with one completed in Team 1, one in Team 2 and one in Team 3. Team 4 and Team 5 have none completed. This distribution is illustrative; update the actual teams and priorities.

**Done includes the release's agreed story criteria:** implementation, required verification and automation of every Must requirement. If velocity 10 measures development alone, testing, automation and release work must be estimated separately before predicting readiness.

Each team's original scope is equal at 15 points. Remaining work differs because of completed spillover. Do not add the previous guide's sample test outcomes to this new planning snapshot.

## 2. Baseline across solution teams

| Solution team / epic | Linked component | Full points | Done stories | Done points | Remaining full points | Remaining Must points |
|---|---|---:|---:|---:|---:|---:|
| Team 1 / SOL-1 | CMP-1 | 15 | 1 | 3 | 12 | 9 |
| Team 2 / SOL-2 | CMP-2 | 15 | 1 | 3 | 12 | 9 |
| Team 3 / SOL-3 | CMP-3 | 15 | 1 | 3 | 12 | 9 |
| Team 4 / SOL-4 | CMP-4 | 15 | 0 | 0 | 15 | 12 |
| Team 5 / SOL-5 | CMP-5 | 15 | 0 | 0 | 15 | 12 |
| Release | 5 components | 75 | 3 | 9 | 66 | 51 |

## 3. Delivery progress by solution epic

**Epic completion = Done points in that epic ÷ Total points in that epic × 100.**

SOL-1 completion = **3 ÷ 15 × 100 = 20%**. SOL-4 completion is **0 ÷ 15 = 0%**.

**Release completion = Total unique Done points ÷ Total unique release points × 100 = 9 ÷ 75 × 100 = 12%.**

**Must completion = Done Must points ÷ Total Must scope × 100 = 9 ÷ 60 × 100 = 15%.**

Do not count a story once under its solution epic and again under its component epic. Track the same ID through both views. Component task completion can show progress without making a story Done.

## 4. Team velocity and aggregate delivery pace

**Actual team velocity = Points of stories becoming Done in that team's sprint.**

**Aggregate actual velocity = Sum of actual Done points from the 5 teams in the same week.**

The nominal aggregate velocity is **5 × 10 = 50 points/week**. This is a planning reference, not a promise that all remaining work can move freely between teams. Shared specialists, environments and dependencies can reduce parallel delivery.

Use aggregate story points only if the teams have a reasonably comparable estimation basis. Otherwise forecast each team in its own point scale and combine finish times. In this example, equal 3-point FR estimates and equal velocity are explicit assumptions.

**Throughput per team = Stories Done per week.** Under a firm 10-point weekly planning limit, each team fits **floor(10 ÷ 3) = 3 stories / 9 points**. Across 5 teams that is up to 15 whole stories/week, but only if enough work is available and ready in each team.

## 5. Release prediction: forecast each team first

**Team point forecast = Round remaining team points ÷ Team velocity upward to a whole sprint.**

**Release team-work forecast = Latest finish among the teams required for release.**

| Team | Must points remaining | Must forecast at 10 | Full points remaining | Full forecast at 10 |
|---|---:|---:|---:|---:|
| Team 1 | 9 | 1 week | 12 | 2 weeks |
| Team 2 | 9 | 1 week | 12 | 2 weeks |
| Team 3 | 9 | 1 week | 12 | 2 weeks |
| Team 4 | 12 | 2 weeks | 15 | 2 weeks |
| Team 5 | 12 | 2 weeks | 15 | 2 weeks |

**ETS 2702 Must team-work milestone = max(1, 1, 1, 2, 2) = 2 weeks.**

**ETS 2702 full team-work milestone = max(2, 2, 2, 2, 2) = 2 weeks.**

The whole-story plan also gives 2 weeks: Team 1 has 4 remaining stories, needing **round 4 ÷ 3 upward = 2 weeks**; Team 4 has 5, needing **round 5 ÷ 3 upward = 2 weeks**.

The aggregate calculation **66 ÷ 50 = 1.32 → 2 weeks** agrees here, but use it only as a cross-check. In an imbalanced release, one team's finish time can be later than the pooled estimate. For example, if only Team 5 has 30 points left, dividing by all teams' velocity predicts 1 week, while Team 5 at 10 needs 3 weeks unless work can actually be redistributed.

These are weeks from the next planning point. No start date or target deadline was supplied.

## 6. A two-week parallel plan

Prioritize Must scope before Should work. The teams select Sprint Goals that respect their dependencies.

| Team | Already Done Must | Week 1 | Week 2 | Total remaining work delivered |
|---|---:|---|---|---:|
| Team 1 | 1 | 3 Must stories, 9 points | 1 Should story, 3 points | 12 points |
| Team 2 | 1 | 3 Must stories, 9 points | 1 Should story, 3 points | 12 points |
| Team 3 | 1 | 3 Must stories, 9 points | 1 Should story, 3 points | 12 points |
| Team 4 | 0 | 3 Must stories, 9 points | 1 Must + 1 Should, 6 points | 15 points |
| Team 5 | 0 | 3 Must stories, 9 points | 1 Must + 1 Should, 6 points | 15 points |
| Release | 3 | 15 stories, 45 points | 7 stories, 21 points | 22 stories, 66 points |

After week 1, cumulative release Done is **9 + 45 = 54 points**, or **54 ÷ 75 = 72%**. Remaining full scope is **21 points**. Must Done is **18 of 20 requirements = 90%**. Team 4 and Team 5 each still have one Must FR to finish.

After week 2, all 75 release points and all 20 Must requirements are Done in this illustrative plan. Actual weekly Done points are **45 then 21**, rather than 50 then 50: finishing a finite backlog does not require using the nominal velocity each week.

## 7. Solution integration and release gates

Component completion alone does not establish solution readiness. For ETS 2702, track the cross-component workflows, integration environment, release candidate, performance/security acceptance, unresolved serious defects and deployment readiness.

**Solution acceptance coverage = Agreed solution scenarios with relevant tests ÷ Total agreed solution scenarios × 100.**

**Solution verified rate = Agreed solution scenarios whose required checks pass ÷ Total agreed solution scenarios × 100.**

Illustration: if 10 solution scenarios are agreed, 10 have tests and 8 pass, coverage is **100%** but verified rate is **80%**. These scenario counts are examples, not supplied ETS 2702 data and are not included in the 25-story baseline.

**Release-ready forecast = Latest required team/dependency/gate finish, including any remaining work after those prerequisites.**

If a 1-week final integration activity can start only after team work finishes in week 2, release readiness becomes **week 3**. If that activity is already included in story estimates and completed by week 2, no extra week should be added. Record actual remaining effort and dependencies before setting the date.

The workbook therefore shows a **2-week team-work milestone** and a separate editable number of sequential release-gate weeks. Its default is **unestimated**, not zero. A final release-ready forecast remains unavailable until that input is confirmed.

## 8. Dependency and critical-path metrics

**Open blocking dependencies = Count of unresolved dependencies preventing required work.**

Track predecessor, dependent story/team, owner, needed-by date and current expected completion. A shared environment blocking Team 4 cannot be solved by adding the other teams' velocities together.

**Dependency delay = Revised prerequisite finish − Baseline prerequisite finish.** A prerequisite moves from end of week 1 to end of week 2: **1 week of delay**. Reforecast downstream work based on when it can start; do not automatically add the same delay to every team.

**Critical path** is the dependency chain governing the earliest release-ready finish. In this parallel baseline, Team 4 and Team 5 govern Must completion. With integration or approval dependencies added, a different chain may become critical. Actual dependency data was not supplied.

## 9. Delivery predictability and spillover across teams

**Commitment completion = Done points from the original Sprint Backlog ÷ Originally committed points × 100.**

For a team committing 9 points and completing 6 from that original scope, predictability is **6 ÷ 9 × 100 = 66.7%**. If it completes another added 3-point story, velocity is 9, but original commitment completion stays 66.7%.

**Release-level commitment completion = Sum of original committed work completed across teams ÷ Sum of original committed points across teams × 100.** Calculate from totals, not an unweighted average when commitments differ.

Illustration: all 5 teams commit 9 points, giving 45. Four deliver their 9 points and one delivers 6. **Completion = 42 ÷ 45 × 100 = 93.3%.** The one unfinished 3-point story gives **spillover = 3 ÷ 45 × 100 = 6.7%**. Investigate its effect on Must delivery rather than relying on the overall percentage.

The 3 stories already Done at baseline are completed carryover. They are not remaining spillover. Credit them only in the sprint in which they became Done, and remove their points from remaining release scope once.

## 10. Burnup, burndown and scope change

**Release burnup:** unique cumulative Done points versus total scope. Baseline **9 / 75**, week 1 planned **54 / 75**, week 2 planned **75 / 75**.

**Release burndown:** remaining points. Planned sequence **66 → 21 → 0**.

**Scope change (%) = Net points added since baseline ÷ Original baseline points × 100.** If 2 new 3-point stories are accepted, **6 ÷ 75 × 100 = 8%** scope growth. Scope becomes 81. Assign those stories to teams and recalculate their finish times; dividing added points by 50 can hide a bottleneck.

Record additions/removals, MoSCoW priority, owner team, reason and approval. An unchanged 75-point scope line would hide the change.

## 11. Mandatory automation readiness

**Must automation coverage = Fully automated Must FRs ÷ Total Must FRs × 100.** A Must FR is complete only when all its 10 required tasks have usable automation and its required verification is Done.

At baseline, 3 completed Must FRs imply **3 ÷ 20 × 100 = 15%** requirement automation completion and **30 ÷ 200 × 100 = 15%** mandatory task completion, assuming the agreed Done rule.

The week 1 plan reaches **18 ÷ 20 = 90%**, or **180 of 200 Must tasks**. Week 2 reaches **100%**. A high overall test pass rate cannot compensate for missing Must automation. Keep automation completion and execution results as separate indicators.

## 12. Resource and capacity metrics

Total team members = **5 teams × 5 = 25**. With a 5-working-day week, gross availability is **25 × 5 = 125 person-days/week**. This working-day convention is an assumption; deduct actual leave and unavailable time.

**Availability rate = Available person-days ÷ Normal baseline person-days × 100.** A team with 5 person-days of leave has **20 ÷ 25 = 80%** availability. A rough planning adjustment is **10 × 80% = 8 points**, but point productivity is not necessarily linear with staffing.

Do not infer hours, cost or individual productivity from story points. Financial metrics require actual budget, rates and spend. Those inputs were not provided, so this guide does not invent a cost forecast.

## 13. Forecast sensitivity

These are planning scenarios, not statistical confidence intervals. Each team uses the same velocity in each scenario.

| Velocity per team | Nominal aggregate | Must team-work forecast | Full team-work forecast | Full whole-story plan |
|---|---:|---:|---:|---:|
| 7 points/week | 35 | 2 weeks | 3 weeks | 3 weeks |
| 10 points/week | 50 | 2 weeks | 2 weeks | 2 weeks |
| 13 points/week | 65 | 1 week | 2 weeks | 2 weeks |

At velocity 13, Team 4 can complete all 4 Must stories (12 points) in one sprint; its fifth Should story still makes full scope 15 points and requires another sprint under that limit. Aggregate capacity alone cannot remove this constraint.

Review actual per-team completion and impediments weekly. Refresh remaining scope and forecast from the team with the latest required finish. Add independently estimated integration/release gates.

## If you meant 3 completed stories per team

That is **15 completed stories / 45 points** across the release, rather than 3 / 9. If all are Must, each team has **2 stories / 6 points** remaining, including **1 Must / 3 points**. Both Must and full team-work scope could then finish in **1 more week** at velocity 10, before any extra release gates.

## Weekly delivery dashboard

| Metric | Baseline / planned forecast | Delivery Manager action |
|---|---|---|
| Release completion | 9 / 75 points = 12% | Keep unique scope and Done totals current |
| Must completion | 9 / 60 points = 15% | Protect mandatory priorities |
| Team forecasts | Must: 1, 1, 1, 2, 2 weeks | Focus on Team 4 and Team 5 dependencies |
| Full milestone | 2 weeks of team work | Confirm all necessary solution gates |
| Actual team velocity | Reference 10 per team | Compare actual Done with comparable history |
| Commitment and spillover | Current sprint actuals not supplied | Capture original scope and outcomes |
| Integration verified rate | Actual scenarios not supplied | Agree scenarios and measure solution behavior |
| Blocking dependencies | Actual dependency register not supplied | Assign owner and needed-by date |
| Scope growth | Baseline 75 points | Reforecast the owning team on changes |
| Must automation | Baseline 15%; target 100% | Enforce the agreed Done rule |
| Risks / serious defects | Actual register not supplied | Review impact, mitigation and disposition |

The Scrum Masters manage team flow, impediments, Sprint Goals and continuous improvement. The Project/Delivery Manager coordinates dependencies, scope, stakeholders and the solution release forecast. Together they validate a delivery plan rather than treating summed velocity as a guaranteed release date.
