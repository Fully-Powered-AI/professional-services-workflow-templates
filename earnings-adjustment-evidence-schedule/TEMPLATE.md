# Quality of earnings adjustment evidence schedule

Workflow template, version 0.1.0.

## Purpose

Prepare the evidence schedule a deal team needs when management of a business being bought or sold proposes adjustments to its reported EBITDA. For each proposed adjustment, the schedule shows the ledger entries management cites and whether they add up to the amount, management's explanation, the supporting documents and whether each matches its entry, and the facts a reviewer would challenge: a cost that also appears in the prior year, a ledger entry claimed by two adjustments, an entry outside EBITDA or outside the test period, and an estimate whose figures have no document behind them. Every gap becomes a draft question for management. The assistant prepares; it proposes no adjustment of its own, states no adjusted earnings of its own, gives no valuation and no opinion, sends nothing and changes no record. The engagement lead decides which adjustments the firm accepts.

It traces management's adjustments to evidence. Agreeing a client's schedule to its own ledger is client schedule to ledger reconciliation; tracking which requested records have arrived is the client document request tracker.

## When to use it and when not to

Use it when a transaction-advisory or accounting team receives management's list of proposed EBITDA adjustments for one target business and one test period, with the ledger detail and documents behind them, and the team must see what is supported before it forms a view. Run it again when management answers questions or sends more documents.

Do not use it:

- to find adjustments management has not proposed. That is the team's own analysis;
- to say whether an adjustment should be accepted, to compute an adjusted EBITDA of the firm's own, or to comment on value, price or deal terms;
- to give an audit, assurance, tax or accounting opinion, or to decide how an item should be accounted for;
- for several businesses or several test periods in one run.

## Roles

- **Runs it:** a member of the deal team, such as the manager or senior on the engagement.
- **Decides which adjustments the firm accepts, in whole or in part, and signs off the analysis:** the engagement lead.
- **Decides which questions go to management, and sends them:** the engagement lead, or a person the lead names.
- **Answers questions only the business can answer:** the target's finance contact.

## Inputs

All amounts are in one currency. If the files mix currencies, stop.

1. **Engagement settings,** as labelled lines: target, test period start and end, look-back period start and end, currency, reported EBITDA for the test period per the financial statements, management's adjusted EBITDA as stated (or "not stated"), tie tolerance (default 0.00), one-off categories (default: non-recurring), estimate categories (default: normalisation; pro forma), files received on, the engagement lead and the target's finance contact. If the test period or the reported EBITDA is missing, stop and ask.
2. **Management's adjustment list.** Default headers: adj_ref, description, mgmt_category, amount, entries_cited. Amount is the effect on EBITDA: positive raises it, negative lowers it. entries_cited holds ledger entry IDs separated by semicolons, or is empty. If an adj_ref appears twice, stop and ask.
3. **Ledger detail.** Every entry in the accounts the adjustments cite, for the test period and the look-back period. Default headers: entry_id, date, account_code, account_name, counterparty, description, amount. Debits are positive and credits negative, as exported.
4. **Account map.** Default headers: account_code, account_name, statement_line, in_ebitda (yes or no). If it is missing, continue and record under "Not assessed" that the EBITDA check was not made.
5. **Management's explanations,** one paragraph per adjustment headed by its adj_ref, with the date received. An adjustment with no paragraph has no explanation.
6. **Supporting documents index.** Default headers: doc_ref, adj_ref, doc_type, doc_date, counterparty, amount, what_it_shows. Where the documents themselves are supplied instead, read the same fields from each and mark them "read from the document".
7. **Earlier questions and answers,** if this is a second run. If none, write "first run".

If a header does not match the defaults, stop and ask which column is which. Never guess a column. The assistant works only from the files supplied; it needs no access to the target's systems and never asks for a password or a login code.

## The procedure

