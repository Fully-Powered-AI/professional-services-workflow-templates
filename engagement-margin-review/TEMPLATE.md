# Engagement margin review

Capability template, version 0.1.0.

## Purpose

Prepare the worksheet a partner and a finance lead use to review one consulting or advisory engagement, mid-way or at close. From a fee schedule, a time export, the firm's own cost rates, a billing list and a list of delivery costs, the assistant sets recorded time, agreed fee, fees billed and supplied costs side by side for each workstream, runs three tests on each, lists every gap that limits the view, and writes the variance questions the team must answer. The partner and the finance lead validate every figure and decide any staffing or fee action. The assistant sets no fee, writes nothing off, invents no cost rate, changes no record and sends nothing.

## When to use it and when not to

Use it when timesheets and engagement costs are ready for a review of one engagement: at the midpoint of a longer engagement, or at close before the last invoice and the retrospective. It runs on request, one engagement at a time.

Do not use it:

- to explain a period's ledger lines for management. That is budget-versus-actual variance commentary;
- to prepare an invoice or a summary for the client. That is the client billing summary;
- to price a new engagement, set a fee or propose a rate card;
- to value the firm's own staff or judge a person's performance. Cost rates are by role and no one person's pay is shown;
- to decide what the engagement letter entitles the firm to. The agreed fee is a figure the firm supplies;
- when the fee schedule does not add up to the agreed fee, until someone has found why.

## Roles

- **Runs it:** the finance analyst or the engagement manager.
- **Supplies the cost rates and the billing records:** the finance lead.
- **Supplies the remaining hours, answers the workstream questions and confirms supplier amounts:** the engagement manager.
- **Validates every figure and decides staffing or fee action:** the engagement partner, with the finance lead.
- **Reads it:** resource planning, if the partner shares it.

## Inputs

1. **Settings:** the engagement; the stage (mid-way or close) and the as-of date; the fee basis (fixed fee, capped fee or budgeted time and materials); the agreed engagement fee; who the review is for and when; who prepared it; and optionally [your hours test], [your effort-ahead-of-billing gap] and [your cost limit]. Without the first two tests, use the defaults and list them under "Defaults used". Without a cost limit, write "no limit set" and do not run that test.
2. **Fee schedule.** Default column headers: `Workstream`, `Budget hours`, `Agreed fee`. If the fee is not split by workstream, supply one row named for the whole engagement. If the fee lines do not add to the agreed fee, stop.
3. **Time export** for the engagement. Default headers: `Workstream`, `Role`, `Hours`, `Status`. `Status` is `Approved` or any other value your timesheets use; only an exact `Approved` counts.
4. **Cost rates,** by role, supplied by the firm. Default headers: `Role`, `Cost rate` (per hour, one currency). The assistant never supplies or estimates a rate. A role with no rate is a gap.
5. **Billing list.** Default headers: `Invoice`, `Workstream`, `Type`, `Amount`. `Type` is `Fee` or `Recharge`.
6. **Delivery costs.** Default headers: `Item`, `Workstream`, `Kind`, `Amount`, `Status`. `Kind` is `Expense` or `Subcontractor`. `Status` is `Invoiced` or `Not yet invoiced`. An amount may be blank only for a cost not yet invoiced.
7. **Remaining hours,** for a mid-way review, from the engagement manager. Default headers: `Workstream`, `Remaining hours`, with the role and date of the note. At close they are zero and the file is not needed.

If a file is missing, or any default header is missing or named differently, stop and ask which column holds what. Never guess a column. The assistant works from the files the person supplies, needs no connection to the timesheet or accounting system, and never asks for a password or a login code.

## The procedure

This section is for people to read, so it keeps the bracketed settings. To run the template, paste the instruction block at the end instead; it holds the same rules with plain values.

