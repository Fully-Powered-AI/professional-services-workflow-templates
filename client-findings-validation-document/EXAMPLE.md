# Client findings validation document: an invented example

*Illustrative example with invented data.* The firm, the client, the people, the evidence and every figure below are invented. Firm A is an invented advisory firm. Client B is an invented regional distributor of garden machinery parts with about 140 staff, and Firm A has been reviewing why orders leave its main warehouse late. First come the inputs the engagement lead supplied, in full, then the document the capability returned.

## The inputs

### 1. Decision brief

```
Engagement: Order-to-dispatch review for Client B
Document goes to: Operations director, Client B. From: Engagement lead, Firm A.
Today: 17 November 2026. Reply by: 27 November 2026.
Decisions the client has to make:
  D1  Whether to trial zone-sorted pick lists at the main warehouse. Decides: Operations director.
  D2  Whether to trial a 16:00 same-day cut-off. Decides: Operations director.
  D3  Whether to add a second returns bench. Decides: Operations director.
```

### 2. Evidence register

```
ref,source,kind,date,from_whom,what_it_says,limits,share
E1,Interview 1,interview,2026-10-12,Warehouse supervisor,"Pick lists come out sorted by order number. On mixed orders pickers walk to aisle C, then aisle F, then back to aisle C.",One person's account.,yes
E2,Interview 2,interview,2026-10-13,Picker (morning shift),Confirmed the order-number sorting and the walk back to the first aisle.,One person's account.,no
E3,Interview 3,interview,2026-10-14,Customer service lead,Said late-order calls come mainly from customers who ordered parts from more than one zone.,One person's account; no call log seen.,yes
E4,Dispatch export,data,2026-10-30,Client warehouse system extract,"September 2026: 2,310 orders. 1,184 had lines in more than one zone, median 31 hours from order to dispatch. 1,126 had lines in one zone, median 19 hours.",One month; timestamps as recorded by the system.,yes
E5,Floor timing,observation,2026-10-15,Firm A consultant,"Timed 12 mixed-zone orders and 12 single-zone orders at the morning pick. Mean walking time 9 minutes for mixed, 4 minutes for single.",One morning.,yes
E6,Interview 4,interview,2026-10-14,Dispatch lead,"Once an order is picked, packing takes under 30 minutes, so an order placed by 16:00 could make the 16:30 courier.",One person's account.,yes
E7,Dispatch export,data,2026-10-30,Client warehouse system extract,"September 2026: 412 orders placed between 14:00 and 16:00. 97 dispatched the same day, 315 the next working day.",One month.,yes
E8,Interview 5,interview,2026-10-15,Picker (afternoon shift),"Said the afternoon pick team stops at 15:30, so later orders wait for the next day whatever the cut-off.",One person's account.,yes
E9,Returns log,document,2026-10-28,Client returns clerk,September 2026 returns log lists 188 returned items.,Counts only items logged at the bench.,yes
```

### 3. Candidate findings

```
finding_id,finding,evidence_refs,counter_refs,assumptions,proposed_implication,material,decision
F1,"Orders with lines in more than one zone take longer to dispatch, and the pick-list sort order is a likely cause.",E1;E2;E4;E5,,September is typical of other months.,Sort pick lists by zone at release and trial it at the main warehouse for four weeks.,yes,D1
F2,Most late-order calls come from customers with mixed-zone orders.,E3,,,Prioritise delay messages for mixed-zone orders.,yes,
F3,"Orders placed between 14:00 and 16:00 could ship the same day if the cut-off moved to 16:00.",E6;E7,E8,The 16:30 courier collection stays as it is.,Trial a 16:00 cut-off for two weeks.,yes,D2
F4,The returns queue at the single bench is longest on Mondays.,E10,,,Add a second returns bench on Mondays.,yes,D3
F5,Pallet wrap use is higher on mixed-zone orders.,E5,,,None.,no,
```

## The output