1. **Check the files.** Confirm one target, one test period and one currency. Count the adjustments. Flag any entry ID that appears twice in the ledger detail, and stop if an adj_ref appears twice.
2. **Set out management's bridge.** Reported EBITDA, then each adjustment as management lists it, then the total of the adjustments and reported EBITDA plus that total. Compare the result with management's adjusted EBITDA as stated, and show any difference. These are management's figures, set out as given; the bridge adds nothing of the firm's own.
3. **Link the ledger.** For each adjustment, link only the entries management cites by ID. Never link an entry management did not cite, even one that looks related; it may be named in a question, never counted. A cited ID that is not in the ledger detail is listed as "cited, not in the ledger detail".
4. **Test the period.** A linked entry dated outside the test period is listed with its date, raises the flag "Outside test period", and is left out of the tie.
5. **Tie the amount.** For an adjustment not in an estimate category, add the linked entries dated in the test period, debits positive and credits negative. It ties when the adjustment's amount equals that sum within the tolerance. Otherwise show the difference, as the adjustment minus the linked entries in the test period. With no entries cited, write "No entries cited".
6. **Test the calculation of an estimate.** For an adjustment in an estimate category, take the calculation from management's explanation. Recompute it; if the result differs from the amount, raise the flag "Calculation differs". Tie any figure in the calculation that comes from the ledger to the linked entries in the test period, within the tolerance; the Ledger line then reads "Estimate: tied in the calculation". List every other figure as an assumption, with the document that supports it or "no document". If the files do not say whether the ledger figure and an assumption are on the same basis (for example, one stated before and the other after a volume rebate), add a question asking. Never supply a figure of your own, such as a market rate, to fill a gap.
7. **Test the EBITDA line.** A linked entry in an account the account map marks in_ebitda "no" raises the flag "Outside EBITDA", with the account and amount.
8. **Find overlaps.** An entry ID linked by two or more adjustments raises the flag "Overlap" on each of them, naming the entry, its amount and the other adjustments.
9. **Look back, for one-off categories.** For each adjustment in a one-off category, list the entries in the look-back period in the same accounts as its linked entries, leaving out its own linked entries: their number and total, and separately those with the same counterparty as a linked entry. Same-counterparty entries raise the flag "Recurs". This is a fact for the reviewer, not a finding that the item recurs. Read "0 entries" as none in the ledger detail supplied, which holds only the accounts management cites; it does not show that the accounts held none. A Recurs flag that rests on an entry two adjustments both cite is shared with the other adjustment's flag; it is one fact, not two. If the ledger detail holds no entries dated in the look-back period other than entries management cites, write "Look-back: not possible; no entries supplied for the period". For other categories, write "Look-back: not checked; [category] is not a one-off category".
10. **Read the explanation.** Record whether one was supplied and its date, in a short summary in management's own terms. Where the explanation states an amount, date or counterparty for a linked entry itself that differs from that entry, quote both and raise the flag "Explanation differs". A date or event the explanation gives for the underlying matter (a settlement, a closure) is not a date for the entry, and is not compared.
11. **Match the documents.** A document matches a linked entry when the counterparty is the same and the amounts agree without regard to sign, within the tolerance. Every linked entry needs a matching document; list each one without as "no document". List a document indexed to the adjustment that matches no linked entry as "matches no linked entry". Compare only what the index or the document states; never judge whether a document is genuine.
12. **Give each adjustment its evidence status,** in this order:
    - **Traced:** the amount ties (for an estimate: the calculation recomputes, its ledger figures tie and every assumption has a document), an explanation was supplied, every linked entry has a matching document, and there is no flag.
    - **Traced with flags:** everything in Traced holds, and one or more flags are raised.
    - **Not traced:** anything else.
    The status describes the evidence. It is not a view on whether the adjustment should be accepted, and it must never be described as one.
13. **Draft the questions.** Every gap and every flag becomes a question for management, numbered Q1, Q2 in adjustment order (a question that serves several adjustments is numbered at the first adjustment it serves), and within an adjustment in the order ledger, calculation, explanation, documents, flags. Each names the adjustment, the entry, the amount and the answer or document that would close it. One question may cover several gaps or flags that rest on the same entry, and may serve several adjustments; list it under each. Write each as a question of fact, never as a conclusion. Where earlier answers were supplied, mark each earlier question answered, partly answered or still open, and keep only the open parts.
14. **Summarise by status.** Count and total the adjustments in each status, and check that the three totals add up to management's total. List every overlapping entry once, with its amount.
15. **List the decisions for the engagement lead.** Always: which adjustments the firm accepts, in whole or in part, and which questions are sent. Then one decision for each flagged matter, in adjustment order and, within an adjustment, in the order Recurs, Overlap, Outside EBITDA, Outside test period, Calculation differs, Explanation differs; flags on several adjustments that rest on the same entry share one decision. State the facts and the question. Recommend nothing.
16. **State what was not assessed:** adjustments management did not propose, entries management did not cite, whether any document is genuine, anything outside the look-back period supplied, and any check skipped for a missing input.

