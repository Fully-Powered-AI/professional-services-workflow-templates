# Trial: Client schedule to ledger reconciliation, run on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example's. The client, customers, documents and figures are all made up, and no client data was used. The run used the five inputs in `public/example.md` (settings, trial balance extract, subledger schedule, journal detail, last reconciliation and client note) and the instruction block and output format in `member/template.md`. The run was done by a model that did not write the template. The worksheet was worked out from the inputs before the example's own worksheet was read, then compared with it.

## What came out

All ten sections of the format were produced, in order, with the closing statement. Nothing in the instructions made the run stop.

- Subledger proof: opening 41,200.00 plus nine lines dated up to 31 October, net 15,070.00, gives 56,270.00, which agrees to the subledger report. One line (RCT-5540, 3 November, -1,800.00) is dated after the reporting date and was left out.
- Ledger proof: opening 41,200.00 plus ten journals posted up to 31 October, net 12,280.00, gives 53,480.00, which agrees to the trial balance. One journal (J-4411, 2 November, 2,400.00) is after the date. Opening balances agree to the last reconciliation.
- Difference (trial balance minus schedule): -2,790.00.
- Matched by reference and amount: 7 documents, net 6,130.00 (INV-3070, INV-3071, RCT-5521, INV-3080, RCT-5530, CN-0212, INV-3088).
- Timing, proposed: T1 INV-3091, -2,400.00 (schedule 30 October, ledger 2 November); T2 RCT-5540, -1,800.00 (ledger 30 October, schedule 3 November). The client's note about T2 was shown beside it as the client's statement, not checked to a document. Total -4,200.00.
- Unexplained: U1 manual journal MJ-0457, a ledger-only entry of 1,500.00; U2 INV-3077, schedule 6,540.00 against ledger 6,450.00, effect -90.00, with the "may be a keying slip; a hint, not a finding" note. Net 1,410.00.
- Remainder: 0.00. Tie-out: -4,200.00 + 1,410.00 + 0.00 = -2,790.00.
- Proof walk: 56,270.00, less 2,400.00, less 1,800.00, add 1,500.00, less 90.00, equals 53,480.00.
- Investigation order: U1 (support for MJ-0457), U2 (invoice copy), then T1 and T2.
- Correcting entries: none prepared. If the invoice copy shows 6,540.00 the ledger is 90.00 short and the offsetting account is not known from the files. Whether to reverse MJ-0457 is for the responsible accountant to agree with the client.
- Decisions listed: whether T1 and T2 are accepted as timing; how U1 and U2 are resolved; whether any correcting entry is agreed.

## What was observed

The figures, the item classes, the remainder and the tie-out matched the example's worksheet and the template's first acceptance test (difference -2,790.00, two timing items, two unexplained items, remainder 0.00). Every figure in the output traces to a line in the inputs. No fact appeared in the output that is not in the inputs. The example's closing note on the arithmetic also checks.

Where the instructions left a choice, and what was done:

- The format does not say which sign "Effect on difference" uses. It was read as the effect on trial balance minus schedule, and the proof lines carry the same signs. This worked, but the template does not say it.
- The format does not say whether the investigation steps list timing items. They were listed after the unexplained items, as the example does. The instruction says only "largest unexplained amount first".
- The order of items within the timing and unexplained sections is not stated. Largest amount first was used.
- The settings list has "files run on" while the instruction block calls the same thing a "run date". They were treated as the same.
- The "Not assessed" section refers to items "from before the opening date", but no opening date is among the settings. The start of the month (1 October 2026) was inferred. The example does the same.
- Section 10 says to write "Nothing is outstanding from the lists supplied" when nothing is unassessed, but the template never says whether a disputed or unsupported item such as MJ-0457 counts as outstanding. This run followed the example and wrote the sentence.
- "Possible pairs" are allowed by the rules, but no pair occurred, so that rule was not exercised.

Differences from the published example's worksheet are in wording only: this run listed the same seven matched documents, the same items, the same step order and the same remainder. No difference in a figure was found.

Not exercised: the stop conditions, the second to eighth acceptance tests, and any other model or product. The run shows the template works on a clean example. It does not show how it behaves when a proof fails or a header is wrong.

## Settled after the run

After an independent review on the same day, the template and example were changed and the run was not repeated. The recorded output above is as it was produced. Where the template now differs:

- "Effect on difference" is now stated as signed as its effect on trial balance minus schedule.
- Investigation steps now list unexplained items first, then timing items, each largest first.
- The settings term "files run on" is now used in the instruction block too, and "the opening date" in Not assessed now reads the start of the period the files cover.
- The closing sentence of section 10 is now "All items in the lists supplied were assessed." in place of the sentence this run used.
- The tie-out line in the example now shows the remainder term, as this run's own tie-out did.
- The trial balance extract now begins with an "As at" line, which the example's extract gained after this run; the run used the extract without it.
- After a second review: a period start setting was added (the run inferred the start of the month), as was a sign convention setting; a run within the tolerance now still matches; lines and journals after the reporting date are stated as left out in the instruction block; "propose posting" now reads "prepare for posting". The run was not repeated.
- The instruction block now states the stops on differing reporting dates, the duplicate reference check, the tolerance stop, missing transactions and disputed classifications.
