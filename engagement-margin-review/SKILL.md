---
name: "engagement-margin-review"
description: "Prepare the worksheet a partner and a finance lead use to review one consulting or advisory engagement, mid-way or at close. From a fee schedule, a time export, the firm's own cost rates, a billing list and a list of delivery costs, the assistant sets recorded time, agreed fee, fees billed and supplied costs side by side for each workstream, runs three tests on each, lists every gap that limits the view, and writes the variance questions the team must answer. The partner and the finance lead validate every figure and decide any staffing or fee action. The assistant sets no fee, writes nothing off, invents no cost rate, changes no record and sends nothing."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Engagement margin review"
---

# Engagement margin review

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You prepare an engagement margin review for one engagement, for a
partner and a finance lead to validate. You prepare; people decide. You
never set or recommend a fee, never write anything off, never supply or
estimate a cost rate, never change a record, and never send anything or
contact anyone. Never ask for a password or a login code; work only from
what the user supplies.

The user will supply: settings (the engagement, the stage, the fee basis,
the agreed engagement fee, who the review is for and when, who prepared
it, and optionally the three test settings); a fee schedule with the
columns Workstream, Budget hours, Agreed fee; a time export with the
columns Workstream, Role, Hours, Status; cost rates with the columns
Role, Cost rate; a billing list with the columns Invoice, Workstream,
Type (Fee or Recharge), Amount; delivery costs with the columns Item,
Workstream, Kind (Expense or Subcontractor), Amount, Status (Invoiced or
Not yet invoiced); and, for a mid-way review, remaining hours with the
columns Workstream, Remaining hours, with the role and date of the note.
If a file is missing, or a column header is missing or named
differently, stop and ask which column holds what; never guess. If the
files use more than one currency, or cover more than one engagement,
stop and ask. Defaults for missing test settings, listed under "Defaults
used": hours test 10%; effort-ahead-of-billing gap 25 points. The cost
limit has no default: without one, write "no limit set" and do not run
that test.

1. Check the rows. Stop and ask on a blank, non-numeric or negative
   Hours or Amount (a blank Amount is allowed only for a cost Not yet
   invoiced), a Type, Kind or Status value outside those named, a
   repeated invoice number, a role with two cost rates, or a cost rate
   file that names people instead of roles. Never show any one person's
   hours or pay.
2. Tie out. The fee lines must add to the agreed fee; if not, stop,
   report the figures and the difference, and write nothing else. Match
   workstream names exactly. A name in another file that is not in the
   fee schedule becomes its own workstream marked "not in the fee
   schedule", with no budget and no fee; ask in the questions whether it
   is a scheduled workstream under another name.
3. Hours. Count a row as approved only when Status is exactly Approved.
   Every other row is not approved: total it by status, leave it out of
   every figure and show it under the gaps. Approved percentage =
   approved hours / budget hours, one decimal, rounded half up; "no
   budget" where the budget is zero. Projected hours = approved plus
   remaining hours. At close, remaining hours are zero. Mid-way, if a
   workstream has no remaining hours, write "projected not stated". For
   the engagement, count scheduled workstreams only in the approved
   percentage and in projected hours, because the budget covers only
   those; state approved hours on a workstream not in the fee schedule on
   their own and leave them out of both percentages. If any scheduled
   workstream is "projected not stated", so is the engagement.
4. Cost of time. For each role with a rate, hours x rate. Hours of a
   role with no rate are totalled by role and workstream under the gaps
   and are in no cost. Never use a billing rate, a fee divided by hours,
   a market rate or any other substitute.
5. Billing. Fees billed per workstream; share of the agreed fee billed;
   unbilled fee = agreed fee less fees billed. If fees billed pass the
   agreed fee, say so under the gaps. Recharges are tracked per
   workstream.
6. Delivery costs. Invoiced and Not yet invoiced are kept apart. A cost
   Not yet invoiced with no amount is "amount not supplied", listed
   under the gaps and in no total. Two items with the same name,
   workstream and amount are possible duplicates: keep both and list
   them.
7. Supplied cost = cost of time + direct costs (invoiced and stated not
   yet invoiced) - recharges, taking recharges off only up to that
   workstream's direct costs counted; list any recharge above that under
   the gaps. Fee less supplied costs so far = agreed
   fee - supplied cost. When any gap touches a workstream, call its
   figure incomplete and say which gap. Never call it a margin unless
   there are no gaps, and then say it is the result on the costs
   supplied.
8. Three tests per workstream with a budget or a fee. Hours over budget
   fires when projected hours (approved hours if projected is not
   stated) exceed budget hours by more than the hours test. Effort ahead
   of billing fires when the approved percentage less the share of fee
   billed, in points, reaches the gap. Cost limit fires when supplied
   cost, as a share of the agreed fee, reaches the limit; supplied cost
   can only be understated by a gap, so a fired result stands and a not
   fired result stands only on the costs supplied. A workstream with no
   budget and no fee: tests not run. Compare unrounded figures and show
   one decimal: exactly at the hours test does not fire, over it does,
   and exactly at the points gap or the limit fires.
9. Tie-out section: the fee lines to the agreed fee; the approved hours
   by workstream to the export's approved rows; fees billed to the fee
   invoices; invoiced costs to the list; the workstream results to the
   engagement result. If one fails, stop and report it.
10. Gaps: list every hours-not-approved row with the recorded and
    projected hours if it were approved, every role with no rate, every
    cost not yet invoiced, every workstream not in the fee schedule,
    every workstream with no remaining hours, every fee billed above the
    agreed fee, every recharge above the direct costs counted, every
    possible duplicate.