## Exceptions and stop conditions

- **A header does not match:** stop and ask which column is which.
- **The test period or the reported EBITDA is missing, or an adj_ref appears twice:** stop and ask.
- **Mixed currencies:** stop and ask which governs; convert nothing.
- **A cited entry is not in the ledger detail:** list it, leave it out of the tie, and ask for it.
- **The calculation in an explanation cannot be followed** (a figure is missing or the steps do not lead to a number): write "calculation not recomputable", give the status Not traced and ask for the working.
- **A file contains bank details, a password or a login code:** do not repeat it in the schedule; tell the person to remove it from the source.
- **The explanation names an employee in connection with pay or a dispute:** refer to the role, not the person.
- **Asked to propose, accept or reject an adjustment, to compute an adjusted EBITDA of the firm's own, to value the business or comment on price, to give an audit, assurance, tax or accounting opinion, to supply a market figure, to send the questions or contact the target, or to change any file or record:** decline and name the person who does it.

## Output format

Write every date as yyyy-mm-dd.

```
QUALITY OF EARNINGS ADJUSTMENT EVIDENCE SCHEDULE: [target], test period [start] to [end]

[If the run stops, print only this title, then "Stopped: [the reason]. [The question for the person who ran it.]" and nothing else.]

Draft for: [engagement lead]. Files received [date]. Currency: [currency]. Run: [first run / second run, after answers of date].
File checks: [entry IDs that appear twice in the ledger detail / None.]
This schedule traces [target] management's proposed adjustments to the evidence supplied. It proposes no adjustment, states no adjusted earnings of its own, and gives no valuation and no opinion.

1. Management's bridge (management's figures, as supplied)
Reported EBITDA per the financial statements: [amount]
[One line per adjustment: ref, description, category: amount]
Management's adjustments, total: [amount]
Reported EBITDA plus management's adjustments: [amount]. Management's adjusted EBITDA as stated: [amount / not stated]. [Agrees. / Differs by [amount].]

2. Summary by evidence status
Traced: [n], [amount]: [refs / None.]
Traced with flags: [n], [amount]: [refs / None.]
Not traced: [n], [amount net]: [refs / None.]
Total: [n], [amount]. [Agrees / Does not agree] to management's total, [amount].
Entries cited by more than one adjustment: [entry, amount, refs / None.]

3. Adjustments
[Ref]. [Description]. Category: [category]. Amount: [amount]. Evidence status: [status].
Ledger: [entry, date, account, counterparty, amount; ...] / No entries cited. Linked entries in the test period: [sum]. [Ties. / Does not tie: difference (adjustment minus linked entries in the test period) [amount]. / Estimate: tied in the calculation.] [Outside the test period: [entries] / Cited, not in the ledger detail: [IDs]]
Calculation: [management's calculation; recomputed [amount], [agrees / differs]; ledger figure [amount] [ties / does not tie]; assumptions: [figure, document or "no document"]] / Calculation not recomputable: [what is missing]. / Not an estimate.
Explanation: [supplied [date]: summary] / Not supplied.
Documents: [doc ref matches entry, adding "(read from the document)" where no index was supplied; entry: no document; doc ref matches no linked entry]. [None indexed, when no document is indexed to the adjustment.]
Look-back [start] to [end]: same accounts [n] entries, [amount]; same counterparty [entries / none]. / Look-back: not checked; [category] is not a one-off category. / Look-back: not possible; no entries supplied for the period.
Flags: [in this order: Recurs / Overlap / Outside EBITDA / Outside test period / Calculation differs / Explanation differs, each with its facts] / None.
Questions: [Q numbers] / None.

4. Questions for management (draft; the engagement lead decides which are sent)
Q[n]. ([refs]) [The question of fact, naming the entry, amount and the answer or document that would close it.] [Earlier answer: answered / partly answered / still open.]
[or: None.]

5. Decisions for the engagement lead
1. Which of management's [n] adjustments the firm accepts, in whole or in part. The evidence status above is not that decision.
2. Which of the questions are sent to management, and in what form.
[n]. [One per flagged matter: the facts, and the question for the lead.]

6. Not assessed
[Always: adjustments management did not propose; entries management did not cite; whether any document is genuine; anything outside the look-back period supplied. Then any check skipped for a missing input.]

Prepared from the files received [date] for the [engagement lead]'s review. It changes no records and sends nothing.
```

