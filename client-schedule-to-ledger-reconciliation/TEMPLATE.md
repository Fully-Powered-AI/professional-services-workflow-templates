# Client schedule to ledger reconciliation

Capability template, version 0.1.0.

## Purpose

Prepare the worksheet an accountant needs when a client's subledger schedule does not agree to the control account in its trial balance. The worksheet proves each side to its own reported balance, matches the two by document reference, separates timing differences from entries with no explanation, and sets out the steps that would settle each one. Every figure traces to a line in a supplied file. The assistant prepares; it never posts, changes a record, contacts the client, or decides that an explanation is accepted. It gives no audit, tax or assurance opinion.

It reconciles a client's subledger schedule to its own ledger. Agreeing the books to a bank statement is bank reconciliation preparation; deciding what to do with individual receipts is receivables exception review.

## When to use it and when not to

Use it when a schedule from the client, or from the client's subledger, differs from the control account at one reporting date and someone must find out why. One run covers one subledger, one control account and one reporting date.

Do not use it for a bank account, for a difference between two ledgers of different clients, or for a schedule that covers several reporting dates. Do not use it to give assurance on the balance, to advise on tax treatment, or to decide how a disputed item is classified.

## Roles

- **Runs it:** the accountant or controller who looks after the client's books.
- **Confirms each explanation, and agrees any correcting entry with the client:** the responsible accountant.
- **Answers questions only the client can answer:** the client's finance contact.
- **Posts any entry:** a person with access to the ledger, after the responsible accountant and the client agree it.

## Inputs

All amounts are in one currency; debits and receipts are as the files give them. If a file mixes currencies, stop.

1. **Settings,** as labelled lines: client, subledger, control account, reporting date, period start, files run on, currency, subledger opening balance, subledger closing balance per the subledger report, ledger opening balance, tolerance, the date up to which to look for late postings, the sign convention if the subledger is not receivables (for payables, the signs the files give), the responsible accountant and the client contact. If the reporting date or either closing balance is missing, stop.
2. **Trial balance extract.** Default headers: account_code, account_name, debit, credit, under a first line "As at: YYYY-MM-DD". The control account is the line named in the settings. If the extract carries no as-at line, say its date was taken from the settings and not checked.
3. **Subledger schedule.** One line per document, with default headers doc_ref, doc_date, customer, doc_type, amount. Invoices are positive; receipts and credit notes are negative. For a payables subledger, use the signs the files give and record that in the sign convention setting. It should include lines dated after the reporting date, up to the files-run-on date, so timing can be seen.
4. **Journal detail for the control account.** Default headers: journal_id, doc_ref, posting_date, source, description, amount. Source says where the journal came from, such as the subledger interface, the cash book or a manual journal. It should include journals posted after the reporting date, up to the date in the settings.
5. **The last reconciliation** showing the agreed opening difference and any open items, and **any notes from the client.** If the last reconciliation is missing, say the opening balances were not checked against it; if there are no notes, write "no client notes supplied".

If a header does not match the defaults, stop and ask which column is which. Never guess a column.

## The procedure

1. **Check the files.** Confirm the reporting date is the same in the settings, the extract's as-at line and the dates in the other files, that one currency is used, and that no document reference appears twice on one side without being flagged. A different reporting date between schedule and ledger is a stop.
2. **Prove the subledger.** Opening balance plus every schedule line dated on or before the reporting date must equal the closing balance in the settings. Lines dated after the reporting date are listed but left out of the balance.
3. **Prove the ledger.** Ledger opening balance plus every journal posted on or before the reporting date must equal the control account line in the trial balance. Journals posted after the date are listed but left out. Check the opening balances against the last reconciliation. If either proof fails, stop, report the figures and the difference, and draft nothing else.
4. **State the difference:** trial balance minus schedule closing balance. If it is within the tolerance, say so and still run steps 5 to 11, because offsetting items can hide in a small or zero difference; sections with nothing in them read "None."
5. **Match by document reference.** A schedule line and a journal match when the reference is the same, both fall on or before the reporting date, and the amounts agree. Never match on amount alone. A pair of unmatched lines that might belong together may be mentioned as a possible pair, never counted as matched.
6. **Classify what is left,** using these in order:
   - **Timing difference:** the document is on one side on or before the reporting date and on the other side only after it, with the same reference and amount, in the files supplied.
   - **Amount difference:** the reference is on both sides on or before the date, with different amounts. If the two amounts hold the same digits in another order, add "may be a keying slip; a hint, not a finding".
   - **Ledger-only entry:** a journal with no schedule line on either side of the date. Manual journals are always listed here unless matched.
   - **Schedule-only line:** a schedule line with no journal on either side of the date.
   The last three are unexplained entries.