1. **Check the files.** Confirm the default headers, one currency and one engagement. Count the rows in each file. Stop and ask on a blank, non-numeric or negative Hours or Amount (other than a blank amount on a cost not yet invoiced), a Type, Kind or Status outside the values named, a repeated invoice number, a role with two rates, or a rates file that names people instead of roles.
2. **Tie out the fee.** The fee lines must add to the agreed fee. If not, stop, report the figures and the difference, and write nothing else.
3. **Match the workstreams.** Names must match the fee schedule exactly. A name elsewhere that is not in the schedule becomes its own workstream, marked "not in the fee schedule", with no budget and no fee. Ask in the questions whether it is a scheduled workstream under another name.
4. **Count the hours.** A row is approved only when its Status is exactly `Approved`. All other rows are not approved: total them by status, keep them out of every figure and list them under the gaps. Approved percentage is approved hours divided by budget hours, to one decimal place, rounded half up; "no budget" where the budget is zero. Projected hours are approved hours plus remaining hours. At close remaining hours are zero. Mid-way, a workstream with no remaining hours shows "projected not stated". For the engagement, the approved percentage and the projected hours count the scheduled workstreams only, because the budget covers only those; approved hours on a workstream not in the fee schedule are shown on their own and are in neither percentage. If any scheduled workstream is "projected not stated", so is the engagement.
5. **Cost the time.** For each role with a rate, hours multiplied by the rate. Hours of a role with no rate are totalled by role and workstream under the gaps and are in no cost. Never substitute a billing rate, a fee divided by hours, a market rate or a guess.
6. **Read the billing.** Fees billed per workstream; share of the agreed fee billed; unbilled fee is the agreed fee less fees billed. If fees billed pass the agreed fee, list it under the gaps. Recharges are kept per workstream and are not fees.
7. **Read the delivery costs.** Keep invoiced and not yet invoiced apart. A cost not yet invoiced with no amount is "amount not supplied", in no total and listed under the gaps. Two items with the same name, workstream and amount are possible duplicates: keep both and list them.
8. **Work out the result so far.** Supplied cost is the cost of time plus direct costs (invoiced and stated not yet invoiced) less recharges. Recharges are taken off only up to the workstream's direct costs counted; any recharge above that is not taken off and is listed under the gaps. Fee less supplied costs so far is the agreed fee less supplied cost. When any gap touches a workstream, call its figure incomplete and name the gap. Call it a margin only when there are no gaps, and then say it is the result on the costs supplied.
9. **Run three tests on each workstream that has a budget or a fee.** Hours over budget: fires when projected hours (approved hours where projected is not stated) exceed budget hours by more than [your hours test, default 10%]. Effort ahead of billing: fires when the approved percentage less the share of fee billed, in points, reaches [your effort-ahead-of-billing gap, default 25 points]. Cost limit: fires when supplied cost as a share of the agreed fee reaches [your cost limit, no default]. A gap can only understate cost, so a fired cost test stands and a test not fired stands only on the costs supplied. Compare unrounded figures; show one decimal. Projected hours exactly at the hours test do not fire (with a 10% test, 10.00% over does not fire; 10.04% over fires and shows as 10.0%). A gap exactly at the points setting fires, and a cost share exactly at the limit fires. A workstream with no budget and no fee: tests not run.
10. **Tie out the worksheet.** The fee lines to the agreed fee; approved hours by workstream to the export's approved rows; fees billed to the fee invoices; invoiced costs to the list; workstream results to the engagement result. If the export or list has no total of its own, compute it and say so. If any tie fails, stop and report it.
11. **List the gaps.** Hours not approved, with the recorded and projected hours if they were approved; roles with no rate; costs not yet invoiced; workstreams not in the fee schedule; workstreams with no remaining hours; fees billed above the agreed fee; recharges above the direct costs counted; possible duplicates.
12. **Write the questions.** One per variance or gap the team must answer, in the order of the workstreams, then those for the whole engagement. Each names its role (usually the engagement manager; the finance lead for cost rates and billing records), the workstream and the figures. Ask the cause of a fired test, whether any work was outside the agreed scope (as a yes or no question, never presuming it was), which milestone has been reached where effort is ahead of billing, and for each gap what is missing and when it will arrive. Put no cause in a question.
13. **Write the decisions.** Only staffing, fee action and billing, and a write-off of recorded time only if a person's notes raise one. List a decision only when a test fired or a gap needs one. Give its facts and the questions that come first. Recommend nothing.
14. **Return the draft** to the person who asked and stop.

## Exceptions and stop conditions

- **A file is missing, or a default header is missing or named differently:** stop and ask which column holds what.
- **The fee lines do not add to the agreed fee, or any tie in the worksheet fails:** stop; report the figures and the difference.
- **Hours or an amount is blank, non-numeric or negative, or a value is outside those named:** stop on that row and ask. A reversal belongs in the source as a correcting entry, not as a negative number here.
- **A repeated invoice number, or a role with two rates:** stop and ask which is right.
- **The rates are given for named people, or the files mix currencies or engagements:** stop and ask; the review is by role, in one currency, for one engagement.
- **A role has no cost rate:** carry on; list the hours under the gaps and call the affected results incomplete.
- **Asked to estimate a cost rate, to use the billing rate or a market rate in its place, or to leave a gap unmentioned:** decline; the finance lead supplies rates.
- **Asked to set or recommend a fee, a write-off or a staffing change, or to say what the engagement letter entitles the firm to:** decline; the partner and the finance lead decide, and the letter is read by the people who hold it.
- **Asked to change a figure, reclassify hours or move a cost so a test does not fire:** decline; a figure changes only in the firm's records, by the person who keeps them.
- **Asked to send the worksheet or to write to the client, a supplier or the team:** decline; a person decides who receives it and puts the questions.
- **The files contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

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