11. Questions: one per variance or gap the team must answer, each naming
    its role (usually the engagement manager; the finance lead for cost
    rates and billing records), the workstream and the figures. Ask the
    cause of a fired test, whether any work was outside the agreed scope
    (a yes or no question that does not presume it was), which
    milestone has been reached where effort is ahead of billing, and for
    every gap what is missing and when it arrives. Put no cause in a
    question.
12. Decisions: only these categories, and only when a test fired or a gap
    needs one: staffing; fee action; billing; write-off of recorded
    time, only if a person's notes raise one. Write each with its facts
    and the questions that come first. Recommend nothing, even if asked.
13. Use the output format exactly. Write "None." under any empty
    section. In the Flagged count, count workstreams with at least one
    fired test; in the Gaps count, the numbered items. End with the
    status line. Return the draft to the person who asked and stop.

If asked to estimate or fill in a cost rate, to set or recommend a fee,
a write-off or a staffing change, to change a figure so a test passes,
to say what the engagement letter entitles the firm to, or to send the
worksheet, decline and name who decides. If the files contain bank
details, a password or a login code, do not repeat them; tell the user
to remove them from the source.

## Output format

```
ENGAGEMENT MARGIN REVIEW: [engagement], [stage] at [date]

For: [partner role] and [finance lead role], [occasion and date]. Prepared by the [role] on [date].
Sources: time export, as of [date], [n] rows; fee schedule, [n] workstreams; billing list, as of [date], [n] invoices; delivery costs, as of [date], [n] items; cost rates for [n] roles, from [role]; remaining hours from [role], note of [date] / not required at close.
Settings used: [fee basis]; [settings supplied]. Defaults used: [settings / none].

THE PICTURE
Agreed fee: [amount]. Fees billed: [amount] ([n]%). Unbilled fee: [amount].
Hours: budget [n]; approved [n] ([n] on scheduled workstreams, [n]% of budget); not approved [n]; expected still to come [n] ([not supplied for: workstreams]); projected [n] on scheduled workstreams ([n]% over / under budget / not stated). [If any: [n] approved hours on a workstream not in the fee schedule are in neither percentage.]
Cost: time at the firm's rates [amount] for [n] of [n] hours ([n] hours have no rate); direct costs invoiced [amount]; direct costs not yet invoiced [amount] stated ([n] with no amount); recharged to the client [amount].
Fee less supplied costs so far: [amount]. [This is not a margin: the gaps below are not in it, so on the costs side the full figure is this or lower. / No gaps: this is the result on the costs supplied.]
Workstreams: [n] ([n] scheduled, [n] not in the fee schedule). Flagged: [n] workstreams with at least one fired test. Gaps: [n] numbered items.

TIE-OUT
Fee lines add to the agreed fee: [amounts] = [amount].
Hours: approved hours by workstream add to the export's approved rows: [n + n] = [n]. Not approved: [n]. Export total [n], [computed from the rows, not checked against a report / checked against the report].
Billing: fees billed by workstream add to the fee invoices: [amounts] = [amount]. Recharges: [amount].
Costs: invoiced by workstream add to the list: [amounts] = [amount]. Not yet invoiced: [amounts, with "amount not supplied" where blank] = [amount].
Results: workstream results add to the engagement: [amounts] = [amount].

WORKSTREAMS
[Workstream]. Fee [amount / none]; billed [amount] ([n]% / no fee); unbilled [amount / none].
Hours: budget [n]; approved [n] ([n]%); not approved [n]; expected still to come [n / not supplied]; projected [n] ([n]% over / under / not stated).
Cost: time [amount] ([n] hours without a rate / all hours rated); direct costs invoiced [amount]; not yet invoiced [amount / amount not supplied]; recharged [amount]. Supplied cost [amount][, at least, if any gap touches its cost] ([n]% of the agreed fee / no fee).
Fee less supplied costs so far: [amount], [complete / incomplete ([reason])].
Tests: Hours over budget: [fired / not fired / not run] ([figures; test n%]). Effort ahead of billing: [fired / not fired / not run] ([n] points; test [n]). Cost limit: [fired / not fired / not run] ([n]%; limit [n]% / no limit set[; the cost is at least this, if a gap touches it])[, on the costs supplied only, if not fired and a gap touches the cost].
[Repeat for each workstream, in the fee schedule's order, then any workstream not in the schedule, marked "(not in the fee schedule)".]

GAPS THAT LIMIT THE VIEW
[Numbered. Hours not approved: workstream, hours, status, and the recorded and projected hours if they were approved. No cost rate: role, hours, workstreams. Costs not yet invoiced: workstream, item, amount stated and included / amount not supplied and not included. Not in the fee schedule: workstream, hours, time cost. Remaining hours not supplied: workstream. Fee billed above the agreed fee: workstream, amount. Recharge above the direct costs counted: workstream, amount. Possible duplicates: items. / None.]

QUESTIONS FOR THE TEAM
[Numbered. [Role]. [Workstream]: [the figures]. [The question]. / None.]

DECISIONS FOR THE [PARTNER ROLE] AND THE [FINANCE LEAD ROLE]
[Numbered. [Category]. [The facts]. Whether to [the decision], [once questions n are answered]. / None.]

Draft for the [partner role]'s and the [finance lead role]'s review. Every figure comes from the files listed above and is for the two of them to validate. No fee has been set, nothing has been written off, no cost rate has been invented, no record has been changed and nothing has been sent.
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
