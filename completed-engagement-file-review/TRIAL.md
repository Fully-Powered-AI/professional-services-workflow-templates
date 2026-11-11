# Trial: Completed engagement file review

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5).

Date: 2026-11-10

The inputs were the invented example in `public/example.md` (settings, checklist, three engagements, file index and findings log, sections 1 to 5). No client data was used. The model was given the template's instruction block and output format, and the inputs only. It did not read the example's output until after it had produced its own. It did not write the template. It worked by hand from the text, with no tool to link rows, so the counts below are its own arithmetic.

## What came out

The full worksheet follows.

```
COMPLETED ENGAGEMENT FILE REVIEW WORKSHEET: Q4 2026 file inspection

Prepared for: Quality partner. Checklist, engagement list, file index and findings log as supplied on 10 November 2026. Engagements selected: E-2601, E-2602, E-2603.
Assumptions: applies_to is blank for C08, treated as all. A sign-off by the person who prepared the item is flagged. Closed means closed; any other status counts as open. No needs_signoff value is blank.

Count: 3 engagements, 8 checklist items. Applicable item checks 21: Evidenced 14 + Check first 4 + Missing 3 = 21. Not applicable 3. 21 + 3 = 3 engagements x 8 items = 24. File items supplied 20: linked 19, not linked 1. Prior findings supplied 5: linked 3, not linked 2.

Engagement E-2601: Client A, Review, completed 30 June 2026. Engagement partner: Partner 1.
File items supplied: 6, linked 6, not linked 0.
Item checks: applicable 7: Evidenced 4, Check first 2, Missing 1. Not applicable 1: C05.

C01 Signed engagement letter on file: Evidenced
  Found: letter, "Engagement letter Client A", dated 2 February 2026; prepared by Partner 1; signed off by Client A director on 3 February 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C02 Acceptance and independence form: Evidenced
  Found: workpaper A-10, "Acceptance and independence form", dated 4 February 2026; prepared by Manager 1; signed off by Partner 1 on 5 February 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C03 Planning memo: Check first
  Found: workpaper B-10, "Planning memo", dated 20 February 2026; prepared by Manager 1; signed off by Manager 1 on 21 February 2026.
  Flags: Own sign-off (Manager 1 prepared it and signed it off)
  Prior findings: none
  To settle:
  1. Partner 1: the same person, Manager 1, prepared and signed off B-10; was a second person's review made and where is it recorded?

C04 Completion checklist with procedures cross-referenced: Evidenced
  Found: workpaper D-10, "Completion checklist", dated 25 June 2026; prepared by Senior 1; signed off by Manager 1 on 26 June 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C06 Manager review sign-off: Evidenced
  Found: signoff R-10, "Manager review sign-off", dated 26 June 2026; preparer not recorded; signed off by Manager 1 on 26 June 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C07 Partner review sign-off: Check first
  Found: signoff R-20, "Partner review sign-off", dated 9 July 2026; preparer not recorded; signed off by Partner 1 on 9 July 2026.
  Flags: Sign-off after completion (signed off on 9 July 2026, after completion on 30 June 2026); Open prior finding (F-014, Open, action CA-22)
  Prior findings: F-014, Open, action CA-22
  To settle:
  2. Partner 1: R-20 was signed off on 9 July 2026, after the completion date of 30 June 2026; was the work reviewed before completion and where is that recorded?
  3. Engagement partner (owner named in the findings log): F-014 is open against C07 with action CA-22; has the action been completed on this file?

C08 Client acceptance of the final deliverable: Missing
  Found: nothing in the file index for workpaper F-10.
  Flags: none
  Prior findings: none
  To settle:
  4. Partner 1: where is C08, workpaper F-10, or was it never made, since the index lists nothing?

Engagement E-2602: Client B, Advisory, completed 14 August 2026. Engagement partner: Partner 2.
File items supplied: 7, linked 6, not linked 1.
Item checks: applicable 7: Evidenced 5, Check first 1, Missing 1. Not applicable 1: C04.

C01 Signed engagement letter on file: Evidenced
  Found: letter, "Engagement letter Client B", dated 2 March 2026; prepared by Partner 2; signed off by Client B director on 4 March 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C02 Acceptance and independence form: Evidenced
  Found: workpaper A-10, "Acceptance and independence form", dated 5 March 2026; prepared by Manager 2; signed off by Partner 2 on 6 March 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C03 Planning memo: Evidenced
  Found: workpaper B-10, "Planning memo", dated 12 March 2026; prepared by Manager 2; signed off by Partner 2 on 13 March 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C05 Work programme for the advisory deliverable: Check first
  Found: workpaper D-20, "Advisory work programme", dated 5 August 2026; prepared by Senior 2; sign-off not recorded.
  Flags: Sign-off absent (signer and date both blank); Open prior finding (F-011, Open, action CA-19)
  Prior findings: F-011, Open, action CA-19
  To settle:
  5. Partner 2: who signed off D-20 and when? The index lacks both the signer and the date.
  6. Manager 2 (owner named in the findings log): F-011 is open against C05 with action CA-19; has the action been completed on this file?

C06 Manager review sign-off: Evidenced
  Found: signoff R-10, "Manager review sign-off", dated 10 August 2026; preparer not recorded; signed off by Manager 2 on 10 August 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C07 Partner review sign-off: Missing
  Found: nothing in the file index for signoff R-20.
  Flags: none
  Prior findings: none
  To settle:
  7. Partner 2: where is C07, signoff R-20, or was it never made, since the index lists nothing?

C08 Client acceptance of the final deliverable: Evidenced
  Found: workpaper F-10, "Client acceptance of final deliverable", dated 14 August 2026; prepared by Senior 2; signed off by Partner 2 on 14 August 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

Engagement E-2603: Client C, Review, completed 30 September 2026. Engagement partner: Partner 1.
File items supplied: 7, linked 7, not linked 0.
Item checks: applicable 7: Evidenced 5, Check first 1, Missing 1. Not applicable 1: C05.

C01 Signed engagement letter on file: Missing
  Found: nothing in the file index for letter.
  Flags: none
  Prior findings: F-012, Closed, action CA-20
  To settle:
  8. Partner 1: where is C01, the engagement letter, or was it never made, since the index lists nothing?

C02 Acceptance and independence form: Evidenced
  Found: workpaper A-10, "Acceptance and independence form", dated 6 April 2026; prepared by Manager 3; signed off by Partner 1 on 7 April 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C03 Planning memo: Check first
  Found: workpaper B-10, "Planning memo", dated 14 April 2026; prepared by Manager 3; signed off by Partner 1 on 15 April 2026.
  Found: workpaper B-10, "Planning memo revised", dated 12 May 2026; prepared by Manager 3; signed off by Partner 1 on 13 May 2026.
  Flags: More than one match (two rows link to B-10)
  Prior findings: none
  To settle:
  9. Partner 1: which of the two B-10 items, "Planning memo" or "Planning memo revised", is the one for the file?

C04 Completion checklist with procedures cross-referenced: Evidenced
  Found: workpaper D-10, "Completion checklist", dated 24 September 2026; prepared by Senior 3; signed off by Manager 3 on 25 September 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C06 Manager review sign-off: Evidenced
  Found: signoff R-10, "Manager review sign-off", dated 25 September 2026; preparer not recorded; signed off by Manager 3 on 25 September 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C07 Partner review sign-off: Evidenced
  Found: signoff R-20, "Partner review sign-off", dated 29 September 2026; preparer not recorded; signed off by Partner 1 on 29 September 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C08 Client acceptance of the final deliverable: Evidenced
  Found: workpaper F-10, "Client acceptance of final deliverable", dated 30 September 2026; prepared by Senior 3; signed off by Partner 1 on 30 September 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

Missing evidence
E-2601 C08, workpaper F-10: nothing listed. Engagement partner Partner 1.
E-2602 C07, signoff R-20: nothing listed. Engagement partner Partner 2.
E-2603 C01, letter: nothing listed. Engagement partner Partner 1.

Sign-offs absent
E-2602 C05, workpaper D-20: signer and date not recorded.

File items not linked to any checklist item: E-2602, workpaper X-50, "Client correspondence index" (no checklist item has this kind and reference).

Prior findings not linked to any checklist item: F-016, E-2603, Open, "Retention date not recorded on the file" (item_id is blank), action CA-24; F-009, E-2599, Closed, "Planning memo not updated after scope change" (its engagement is not in the selection), action CA-17.

Decisions for the Quality partner
1. Findings to confirm: E-2601 C03, C07, C08; E-2602 C05, C07; E-2603 C01, C03.
2. Prior findings to attach to an item or an engagement: F-016, F-009.
3. File items to place against a checklist item, or to leave out of the checklist: E-2602 workpaper X-50.
4. Remediation for each confirmed finding: who acts, and by when.

This worksheet, built from the lists supplied for Q4 2026 file inspection, shows what the file index lists against the firm's checklist. It does not show that any item's content is right, that a sign-off was properly given, or that any engagement complies with professional standards. The quality partner confirms findings and the engagement partner answers questions about the file. The worksheet changes no file and sends nothing.
```

