# Engagement margin review: an invented example

*Illustrative example with invented data.* The firm, the client, the suppliers, the roles' cost rates and every figure below are invented. Firm A is an invented 30-person advisory firm. It is mid-way through an operating-model review for Client B, a fixed-fee engagement billed on milestones. The finance analyst prepares the review for the engagement partner and the finance lead. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The worksheet follows.

## The inputs

### 1. Settings

```
Engagement: Operating-model review for Client B
Stage: mid-way, as of Friday 30 October 2026
Fee basis: fixed fee of $100,000, billed on milestones agreed with Client B
Agreed engagement fee: 100,000
For: engagement partner and finance lead, review on Thursday 5 November 2026
Prepared by: finance analyst, on Monday 2 November 2026
Cost limit: 45% of a workstream's agreed fee
```

### 2. Fee schedule

```
Workstream | Budget hours | Agreed fee
Assessment | 120 | 30,000
Design | 200 | 50,000
Rollout support | 80 | 20,000
```

### 3. Time export, as of 30 October 2026

```
Workstream | Role | Hours | Status
Assessment | Partner | 10 | Approved
Assessment | Manager | 40 | Approved
Assessment | Consultant | 80 | Approved
Assessment | Analyst | 12 | Approved
Design | Partner | 14 | Approved
Design | Manager | 46 | Approved
Design | Consultant | 70 | Approved
Design | Analyst | 20 | Approved
Design | Consultant | 16 | Submitted
Rollout support | Manager | 8 | Approved
Rollout support | Consultant | 10 | Approved
Workshops | Consultant | 8 | Approved
```

### 4. Cost rates, supplied by the finance lead

```
Role | Cost rate
Partner | 150
Manager | 95
Consultant | 60
```

### 5. Billing list, as of 30 October 2026

```
Invoice | Workstream | Type | Amount
INV-1 | Assessment | Fee | 30,000
INV-2 | Design | Fee | 15,000
INV-3 | Design | Recharge | 960
```

### 6. Delivery costs, as of 30 October 2026

```
Item | Workstream | Kind | Amount | Status
Survey platform licence | Assessment | Expense | 1,400 | Invoiced
Data extract, Supplier A | Assessment | Subcontractor | 3,000 | Invoiced
Facilitation, Supplier B, first invoice | Design | Subcontractor | 6,000 | Invoiced
Travel | Design | Expense | 960 | Invoiced
Facilitation, Supplier B, second invoice | Design | Subcontractor | 4,500 | Not yet invoiced
Rollout delivery, Supplier C | Rollout support | Subcontractor | | Not yet invoiced
```

### 7. Remaining hours, from the engagement manager's note of Thursday 29 October 2026

```
Workstream | Remaining hours
Assessment | 10
Design | 80
Rollout support | 60
```

## The worksheet

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
