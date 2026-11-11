# Client findings validation document: one trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md`: the decision brief, the evidence register and the five candidate findings. No client data was used. This is the second run. The first run found eight ambiguities; the instruction block, the output format and the example were then edited to answer them (F2 now names no decision, and the dates are written one way). This run was made by the same model that made those edits, after it had read the first record and the reviewer's points, so it is not an independent run. It followed the revised instruction block and output format in `member/template.md` and compared its output with the revised example afterwards. The first run's record is replaced by this one.

## What came out

The document had all three parts of the format, filled as follows.

- **Part A** put three findings to the client (F1, F2, F3). F1 showed three of its four items and said one was not shown. F2 was labelled single source. F3 showed its counter-evidence (E8) beside the finding.
- **Part B** gave the counts: 5 findings supplied, 3 put to the client, 1 held back, 1 not material, 5 flagged. The flags were:
  - F1: evidence withheld (E2).
  - F2: single source and wording stronger than the evidence ("Most", one counted interview, no data item).
  - F3: counter-evidence present (E8).
  - F4: reference not in register (E10), and held back, no evidence.
  - F5: item does not address the finding (E5 gives walking times, nothing about pallet wrap).
- **Figures checked:** E4 (1,184 + 1,126 = 2,310) and E7 (97 + 315 = 412) both match. No other item gives parts and a total.
- **Evidence no finding uses:** E9. F4 was not given E9 as a replacement; the lead was asked which reference was meant, and told that E9 is the only returns item and that it says nothing about Mondays.
- **Five numbered decisions** for the engagement lead, one for each flagged finding.
- **Part C** said "Not run: no replies supplied.", then printed the four summary lines (none, none, none, and "Not put to the client: F4, F5") and the closing line saying nothing had been changed or sent, as the revised format requires on a first run.
- F2's implication ended "No decision named.", because the lead left its decision blank.
- Dates were written as 17 November 2026 and 27 November 2026 throughout.

## What was observed

- Every required part was produced. Nothing in the inputs made the run stop, and no stop condition was triggered.
- **Ambiguities where a guess was needed:**
  1. Whether "n kinds" counts kinds of counted items or of shown items. Counted items were used, so F1 reads "4 items, 3 kinds; 1 not shown".
  2. Whether the "Not put to the client" lines in Part B and Part C put a held-back finding (F4) with a not-material one (F5). Both were listed in each.
  3. The first run's other ambiguities (withheld evidence as a flag, the tests on a not-material finding, a blank share, the personal-name rule, the all-evidence-withheld exception, Part C on a first run) are now answered in the block and the format, and none needed a guess in this run. The example has no blank share, no personal name and no finding whose evidence is all withheld, so those three rules were read but not exercised.
- **Differences from the example:** none in any count, flag, decision or figure. Wording of the Part B flag lines and decision questions varies slightly between the two.
- **Facts in either output that are not in the inputs:** none in the findings, evidence or figures. Both outputs add small words of their own, such as "the order-to-dispatch review" in the "What this is" line.
- **Shortcomings of this trial:** one run, by the model that edited the template, on one invented example with no replies, so Part C was not exercised. The acceptance tests in the template were not run. This does not show how the template behaves on real client material.

## Changes made after the independent review

After this run, a reviewer's minor points were applied to the template and the example. They clarify wording and do not change any count, flag, figure or decision in the example. The recorded output and observations above are unchanged. No new run was made; the revised block and format were re-read line by line against the example instead, so this is a read-through, not a third run.

- The instruction block now lists the kinds of flag and says that being marked not material is a listing, not a flag. This settles which findings count as flagged (five).
- The format notes now say that counts of items and kinds are of counted items, which settles the first ambiguity above, and that "Not put to the client" lists held-back and not-material findings together, which settles the second.
- The example's "What this is" line now writes the engagement as the brief gives it, so the small wording difference noted above no longer applies to the example. The run recorded above had written it in lower case.
- Example decision 4 now also says E9 says nothing about Mondays, as this run reported to the lead.