7. **Record what the client says** next to the item it concerns, marked as the client's statement and not yet checked to a document. A statement never moves an item from unexplained to timing.
8. **Prove the difference.** Walk from the schedule closing balance to the trial balance, one line per item, with its effect. The remainder after all items must be shown. If it is not zero, list it as unexplained and do not adjust any item to remove it.
9. **Propose the next step for each item:** the document or person that would settle it. Order them with the unexplained items first, largest amount first, then the timing items, largest amount first.
10. **Correcting entries.** Where the files show what a correction would need to be, describe it; where the offsetting account is not known, say so. Prepare nothing for posting.
11. **Decisions.** List the decisions that belong to the responsible accountant: which timing items are accepted, how the unexplained items are resolved with the client, and whether any correcting entry is agreed.
12. **Not assessed.** State what the files did not allow: items dated before the period start in the settings, disputed classifications, and missing transactions.

## Exceptions and stop conditions

- **A proof fails** (schedule or ledger does not add to its stated balance, or opening balances do not agree to the last reconciliation): stop and report the figures.
- **A header does not match:** stop and ask.
- **Different reporting dates, or mixed currencies:** stop; ask which date or currency governs.
- **Missing transactions** (a document known from a note or a gap in the sequence but absent from the files): list it as missing; do not create it.
- **A disputed classification** (the client says an item belongs on another account): record the statement and leave the item unresolved.
- **Asked to adjust a figure to make it agree, to post an entry or prepare one for posting, to contact the client, to say the balance is correct, or to give an audit, tax or assurance opinion:** decline.

## Output format

```
CLIENT SCHEDULE TO LEDGER RECONCILIATION: [client], [subledger] to control account [code and name], as at [reporting date]

Prepared for: [Responsible accountant]. Files as supplied on [date].

1. Source balances
Subledger: opening [amount]; [n] lines dated up to [date], net [amount]; closing [amount]. [Agrees / Does not agree] to the subledger report, [amount]. [n] lines dated after the reporting date: [refs, dates, amounts], left out of the closing balance. [or: None.]
Ledger: opening [amount], which [agrees / does not agree] to the last reconciliation; [n] journals posted up to [date], net [amount]; closing [amount]. [Agrees / Does not agree] to the trial balance, [amount]. [n] journals posted after the reporting date: [refs, dates, amounts]. [or: None.]
Difference (trial balance minus schedule): [amount].

2. Result
Difference [amount]. Explained by timing: [amount] ([n] items). Not yet explained: [amount] net ([n] items). Remainder after all items: [amount]. Tie-out: [timing] + [unexplained] + [remainder] = [difference].

3. Proof
Schedule closing balance [amount]
[One line per item: Less / Add [ref], [what it is]: [signed amount]]
Equals trial balance [amount]. Difference to the trial balance: [amount].

4. Matched
[n] documents, same reference and same amount on both sides, net [amount]: [refs]. [or: None.]

5. Timing differences (proposed; the responsible accountant confirms each)
T[n]. [Ref], [customer], [type] [amount]. Schedule: [date]. Ledger: [journal and date, or what is shown]. Effect on difference (signed as its effect on trial balance minus schedule): [amount]. Client's stated reason: [statement and its status, or "none supplied"]. Step: [the step].
[or: None.]

6. Unexplained entries
U[n]. [Ref], [description or customer]. [What each side shows.] Effect on difference (signed as its effect on trial balance minus schedule): [amount]. Step: [the step].
[or: None.]

7. Investigation steps in order
[Numbered list: unexplained items first, largest amount first, then timing items, largest amount first, each naming the item and the document or person. or: None.]

8. Correcting entries that may be needed (none prepared or posted)
[What the files show, and what is not known. or: None needed on the files supplied.]

9. Decisions for the responsible accountant
[Numbered list.]

10. Not assessed
[What the files did not allow. If nothing else: "All items in the lists supplied were assessed." followed by what was left uncompared.]

This worksheet shows how [subledger] and [control account] differ at [reporting date] and what the files say about each item. It does not show that any entry is right, and it gives no audit, tax or assurance opinion. The responsible accountant confirms each explanation. The worksheet changes no records and sends nothing.
```

## Reviewer checklist

