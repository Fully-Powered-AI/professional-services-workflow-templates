# Engagement margin review: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (`claude-sonnet-5-5`)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (the seven input blocks: settings, fee schedule, time export, cost rates, billing list, delivery costs and remaining hours). No client data was used. The template's fenced instruction block and output format were followed as written. This is the third run of the day. An independent review of the second run raised minor points. The ones that touch what a run produces were wording changes: the picture line now reads "so on the costs side the full figure is this or lower", and the hours line reads "not approved [n]" in place of "submitted, not approved [n]". The instruction block was only re-wrapped, and a rule in the output format now says "if any gap touches its cost". This record replaces the second run's record. Its figures were re-derived from the inputs, not copied; the only differences from the second run's output are those two phrases, and the questions are now given in full. The first run found the Workshops conflict and the points listed under the earlier ambiguities below; they are now settled in the template.

One limit on this record. The run was done by the same session that made those edits, not by an assistant that had not seen the template, and the example file holds the inputs and the worked output together, so the published output was known before the worksheet below was produced. The arithmetic was redone from the inputs line by line, but this is not a blind run. A reader should weigh the close match with the example accordingly.

## What came out

The run reached the end and returned a full draft. It stopped for nothing: every header matched, there was one currency and one engagement, the fee lines added to $100,000, and no row fell under a stop condition. All sections of the output format were produced. The worksheet follows in full, questions included.

```
ENGAGEMENT MARGIN REVIEW: Operating-model review for Client B, mid-way at 30 October 2026

For: the engagement partner and the finance lead, review on Thursday 5 November 2026. Prepared by the finance analyst on Monday 2 November 2026.
Sources: time export, as of 30 October 2026, 12 rows; fee schedule, 3 workstreams; billing list, as of 30 October 2026, 3 invoices; delivery costs, as of 30 October 2026, 6 items; cost rates for 3 roles, from the finance lead; remaining hours from the engagement manager, note of 29 October 2026.
Settings used: fixed fee, billed on milestones; cost limit 45% of a workstream's agreed fee. Defaults used: hours test 10%; effort-ahead-of-billing gap 25 points.

THE PICTURE
Agreed fee: $100,000. Fees billed: $45,000 (45.0%). Unbilled fee: $55,000.
Hours: budget 400; approved 318 (310 on scheduled workstreams, 77.5% of budget); not approved 16; expected still to come 150 (not supplied for: Workshops); projected 460 on scheduled workstreams (15.0% over budget). 8 approved hours on a workstream not in the fee schedule are in neither percentage.
Cost: time at the firm's rates $22,610 for 286 of 318 hours (32 hours have no rate); direct costs invoiced $11,360; direct costs not yet invoiced $4,500 stated (1 with no amount); recharged to the client $960.
Fee less supplied costs so far: $62,490. This is not a margin: the gaps below are not in it, so on the costs side the full figure is this or lower.
Workstreams: 4 (3 scheduled, 1 not in the fee schedule). Flagged: 2 workstreams with at least one fired test. Gaps: 5 numbered items.

TIE-OUT
Fee lines add to the agreed fee: $30,000 + $50,000 + $20,000 = $100,000.
Hours: approved hours by workstream add to the export's approved rows: 142 + 150 + 18 + 8 = 318. Not approved: 16. Export total 334, computed from the rows, not checked against a report.
Billing: fees billed by workstream add to the fee invoices: $30,000 + $15,000 + $0 + $0 = $45,000. Recharges: $960.
Costs: invoiced by workstream add to the list: $4,400 + $6,960 + $0 + $0 = $11,360. Not yet invoiced: $0 + $4,500 + amount not supplied + $0 = $4,500.
Results: workstream results add to the engagement: $15,500 + $28,830 + $18,640 - $480 = $62,490.

WORKSTREAMS
Assessment. Fee $30,000; billed $30,000 (100.0%); unbilled $0.
Hours: budget 120; approved 142 (118.3%); not approved 0; expected still to come 10; projected 152 (26.7% over).
Cost: time $10,100 (12 hours without a rate); direct costs invoiced $4,400; not yet invoiced $0; recharged $0. Supplied cost $14,500, at least (48.3% of the agreed fee).
Fee less supplied costs so far: $15,500, incomplete (12 Analyst hours have no rate).
Tests: Hours over budget: fired (26.7% over; test 10%). Effort ahead of billing: not fired (18.3 points; test 25). Cost limit: fired (48.3%; limit 45%; the cost is at least this).

Design. Fee $50,000; billed $15,000 (30.0%); unbilled $35,000.
Hours: budget 200; approved 150 (75.0%); not approved 16; expected still to come 80; projected 230 (15.0% over).
Cost: time $10,670 (20 hours without a rate); direct costs invoiced $6,960; not yet invoiced $4,500; recharged $960. Supplied cost $21,170, at least (42.3% of the agreed fee).
Fee less supplied costs so far: $28,830, incomplete (20 Analyst hours have no rate).
Tests: Hours over budget: fired (15.0% over; test 10%). Effort ahead of billing: fired (45.0 points; test 25). Cost limit: not fired (42.3%; limit 45%), on the costs supplied only.

Rollout support. Fee $20,000; billed $0 (0.0%); unbilled $20,000.
Hours: budget 80; approved 18 (22.5%); not approved 0; expected still to come 60; projected 78 (2.5% under).
Cost: time $1,360 (all hours rated); direct costs invoiced $0; not yet invoiced: amount not supplied (Supplier C); recharged $0. Supplied cost $1,360, at least (6.8% of the agreed fee).
Fee less supplied costs so far: $18,640, incomplete (Supplier C amount not supplied).
Tests: Hours over budget: not fired (2.5% under; test 10%). Effort ahead of billing: not fired (22.5 points; test 25). Cost limit: not fired (6.8%; limit 45%), on the costs supplied only.

Workshops (not in the fee schedule). Fee none; billed $0 (no fee); unbilled none.
Hours: no budget; approved 8; not approved 0; expected still to come not supplied; projected not stated.
Cost: time $480 (all hours rated); direct costs invoiced $0; not yet invoiced $0; recharged $0. Supplied cost $480 (no fee).
Fee less supplied costs so far: -$480, incomplete (not in the fee schedule; remaining hours not supplied).
Tests: not run (no budget and no fee).

GAPS THAT LIMIT THE VIEW
1. Hours not approved: Design, 16 hours, status Submitted. If approved, recorded 166 and projected 246 (23.0% over). Not in any figure above.
2. No cost rate: Analyst, 32 hours (Assessment 12, Design 20). Not in any cost above.
3. Costs not yet invoiced: Design, Supplier B second invoice, $4,500 stated and included. Rollout support, Supplier C, amount not supplied and not included.
4. Not in the fee schedule: Workshops, 8 hours, $480 of time, no fee.
5. Remaining hours not supplied: Workshops.

QUESTIONS FOR THE TEAM
1. Engagement manager. Assessment: 142 approved hours against a budget of 120, with 10 more expected (152, 26.7% over), and the fee is fully billed. Did any of the extra hours come from work outside the agreed scope, and if so what was agreed with Client B about it?
2. Engagement manager. Assessment: supplied cost is at least $14,500, 48.3% of the $30,000 fee, above the 45% limit. Were the survey platform licence ($1,400) and the data extract from Supplier A ($3,000) in the plan the fee was set on?
3. Engagement manager. Design: 75.0% of the budget hours are used and 30.0% of the fee is billed, 45.0 points apart. Which agreed milestone has Design reached, and when will the next invoice be raised?
4. Engagement manager. Design: 80 hours are expected against 50 left in the budget (projected 230, 15.0% over). What drives the extra 30 hours?
5. Engagement manager. Design: 16 hours are Submitted and not approved. When will they be approved or returned?
6. Engagement manager. Design: Supplier B's second invoice is stated at $4,500 and not yet invoiced. Is that amount still current, and when is the invoice due?
7. Engagement manager. Rollout support: no amount was supplied for Supplier C. What has been quoted or agreed, and when will it be invoiced?
8. Engagement manager. Workshops: 8 hours are recorded to a workstream that is not in the fee schedule. Do they belong to a scheduled workstream under another name, or to additional work agreed with Client B?
9. Engagement manager. Workshops: remaining hours were not supplied for this workstream, which has 8 approved hours. How many hours remain, and when will the note be updated?
10. Finance lead. Analyst: no cost rate was supplied for 32 hours (Assessment 12, Design 20). What is the rate, or should those hours stay out of the cost view?

DECISIONS FOR THE ENGAGEMENT PARTNER AND THE FINANCE LEAD
1. Staffing. Projected hours are 152 against 120 for Assessment, 230 against 200 for Design and 78 against 80 for Rollout support; 150 hours are expected still to come. Whether to change who does the remaining work, once questions 1 and 4 are answered.
2. Fee action. Assessment is fully billed at $30,000 with projected hours 26.7% over; Design is 15.0% over with $35,000 unbilled. Whether to take any action on Client B's fee or scope, once questions 1, 4 and 8 are answered.
3. Billing. Design has 30.0% of its fee billed with 75.0% of its budget hours used. Whether the next Design invoice is due, once question 3 is answered.

Draft for the engagement partner's and the finance lead's review. Every figure comes from the files listed above and is for the two of them to validate. No fee has been set, nothing has been written off, no cost rate has been invented, no record has been changed and nothing has been sent.
```