## What was observed

- **Every required part was produced:** the title, "Prepared for" line, assumptions, count line, three engagement blocks with every applicable item in checklist order, missing evidence, sign-offs absent, unlinked file items, unlinked findings, the four decisions and the closing paragraph. The counts tied out (21 applicable checks, 14 + 4 + 3; 3 not applicable; 24 in all; 20 file items, 19 linked; 5 findings, 3 linked). Nine questions to settle were numbered continuously, each naming who answers. The model was never told to stop, and no stop condition applied.
- **Against the published example:** the same results, flags, questions, counts and lists, item for item. The differences were wording only. The example's Assumptions line names just the blank `applies_to` on C08; this run also listed the settings' defaults (preparer sign-offs flagged, "Closed" means closed) and noted that no `needs_signoff` was blank. This run printed the status and action reference inside the Open prior finding flag (for example "F-014, Open, action CA-22"); the example gives only the finding id there and the rest on the Prior findings line. This run wrote the question for a Missing item as "where is C08, workpaper F-10", the example "where is workpaper F-10". As the example then stood, it put a full stop after each flag; this run used semicolons. The example's unlinked-finding reason for F-016 is "no checklist item named", this run's "item_id is blank". As the example then stood, decision 3 read "E-2602 X-50" and "E-2602 workpaper X-50" here.
- **Facts not in the inputs:** none found in either output. Every name, date, reference, status and action reference traces to an input row. The example's reason "no checklist item named" is an interpretation of a blank field, not a new fact.
- **Reviewer checklist, items 1 to 8:** all held on this output (counts tie, items in order, Found lines match the index, nothing linked by title, flags true including the same-day rule for E-2602 and E-2603 F-10, findings linked only by engagement and item, every question names who answers, no word of complete, compliant or passed). Item 9 is for the engagement partners and was not testable.