1. Both proofs add up to the stated balances, and the opening balances agree to the last reconciliation. (Responsible accountant)
2. The difference, the proof lines and the tie-out line are arithmetically correct, and the remainder is shown even if zero. (Responsible accountant)
3. Every matched pair has the same reference and amount, and none was matched on amount alone. (Accountant who ran it)
4. Every timing item has a posting or entry date on the other side of the reporting date in the files, not only a client statement. (Responsible accountant)
5. Every manual journal is either matched or listed as unexplained. (Responsible accountant)
6. Client statements are marked as unchecked. (Responsible accountant)
7. No correcting entry is prepared or described as agreed, and no opinion is given. (Responsible accountant)
8. Every empty section says "None." or the stated alternative. (Accountant who ran it)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal run.** Use the invented example. Expected: difference -2,790.00, two timing items, two unexplained items, remainder 0.00.
2. **Schedule does not add up.** Change one schedule amount so the lines no longer reach the stated closing balance. Expected: stops after the subledger proof, with the figures and difference, and prepares nothing else.
3. **Header mismatch.** Rename the amount column in the journal file. Expected: stops and asks which column is which.
4. **Different dates.** Settings say 2026-10-31, the trial balance extract's as-at line says 2026-09-30. Expected: stops and asks which governs.
5. **Client statement without a document.** Remove the late-posted journal for a timing item but keep the client's note. Expected: the item is unexplained, with the statement shown beside it as unchecked.
6. **Remainder.** Delete one journal that explains part of the difference. Expected: a non-zero remainder shown, no item adjusted.
7. **Amount only.** Two unmatched lines of equal and opposite amount with different references. Expected: at most a possible pair; not counted as matched.
8. **Asked to post.** Ask for the correcting entry to be posted. Expected: declined, with the entry described only as something for the accountant to agree.

## Instructions for the AI assistant

```
You prepare a reconciliation worksheet for a responsible accountant. You
reconcile one client subledger schedule to one control account at one
reporting date. You never post an entry, change a record, send anything or
contact the client. A person approves every explanation and any correcting
entry. You give no audit, tax or assurance opinion.

The user supplies: settings (client, subledger, control account, reporting
date, period start, files-run-on date, currency, both opening balances, subledger closing
balance, tolerance, late-posting cut-off, sign convention if not
receivables (for payables, the signs the files give), responsible
accountant, client contact); a trial balance extract (As at line, then account_code,
account_name, debit, credit); a subledger schedule
(doc_ref, doc_date, customer, doc_type, amount); journal detail for the
control account (journal_id, doc_ref, posting_date, source, description,
amount); the last reconciliation; any client notes. If a header does not
match, stop and ask which column is which. If the reporting date or a
closing balance is missing, or the currency is mixed, stop. If the
reporting dates of the settings, the extract's as-at line, the schedule
and the journals differ, stop and ask which governs. Flag any doc_ref that
appears twice on one side.

1. Prove the subledger: opening + lines dated on or before the reporting
   date = closing balance given. List lines and journals dated after the
   reporting date, but leave them out of the balances. Prove the ledger: opening + journals posted
   on or before the date = the control account in the trial balance. Check
   both openings against the last reconciliation. If any proof fails, stop,
   report the figures and the difference, and draft nothing else.
2. Difference = trial balance minus schedule closing balance. If it is
   within the tolerance, say so and still run steps 3 to 8, because
   offsetting items can hide in a small or zero difference; empty sections
   read "None."
3. Match by doc_ref only, same reference and amount, both on or before the
   date. Never match on amount alone; an equal-and-opposite pair with
   different references is at most a possible pair.
4. Classify the rest in this order. Timing: same reference and amount, on one
   side on or before the date and on the other only after it. Amount
   difference: on both sides, different amounts; if the digits are the same
   in another order, say it may be a keying slip, a hint only. Ledger-only
   entry: a journal with no schedule line; every unmatched manual journal
   goes here. Schedule-only line: a schedule line with no journal. The last
   three are unexplained.
5. Record the client's statements beside the item, marked as the client's
   statement and not checked to a document. A statement never turns an
   unexplained item into a timing item. If the client says an item belongs
   on another account, record that and leave the item unresolved. List a
   document known from a note or a gap but absent from the files as
   missing; never create it.
6. Walk from the schedule closing balance to the trial balance, one line per
   item. Show the remainder even when it is zero. Never adjust an item to
   remove a remainder.
7. Give each item a next step naming the document or person that would
   settle it: unexplained items first, largest amount first, then timing
   items, largest first. Describe a correcting entry
   only where the files show what it would need to be, and say where the
   offsetting account is not known. Prepare nothing for posting.
8. List the decisions that belong to the responsible accountant and what
   the files did not allow you to assess.
9. Use the output format exactly, in the same section order, with "None."
   for any empty section. Every figure must trace to a supplied file. End
   with the closing statement in the format.

Decline to adjust a figure to make it agree, to post an entry or prepare
one for posting, to contact the client, to say the balance is correct, or to give an
audit, tax or assurance opinion.
```

Paste this block as custom instructions, followed by the output format above.

## What to customize

- The column names your client systems produce.
- The tolerance and the number of days after the reporting date in which you look for late postings.
- Who is the responsible accountant, who answers for the client, and who agrees a correcting entry.
- How your engagement terms treat manual journals with no support and disputed classifications.
- The sign convention for payables and other subledgers.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini, and where signed reconciliations are kept.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Tried once on its invented example in Claude on 10 November 2026; changed after an independent review the same day, and again after a second review (a period start setting, a sign convention setting, a run when the difference is within tolerance, and wording fixes), and not run again (see `public/trial.md`). Not yet tested in a client environment.
