# Quality of earnings adjustment evidence schedule: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-11

The inputs were the template's own invented example (Company K, an invented 70-person maker of shop fittings). No client data was used. The run was made by a model that did not write the template.

## Inputs used

The seven inputs in `public/example.md`, section "The inputs": engagement settings, management's adjustment list, ledger detail, account map, management's explanations, supporting documents index and earlier questions (first run). The example's own output was not read until the run was finished. One caveat: the template's acceptance tests (in the member file) state the expected counts for this example, and they were read before the run, so the run was not blind to those counts.

## What came out

The instruction block and output format were followed exactly. Every one of the six parts was produced. The substantial parts are below. The sections for each adjustment are in the same shape as the published example.

```
QUALITY OF EARNINGS ADJUSTMENT EVIDENCE SCHEDULE: Company K, test period 2025-10-01 to 2026-09-30

Draft for: Engagement lead. Files received 2026-11-06. Currency: dollars. Run: first run.
File checks: None.

1. Management's bridge
Reported EBITDA per the financial statements: 842,600.00
A1 to A6 as listed: 90,000.00; 18,400.00; 12,500.00; 7,300.00; 11,000.00; -6,000.00
Management's adjustments, total: 133,200.00
Reported EBITDA plus management's adjustments: 975,800.00. Management's adjusted EBITDA as stated: 975,800.00. Agrees.

2. Summary by evidence status
Traced: 1, 7,300.00: A4.
Traced with flags: 1, 12,500.00: A3.
Not traced: 4, 113,400.00 net: A1, A2, A5, A6.
Total: 6, 133,200.00. Agrees to management's total, 133,200.00.
Entries cited by more than one adjustment: G-230, 3,000.00, A2 and A5.

3. Adjustments (in brief)
A1 Not traced. P-01 to P-04 = 240,000.00 in the test period. 240,000 less 150,000 recomputes to 90,000.00 (agrees); assumption 150,000.00 has no document; P-01 to P-04 each "no document". Look-back not checked (normalisation). Flags: None. Questions Q1, Q2.
A2 Not traced. G-211 + G-219 + G-230 = 18,400.00, ties. D-01 matches G-211, D-02 matches G-219, G-230 no document. Look-back: 2 entries, 9,700.00; same counterparty G-150 (Supplier L, 4,200.00). Flags: Recurs (G-150); Overlap (G-230 also in A5). Questions Q3, Q4.
A3 Traced with flags. R-301 + R-305 = 12,500.00, ties; D-03 and D-04 match. Look-back: 0 entries. Flag: Outside EBITDA (R-305, 5,000.00, account 1610 marked in_ebitda no). Question Q5.
A4 Traced. B-410 = 7,300.00, ties; D-05 matches. Look-back: 1 entry, 2,100.00, no same counterparty. Flags: None. Questions: None.
A5 Not traced. C-501 + G-230 = 11,000.00, ties. D-06 matches C-501; G-230 no document. Look-back as A2. Flags: Recurs (G-150); Overlap (G-230 also in A2). Questions Q3, Q4.
A6 Not traced. I-601 is dated 2025-09-28, outside the test period: linked entries in the test period 0.00; does not tie, difference -6,000.00. Explanation not supplied. D-07 matches I-601. Look-back: 0 entries. Flag: Outside test period. Question Q6.

4. Questions for management (draft)
Q1. (A1) What is the 150,000.00 yearly cost of a general manager based on, which document supports it, and do it and the 240,000.00 in P-01 to P-04 both include, or both exclude, employer payroll costs?
Q2. (A1) Please supply the payroll records for P-01 to P-04, 60,000.00 each.
Q3. (A2, A5) Please supply the invoice behind G-230, Supplier L, 3,000.00, 2026-03-05, and say how it divides between the distributor dispute and the sale document review. Both adjustments cite the full 3,000.00.
Q4. (A2, A5) Supplier L was also paid 4,200.00 on 2025-03-14 (G-150, "Dispute advice"). Did that relate to the same dispute, another dispute or other work?
Q5. (A3) R-305, Supplier N, 5,000.00, is posted to 1610 Leasehold improvements, outside EBITDA per the account map. Was it charged in arriving at reported EBITDA of 842,600.00, and if not, what is the 5,000.00 adjusting?
Q6. (A6) Please supply management's explanation for A6. I-601, Insurer V, -6,000.00, is dated 2025-09-28, before the test period starts. Is there an entry in the test period for these proceeds, and if not, why is the deduction made against this period?

5. Decisions for the engagement lead
1. Which of management's 6 adjustments the firm accepts, in whole or in part. The evidence status is not that decision.
2. Which questions are sent to management, and in what form.
3. A2 and A5, Recurs (G-150, 4,200.00).
4. A2 and A5, Overlap (G-230, 3,000.00).
5. A3, Outside EBITDA (R-305, 5,000.00).
6. A6, Outside test period (I-601, -6,000.00).

6. Not assessed
Adjustments management did not propose. Entries management did not cite. Whether any document is genuine. Anything outside the look-back period supplied. No check was skipped for a missing input.
```