## Reviewer checklist

1. Management's bridge adds up, and its total agrees with the adjustment list. (Deal team member who ran it)
2. Every linked entry was cited by management, and no other entry is counted. (Deal team member who ran it)
3. Every tie, difference and recomputed calculation is arithmetically right, with entries outside the test period left out. (Engagement lead)
4. Every assumption in an estimate shows its document or "no document", and no figure was supplied by the assistant. (Engagement lead)
5. Every overlap, outside-EBITDA, outside-period and recurrence flag is true against the ledger detail and account map. (Engagement lead)
6. No status is described as acceptance or rejection, and no adjusted EBITDA of the firm's own appears. (Engagement lead)
7. Every gap and flag has a question, and every question is a question of fact. (Engagement lead)
8. The three status totals add up to management's total, and every empty section says "None." or the stated alternative. (Deal team member who ran it)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal run.** Use the invented example. Expected: one Traced (A4, 7,300.00), one Traced with flags (A3, 12,500.00), four Not traced (113,400.00 net), totals agreeing to 133,200.00, eight questions, or fewer where one question covers several gaps on the same entry (the trial produced six), and six decisions.
2. **Header mismatch.** Rename the amount column in the ledger detail. Expected: stops and asks which column is which.
3. **Uncited entry.** Remove G-230 from A5's entries_cited. Expected: A5 does not tie (difference 3,000.00); G-230 is not linked to A5 and is named only in a question; the overlap flag disappears from both, and so does A5's Recurs flag, which rested on G-230.
4. **Market figure asked for.** Ask the assistant what a general manager would cost. Expected: declines to supply a figure and keeps the question for management.
5. **Calculation differs.** Change A1's amount to 95,000.00. Expected: "Calculation differs", status Not traced, a question asking for the working. The bridge also differs from management's stated 975,800.00, by 5,000.00.
6. **Asked for a view.** Ask which adjustments are supportable, or for a diligence-adjusted EBITDA. Expected: declines, names the engagement lead, and leaves the statuses as they are.
7. **No look-back data.** Remove every entry dated in the look-back period except I-601. Expected: "Look-back: not possible" for A2 to A6; no Recurs flag; the gap stated under "Not assessed".
8. **Second run.** Supply an answer and the missing invoice for G-230. Expected: Q4 marked answered or partly answered; G-230 shows a matching document; the overlap flag stays until the lead decides.
9. **Asked to send.** Ask for the questions to be emailed to the finance contact. Expected: declined; the draft is returned to the person who ran it.

## Instructions for the AI assistant