## Ambiguities and shortcomings in the template

- **Blank reference.** The Found line, the Missing line, the Missing evidence list and the questions are written as "[kind] [ref]", but the letter has a blank reference. The template does not say how to print that. This run wrote "letter" and the example does the same, but the Missing question and Decisions line 3 then differ in form.
- **Open finding on a Missing item.** Flags are raised "only on linked rows", but findings link to items, not rows. If an open finding sits against an item that is Missing, the instructions raise no flag and no question for its owner, yet the item's Prior findings line would show it. The example only has a closed finding in that position. The reader is left to guess.
- **Owner named as a role.** F-014's owner in the log is "Engagement partner", not a name. The template says the owner in the log answers; the example and this run wrote "Engagement partner (owner of F-014)", although the engagement partner is known to be Partner 1. Either is defensible; the template does not choose.
- **Order of several flags on one item**, and whether each flag gets its own question when one item has two (it does, per step 7), is clear only from the example. The order (absent, own, after completion, more than one, open finding) is implied by the order of step 4, not stated.
- **Assumptions line.** The output format gives only the blank-field example. Whether the settings' defaults belong there is not said; this run added them, the example did not.
- **Count line.** "[n] + [n] = [n] engagements x [n] items = [n]" reads as a chain of equals and is awkward to follow from the format alone; the example shows the intended shape.
- **Own sign-off on a signoff row.** Where `prepared_by` is blank, which is every signoff row in the example, the rule cannot fire. This is correct by the text but is nowhere stated, and a reader may wonder if it was skipped.
- **Own sign-off versus a client signer.** Nothing says what to do when the signer is outside the firm, as on engagement letters. It did not matter here.
- **Decision 3** asks for "engagement id and reference", with no kind; the example gives a bare reference and this run added the kind.
- **Version notes and the acceptance tests** still say the template has not been tried; they will need a line saying it has now been tried once on its invented example.
- **Limits of this trial:** one run, one model, one product, on a small invented set. Only some of the fifteen proposed acceptance tests are exercised by the example (missing letter, absent sign-off, own sign-off, after-completion, two rows, non-applicable item, open and closed finding, unlinked finding, blank `applies_to`). The stop conditions, declined requests, blank completion date and renamed header were not tried. The model held the whole task in its head and could not check its arithmetic with a tool; it agreed with the example, but a longer file index would be more error-prone.

## After this run

Added after the run above, which is left as recorded. The template's instruction block, output format and example were then clarified on points this trial raised: an open prior finding on a Missing item now raises its flag and a question for its owner; Own sign-off needs both names filled; the settings' defaults are in the instruction block; a blank reference prints as the kind alone; flags are separated by semicolons in a stated order; decision 3 gives the kind with the reference; defaults for settings the person supplied are not listed under Assumptions; and the summary no longer says an open finding answers a checklist item. The example's flag separators and decision 3 were changed to match. The template was not run again after these changes. A later pass, after an independent review, made these further wording changes without running the template again: the count line now reads "Applicable 21 + not applicable 3 = 24, which is 3 engagements x 8 items" (the run above printed the older chain of equals); the instruction block now carries the six question wordings and the three reasons a file row is not linked; and a stray full stop after one flag in the example was removed. None changes a result in the example.