```
CLIENT FINDINGS VALIDATION DOCUMENT: Order-to-dispatch review for Client B

PART A. FOR THE CLIENT

For: Operations director, Client B. From: Engagement lead, Firm A. Prepared 17 November 2026. Please reply by 27 November 2026.
What this is: 3 findings from the research on Order-to-dispatch review for Client B, each with the evidence under it, what is assumed and the implication we propose. For each, please say whether you confirm it, want to correct it, or want to defer it. A deferred finding is not agreement, and work that depends on it waits.

Finding F1: Orders with lines in more than one zone take longer to dispatch, and the pick-list sort order is a likely cause.
Evidence behind it: 4 items, 3 kinds; 1 not shown, marked not to be shared.
E1 · interview · 12 October 2026 · Warehouse supervisor: Pick lists come out sorted by order number. On mixed orders pickers walk to aisle C, then aisle F, then back to aisle C. Limits: One person's account.
E4 · data · 30 October 2026 · Client warehouse system extract: September 2026: 2,310 orders. 1,184 had lines in more than one zone, median 31 hours from order to dispatch. 1,126 had lines in one zone, median 19 hours. Limits: One month; timestamps as recorded by the system.
E5 · observation · 15 October 2026 · Firm A consultant: Timed 12 mixed-zone orders and 12 single-zone orders at the morning pick. Mean walking time 9 minutes for mixed, 4 minutes for single. Limits: One morning.
Evidence pointing the other way: none supplied
Not yet shown: September is typical of other months.
Implication we propose: Sort pick lists by zone at release and trial it at the main warehouse for four weeks. This bears on D1, whether to trial zone-sorted pick lists at the main warehouse.
Your response: [ ] Confirm   [ ] Correct: what is wrong or missing: ______   [ ] Defer: what you need, and by when: ______

Finding F2: Most late-order calls come from customers with mixed-zone orders.
Evidence behind it: 1 item, 1 kind; single source.
E3 · interview · 14 October 2026 · Customer service lead: Said late-order calls come mainly from customers who ordered parts from more than one zone. Limits: One person's account; no call log seen.
Evidence pointing the other way: none supplied
Not yet shown: none stated
Implication we propose: Prioritise delay messages for mixed-zone orders. No decision named.
Your response: [ ] Confirm   [ ] Correct: what is wrong or missing: ______   [ ] Defer: what you need, and by when: ______

Finding F3: Orders placed between 14:00 and 16:00 could ship the same day if the cut-off moved to 16:00.
Evidence behind it: 2 items, 2 kinds.
E6 · interview · 14 October 2026 · Dispatch lead: Once an order is picked, packing takes under 30 minutes, so an order placed by 16:00 could make the 16:30 courier. Limits: One person's account.
E7 · data · 30 October 2026 · Client warehouse system extract: September 2026: 412 orders placed between 14:00 and 16:00. 97 dispatched the same day, 315 the next working day. Limits: One month.
Evidence pointing the other way: E8 · interview · 15 October 2026 · Picker (afternoon shift): Said the afternoon pick team stops at 15:30, so later orders wait for the next day whatever the cut-off. Limits: One person's account.
Not yet shown: The 16:30 courier collection stays as it is.
Implication we propose: Trial a 16:00 cut-off for two weeks. This bears on D2, whether to trial a 16:00 same-day cut-off.
Your response: [ ] Confirm   [ ] Correct: what is wrong or missing: ______   [ ] Defer: what you need, and by when: ______

This document is a draft for the engagement lead to verify. Nothing has been sent.

PART B. FOR THE ENGAGEMENT LEAD ONLY. REMOVE BEFORE SENDING.

Findings supplied: 5. Put to the client: 3. Held back: 1. Not material: 1. Flagged: 5.
Register: 9 items. Prepared 17 November 2026 from decision brief, register, findings.
Flags:
F1: evidence withheld (E2).
F2: single source; wording stronger than the evidence (the finding says "Most"; one counted interview, no counted data item).
F3: counter-evidence present (E8).
F4: reference not in register (E10); held back, no evidence.
F5: item does not address the finding (E5 gives walking times and says nothing about pallet wrap).
Withheld from the client copy: E2, used by F1.
Items that do not address the finding they are cited for: E5, cited by F5.
Figures checked: E4: 1,184 + 1,126 = 2,310, matches. E7: 97 + 315 = 412, matches. No other item gives a total.
Evidence no finding uses: E9.
Not put to the client: F4 (held back, reference not in register); F5 (marked not material).

Decisions for the engagement lead before sending: 5
1. F1, evidence withheld. E2 is marked not to be shared and is not shown, so F1 goes to the client with 3 of its 4 items visible. Does F1 go as it stands?
2. F2, single source and wording. The finding says "Most" and rests on one interview, E3, with no call log seen. Do you reword F2, add evidence, or leave it out of the client list?
3. F3, counter-evidence present. E8 is shown beside E6 and E7, and one assumption about the courier is listed as not yet shown. Does F3 go with both sides shown?
4. F4, reference not in register. It cites E10, which is not in the register. E9, the returns log, is the only item on returns, says nothing about Mondays, and no finding cites it. Which reference is meant, if any?
5. F5, not material, and no cited item addresses it. Does F5 stay out, or is there evidence to add?

PART C. CLIENT REPLIES

Not run: no replies supplied.
May be carried into the recommendations: none
Lead to revisit before use: none
Held: none
Not put to the client: F4, F5
The assistant has changed no finding and no record. Nothing has been sent.
```