## What was observed

Every required part of the output format was produced, and every tie-out balanced. The figures agree with the published example in every place. Three of the four workstreams were as the template expects. The three things the first run had to guess are now settled and were followed: the engagement projection counts scheduled workstreams only (460 against a budget of 400, with Workshops' 8 hours stated on their own), Workshops is called incomplete because the fee schedule and the missing remaining hours touch it, and the cost test carries "on the costs supplied only" when it is not fired and a gap touches the cost. The assistant declined nothing and had nothing to decline, because the run contained no request to estimate a rate, recommend an action or send the worksheet; those refusals were not exercised. Nor were the new recharge rule (no recharge exceeded its workstream's direct costs) or the exact-boundary rule.

No fact appears in the run's output that is not in the inputs. The one thing the example adds is the description "Firm A ... 30-person advisory firm" in its introduction, which is context and not in the inputs; it does not enter the worksheet.

Where the template was still ambiguous or the assistant had to guess:

1. **The cost limit is never tested for the whole engagement,** only for workstreams. The template's wording says so and it was clear enough.
2. **"Expected still to come ... (not supplied for: workstreams)"** and the workstream line "expected still to come [n / not supplied]" are two forms for the same fact; the run kept each as given.
3. **A gap item can cover several rows,** so a different reading of "numbered items" would count the gaps differently; the format now says numbered items and the run counted 5.

The template's acceptance tests still say none has been run. This trial ran one acceptance-style case (the ordinary mid-way review with gaps), not the fifteen tests. Nothing here is a test in a client environment.
