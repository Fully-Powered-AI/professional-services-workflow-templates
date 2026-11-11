# Trial: Client document request tracker, run on its invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). The assistant that ran this trial is the one that revised the template after an earlier trial and a review, so it knew the template and the example; this is not a run by a fresh reader. An earlier run on 10 November 2026, made by a different assistant before the revisions, found that the example's follow-up draft broke the template's own rules and that the pasted instructions had left out several rules. Those were fixed, and this is the second run, on the revised text.

Date: 2026-11-10

The inputs are the invented example in `public/example.md` (an invented accounting practice and its invented client, Client A). No client data was used.

## Inputs used

All five inputs from "The inputs" in `public/example.md`: the engagement settings, the eleven-row request list, the seven-file delivery log, the two client messages (one email, one call note), and the note that no previous status list exists. The instruction block and output format from `member/template.md` were applied as written.

## What came out

```
CLIENT DOCUMENT REQUEST TRACKER: Quarter-three records, Client A

For: Engagement manager. Client: Client A. Check date: Tuesday 10 November 2026. Reply requested by: Friday 13 November 2026.
Supplied: request list (11 rows, 10 required); delivery log (7 files); client messages (2); previous status list (not supplied).

Position: required rows 10: 3 Received, 3 Incomplete, 2 Mentioned only, 2 Missing. Optional rows 1: 0 Received, 0 Incomplete, 1 Mentioned only, 0 Missing. Received means usable files cover the period; it is not a judgment that they are sufficient.

Request list by document

Operating account bank statement
R01, 1 to 31 July 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F01. F01 covers 1 July to 20 August 2026.
R02, 1 to 31 August 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F01. F01 covers 1 to 20 August 2026. Not covered: 21 to 31 August 2026, 11 days. Overdue by 4 days.
R03, 1 to 30 September 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F02 (not counted: unreadable). F02 is logged as not readable; note: "Opens blank after page 1". Overdue by 4 days.

Payroll register
R04, 1 to 31 July 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F03. F03 covers 1 to 31 July 2026.
R05, 1 to 31 August 2026. Required. Due Friday 6 November 2026. Status: Missing. Files: none. No message mentions August. Overdue by 4 days.
R06, 1 to 30 September 2026. Required. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Email from the finance manager at Client A, Thursday 5 November 2026: the September register will come on Thursday 12 November 2026. Overdue by 4 days.

Receivables aging report
R07, 30 September 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F05. F05 covers 30 September 2026. Total shown 209,330.00; total expected 212,480.00; difference 3,150.00, shown lower. Overdue by 4 days.

Term loan statement
R08, 1 July to 30 September 2026. Required. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Email from the finance manager at Client A, Thursday 5 November 2026: the lender statement for the term loan comes through the bank contact, who has been asked; no date given. Overdue by 4 days.

Trial balance
R09, 1 July to 30 September 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F06. F06 covers 1 July to 30 September 2026.

Insurance schedule
R10, 30 September 2026. Optional. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Call note, Monday 9 November 2026, reporting the finance manager: the broker holds the current insurance schedule; no date given. Overdue by 4 days.

Fixed asset additions listing
R11, 1 July to 30 September 2026. Required. Due Friday 20 November 2026. Status: Missing. Files: none. Due in 10 days.

Received but not requested
F07, vehicles list final v2.xlsx, Vehicle list, 1 January to 30 September 2026, received Monday 9 November 2026

Files that match no requested row
F04, ClientA_Payroll-register_2025-08.xlsx, Payroll register, 1 to 31 August 2025, received Wednesday 4 November 2026, period shares no day with any requested payroll period

File names that break the naming rule
F07, vehicles list final v2.xlsx: one part, not three; no underscores

Changed since the last update
no previous list supplied

Follow-up draft (not sent)
Thank you for the 7 files received between Tuesday 3 November and Monday 9 November 2026. We are still waiting on the items below:
- Operating account bank statement, 21 to 31 August 2026: the file received covers 1 to 20 August.
- Operating account bank statement, 1 to 30 September 2026: the file received will not open, please resend.
- Payroll register, 1 to 31 August 2026: no file received for this period.
- Payroll register, 1 to 30 September 2026: we understand it will follow on Thursday 12 November.
- Receivables aging report, 30 September 2026: the file shows a total of 209,330.00 against 212,480.00 expected, a difference of 3,150.00.
- Term loan statement, 1 July to 30 September 2026: we understand it is being requested through your bank contact.
Please send these items, or let us know of any delay, by Friday 13 November 2026.
[Engagement manager]

Not in the draft
R10, optional row
R11, not yet due (due in 10 days)

For the Engagement manager to decide: 6
1. Approve, change or hold the follow-up draft.
2. R02: the bank statement covers 1 to 20 August 2026 and 21 to 31 August did not arrive. Start on what arrived, or wait for the rest?
3. R07: total shown 209,330.00 against 212,480.00 expected. Start on what arrived, or wait for the rest?
4. R01, R04 and R09 are Received. Are the files sufficient?
5. F04, a payroll register for August 2025, matches no requested row. Ask the client about it, or set it aside?
6. F07, a vehicle list, is not on the request list. Ask the client about it, or set it aside?

Prepared for the Engagement manager's approval. Nothing has been sent to the client, filed or changed.
```

## What was observed

- Every part of the output format was produced. Nothing in the inputs triggered a stop condition: the headings matched, no identifier repeated, every date and amount was well formed, and there was no password or similar secret.
- Statuses, counts (10 required rows: 3 Received, 3 Incomplete, 2 Mentioned only, 2 Missing; 1 optional row Mentioned only), overdue counts, the 11 uncovered days, the 3,150.00 difference, the two unplaced files and the six decisions were rechecked before the output was returned. The output matches the published example in states and figures; the example was revised to match the rules and this run agrees with it.
- The follow-up draft has no subject line or greeting, asks for nothing that is not on the request list, offers no cause for the 3,150.00 difference and does not say what the items are for. Timing appears only on rows that are not Received. Received rows carry only the period each listed file covers.
- Facts used that rest on a reading of the inputs: the email's "lender statement for the term loan" was treated as an unmistakable short form of "Term loan statement" (it uses every word of the name); the call note's "the broker holds the current insurance schedule" was treated as a statement that the document exists, attributed to the finance manager as the person the note says spoke; the email's "Payroll for September ... the September register" was treated as naming the payroll register for September, since it uses both words of the name and a period.
- Decisions about unplaced files follow log order (F04, then F07), as the revised procedure says. The file count in the thanks line counted all seven logged files, as the revised procedure says.
- F06, named for 2026-09 but covering 1 July to 30 September, was not flagged by the naming check, because the revised procedure checks only the parts the rule names and how they are separated.
- Where the instructions are still thin: the test for an unmistakable short form is a word test, so a message that names a document in words that match its name but in a looser sense would pass; whether "a statement that it exists" covers "the broker holds it" remains a reading. Nothing told the assistant to stop, and it opened no file, sent nothing and contacted no one.
- This run does not cover the 20 proposed acceptance tests in the template, only the example.