## What was observed

- **Every required part was produced,** and the arithmetic holds: the bridge, the three status totals (7,300.00 + 12,500.00 + 113,400.00 = 133,200.00) and each tie.
- **Nothing in the template made the run stop.** No header was wrong and no input was missing. The stop conditions were not exercised.
- **No judgment, no figure of its own.** The run proposed no adjustment, stated no adjusted earnings of its own and recommended nothing. The 150,000.00 general-manager cost was treated as an unsupported assumption and turned into a question.
- **Differences from the published example.** The statuses, flags, tie results, look-back results, overlap, matched documents and the six decisions came out the same. The only difference of substance is the questions: the example has eight and this run has six. This run put two of the example's pairs into one question each (the A1 basis and support for 150,000.00; the A6 explanation and the date of I-601). The template lets one question cover several gaps, so both are allowed, but the acceptance test for this example gives a fixed count that is higher. The wording of every other line differs slightly.
- **Facts not in the inputs.** None found in this run's output. In the published example, every fact also traces to the inputs.
- **Where the instructions were ambiguous and a guess was needed:**
  - The number of questions is not fixed by the rules, yet the acceptance test for this example gives a count.
  - The look-back rule says to write "not possible" when the ledger holds no look-back entries except cited ones. It does not say what to write when the ledger holds some look-back entries but none in the adjustment's accounts (A3, A6). This run wrote "0 entries, 0.00", as the example does. The ledger is limited to accounts the adjustments cite, so a zero may mean "none" or "none supplied", and the schedule cannot tell them apart.
  - A5 raised Recurs because of G-150, which shares a counterparty with G-230, an entry A5 shares with A2. The rule says "same counterparty as a linked entry", which allows this, but a reviewer may think it counts the same fact twice.
  - A question that serves two adjustments is numbered once and listed under both. The numbering rule ("in adjustment order") does not say where it falls in that order.
  - The fenced instruction block is a shortened form of the procedure. It leaves out the exact "Stopped:" output for a stopped run, the "calculation not recomputable" handling and the rule against repeating bank details is only partly carried over. Pasted alone, it does less than the full template.
  - Step 6 uses employer payroll costs as its example of a basis mismatch, which is exactly the case in this invented example, so this example does not test whether the instruction works for other kinds of mismatch.
- **Since addressed (not re-run):** after this run, the template was revised for the look-back zero, the shared Recurs flag, the numbering of a question that serves several adjustments, the shortened instruction block, and the basis-mismatch illustration in step 6, and the output format now fixes the date style. This record shows the run as it was, before those edits; the template has not been run again.
- **Not tried:** the other eight acceptance tests (header mismatch, uncited entry, requests to give a view or to send, a second run, and so on). They remain "proposed, none run" in the template.
- **Limits.** One run, one model, one invented example. It shows the template can be followed to a complete schedule here. It does not show how it behaves on a real data room, and nothing here is tested for a client.