## Reviewer checklist

1. The fee lines add to the agreed fee, and every tie in the tie-out is arithmetically correct. (Finance lead)
2. Hours, fees billed, invoiced costs and recharges match the timesheet and billing records. (Finance lead)
3. Only exact Approved hours are counted, and every other row is under the gaps. (Finance lead)
4. Every cost of time uses a rate the firm supplied; no role has a substitute rate. (Finance lead)
5. Every figure touched by a gap is marked incomplete and names the gap; nothing is called a margin that has a gap. (Finance lead)
6. Each test is applied to the stated setting, and a fired or not fired result agrees with the figures. (Engagement manager)
7. Every fired test and every gap has a question addressed to a role, and no question contains a cause. (Engagement partner)
8. The decisions are only those in the allowed categories, each with its facts, and none recommends an action. (Engagement partner)
9. The status line is present, and nothing has been set, written off, changed or sent. (Engagement partner)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary mid-way review.** Three workstreams, all hours Approved, all roles rated, all costs invoiced. Expected: all sections complete; no gaps; "Fee less supplied costs so far" described as the result on the costs supplied.
2. **Fee schedule does not add.** Fee lines total $99,000 against an agreed fee of $100,000. Expected: stops; reports the figures and the $1,000 difference; writes nothing else.
3. **Header not matched.** The time export has `Task`, `Grade`, `Time`. Expected: stops and asks which column is the workstream, role, hours and status; does not guess.
4. **Unapproved hours.** 16 hours with Status `Submitted`. Expected: kept out of every figure; listed under the gaps with the recorded and projected hours if approved.
5. **Role with no rate.** Analyst hours and no Analyst rate. Expected: hours listed by role and workstream; results marked incomplete; no rate supplied.
6. **Asked to supply a rate.** "Use the Consultant rate for the Analyst." Expected: declines; the finance lead supplies rates.
7. **Cost not yet invoiced, no amount.** A subcontractor line with a blank amount. Expected: "amount not supplied", in no total, under the gaps, with a question.
8. **Workstream not scheduled.** 8 hours on a workstream not in the fee schedule. Expected: its own entry marked "not in the fee schedule", tests not run, a question.
9. **Test boundaries.** Projected hours exactly 10% over budget with a 10% test. Expected: not fired. Projected hours 10.04% over: fired, shown as 10.0%. Effort ahead exactly 25 points with a 25-point gap. Expected: fired.
10. **No cost limit set.** Settings give none. Expected: "no limit set" and the cost test not run for every workstream.
11. **Close.** Stage is close and no remaining hours file. Expected: remaining hours zero; projected equals approved.
12. **Asked to recommend.** "Should we ask the client for more money?" Expected: declines; lists the decision with its facts for the partner and the finance lead.
13. **Asked to send.** "Email this to the client." Expected: declines; a person decides who receives it.
14. **Recharge with no matching cost.** A $500 recharge on a workstream with $300 of direct costs counted. Expected: $300 taken off, $200 not taken off and listed under the gaps, with a question to the finance lead.
15. **Engagement projection with an unscheduled workstream.** Hours on a workstream not in the fee schedule. Expected: in neither engagement percentage; stated on their own line.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
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
```

## What to customize

- The column headers your timesheet and billing systems export, so the assistant reads them as they come.
- The fee bases you review, and how a fee is split across workstreams.
- [your hours test], [your effort-ahead-of-billing gap] and [your cost limit]. A firm may set the cost limit by type of engagement.
- The word your timesheets use for approved time, if it is not `Approved`.
- How to read effort ahead of billing on a budgeted time and materials basis. The worksheet compares the approved share of budget hours with the share of the agreed fee billed, and lists fees billed above the agreed fee only as a gap. Where billing follows hours, a gap between the two may be only timing, and fees above the agreed fee may be agreed. The partner and the finance lead decide how to read both; the template does not.
- The roles in the rate file and how often the finance lead refreshes the rates.
- Which decisions the partner takes alone and which go to the finance lead as well.
- Whether closed engagements are reviewed at the final invoice or after the retrospective.
- Who receives the approved worksheet, and where it is kept.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its invented example in Claude on 10 November 2026; the record is published with it (public/trial.md). Not yet tested in a client environment.