```
You prepare an evidence schedule for a deal team's engagement lead. It
traces management's proposed EBITDA adjustments for one target and one
test period to the files supplied. You propose no adjustment, compute no
adjusted EBITDA of the firm's own, give no valuation, comment on no price,
and give no audit, assurance, tax or accounting opinion. You never send
anything, contact the target or change a file or record; a person
approves and sends anything that leaves the team. The engagement lead
decides which adjustments are accepted.

The user supplies: settings (target, test period, look-back period,
currency, reported EBITDA, management's adjusted EBITDA as stated, tie
tolerance default 0.00, one-off categories default "non-recurring",
estimate categories default "normalisation; pro forma", files received
on, engagement lead, finance contact); the adjustment list (adj_ref,
description, mgmt_category, amount, entries_cited); ledger detail
(entry_id, date, account_code, account_name, counterparty, description,
amount; debits positive, credits negative); an account map (account_code,
account_name, statement_line, in_ebitda); management's explanations by
adj_ref; a documents index (doc_ref, adj_ref, doc_type, doc_date,
counterparty, amount, what_it_shows); earlier questions and answers, if
any. If a header does not match, stop and ask which column is which. If
the test period or reported EBITDA is missing, an adj_ref repeats, or the
currency is mixed, stop and ask. Flag any entry_id that appears twice
in the ledger detail. Never ask for a password or login code.

1. Bridge: reported EBITDA, each adjustment as listed, their total, and
   reported plus total compared with management's stated figure.
2. Link only entries management cites by ID. Never link or count another
   entry; you may name it in a question. List cited IDs missing from the
   ledger detail.
3. Entries dated outside the test period: flag "Outside test period" and
   leave them out of the tie.
4. Non-estimates: the amount ties when it equals the sum of linked entries
   in the test period within the tolerance; otherwise show adjustment
   minus that sum. Estimates: recompute management's calculation (flag
   "Calculation differs" if it does not give the amount), tie its ledger
   figures, and list every other figure as an assumption with its
   document or "no document". Ask whether figures are on the same basis
   when the files do not say. Never supply a figure of your own.
5. Flag "Outside EBITDA" for a linked entry in an account mapped in_ebitda
   no, and "Overlap" on every adjustment that links the same entry.
6. One-off categories only: in the look-back period, count and total the
   entries in the same accounts, excluding the adjustment's own, and list
   those with the same counterparty as a linked entry; any such entry is
   flag "Recurs", a fact for the reviewer and not a finding; a Recurs
   flag resting on an entry two adjustments both cite is one fact,
   shared. If the look-back period holds no entries except cited ones,
   say the look-back was not possible. "0 entries" means none in the ledger
   detail supplied.
7. Explanation: supplied or not, with its date; if it states an amount,
   date or counterparty for a linked entry itself that differs from that
   entry, quote both and flag "Explanation differs". A date or event it
   gives for the underlying matter is not compared.
8. Documents: a document matches a linked entry on the same counterparty
   and the same amount without regard to sign. Mark each linked entry with
   no match "no document" and each unmatched document "matches no linked
   entry". Never judge whether a document is genuine.
9. Status: Traced (ties or estimate fully supported, explanation supplied,
   every entry documented, no flag); Traced with flags (the same, with
   flags); Not traced (anything else). A status is never a view on
   acceptance; never describe it as one.
10. Questions: one for every gap and flag, numbered in adjustment order,
    then ledger, calculation, explanation, documents, flags. Each is a
    question of fact naming the entry, amount and what would close it.
    One question may cover gaps or flags resting on the same entry, or
    serve several adjustments; number it at the first adjustment it
    serves. On a second run mark earlier questions answered, partly
    answered or still open, and keep only the open parts.
11. Summarise by status; the three totals must add to management's
    total. List the decisions for the engagement lead: always which
    adjustments are accepted and which questions are sent, then one per
    flagged matter (flags resting on one entry share one). Recommend
    nothing. State what was not assessed.

If the account map is missing, carry on and write under "Not assessed"
that the EBITDA check was not made. If an estimate's calculation cannot
be followed, write "calculation not recomputable", give the status Not
traced and ask for the working. If a file holds bank details, tell the
person to remove them from the source.

Use the output format exactly, in the same section order, with "None."
or the stated alternative for any empty part. Every figure must trace to
a supplied file. Do not repeat bank details, passwords or login codes
found in a file. Refer to an employee by role. Write every date as
yyyy-mm-dd. Decline to propose, accept or reject an adjustment, compute an adjusted EBITDA of the firm's
own, value the business, give an opinion, supply a market figure, send
the questions or change a record; name the engagement lead instead.
```

Paste this block as custom instructions, followed by the output format above.

## What to customize

- The column names your ledger exports and data room index produce.
- The tie tolerance, and the one-off and estimate categories your firm uses.
- The length of the look-back period: one prior year by default, more where the files allow.
- Who runs it, who the engagement lead is, and who sends questions to the target.
- How your firm wants questions phrased and numbered, so the list can go straight into its request tracker after the lead's review.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini, given the confidentiality of the deal, and where the signed-off analysis is kept.

## Version notes

- 0.1.0, 11 November 2026. Written by Fully Powered AI from its own published map of the work, a transaction-advisory team receiving management's proposed earnings adjustments. No third-party text or method is used. Tried once on its invented example in Claude on 11 November 2026; the record is published with it. After that run its wording was tightened following independent review (a few lines added to the instructions for edge cases the example does not reach, and clarifications to the procedure and acceptance tests); a later review pass made small further edits (which dates the explanation check compares, a different illustration for a basis mismatch, two rules carried into the instruction block, and one date style, yyyy-mm-dd, which the example's schedule now uses throughout); the example's inputs and figures and the output format's sections were not changed, and the example was not run again. Not yet tested in a client environment.
