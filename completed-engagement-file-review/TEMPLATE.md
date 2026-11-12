# Completed engagement file review

Workflow template, version 0.1.0.

## Purpose

Prepare the worksheet a quality partner uses to test finished engagement files against the firm's own checklist. For each selected engagement, every applicable checklist item is linked to the engagement letter, workpaper or sign-off that answers it, with the file's sign-off details, any open finding from an earlier inspection and the question for the engagement partner. Missing evidence and absent sign-offs are listed across all the files. The assistant prepares the worksheet from four lists the person supplies. It opens no file, judges no content, decides nothing about compliance with professional standards, recreates no sign-off, contacts no one and changes no record. The quality partner confirms findings and assigns remediation.

## When to use it and when not to

Use it when the engagements for inspection have been chosen and the file index of each can be exported. Run it again after the engagement partners have answered, with the corrected file index.

Do not use it:

- to answer an outside audit's request list from a document register (use the audit evidence index);
- to brief senior leaders on quality measures (use the quality management review pack);
- to draw lessons from how an engagement went (use the project lessons review);
- to judge whether the work in a file is sound, whether an opinion was right or whether any engagement meets professional standards. Those are for the people who hold the responsibility;
- to review the legal or technical substance of any matter or project. For a law firm it covers the administrative contents of a closed file only;
- to design the checklist. The firm writes it; the workflow template tests files against it.

## Roles

- **Runs it:** the practice administrator, or the quality partner.
- **Reviews the worksheet, confirms which results are findings and assigns remediation:** the quality partner.
- **Answers the questions about a file and resolves them:** the engagement partner named for that engagement.
- **Owns an earlier finding and its corrective action:** the owner named in the findings log.

## Inputs

Four lists and a few settings. Each list is a table with a header row. The assistant expects these default headers and reads nothing else into them. If a header differs, is missing or is not recognised, the assistant stops and asks which column is which before it does anything else. Dates are written year-month-day.

1. **The checklist.** Headers: `item_id`, `item_text`, `evidence_kind`, `ref`, `needs_signoff`, `applies_to`.
   - `evidence_kind` is `letter`, `workpaper` or `signoff`. Any other value: stop and ask.
   - `ref` is the reference the firm's file standard gives the item. It is blank for the engagement letter.
   - `needs_signoff` is `yes` or `no`. A blank counts as `yes`, and the worksheet says so. An item of kind `signoff` always needs one.
   - `applies_to` is `all` or a list of engagement types separated by semicolons. A blank counts as `all`, and the worksheet says so.
   - If the list is missing, stop.
2. **The engagements selected.** Headers: `engagement_id`, `client_code`, `engagement_type`, `completion_date`, `engagement_partner`. If the list is missing, stop. A blank `completion_date` is allowed; the worksheet then does not compare sign-off dates for that engagement and says so.
3. **The file index.** One row for each item the file holds. Headers: `engagement_id`, `kind`, `ref`, `title`, `prepared_by`, `item_date`, `signed_off_by`, `signoff_date`. `kind` is `letter`, `workpaper` or `signoff`. If the list is missing, stop. An engagement with no rows is still checked: every applicable item is Missing, and the worksheet says that no file items were supplied for it.
4. **The findings log from earlier inspections.** Headers: `finding_id`, `engagement_id`, `item_id`, `finding_text`, `status`, `owner`, `action_ref`. If it is missing, write "Prior findings not supplied" in place of each Prior findings line and in the section on unlinked findings.
5. **Settings.** The inspection name, today's date, the quality partner's role, whether a sign-off by the person who prepared the item is flagged (default: flagged), and which status means a finding is closed (default `Closed`; any other status counts as open). If the inspection name is missing, stop.

The assistant works from files and notes the person supplies. It needs no connection to the document system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers and that dates are readable. Confirm that `item_id` values are unique in the checklist, `engagement_id` values are unique in the engagement list and `kind` values are among the three allowed. Stop on any failure and name the rows.
2. **Decide which items apply.** For each selected engagement, an item applies when `applies_to` is `all`, blank, or lists that engagement's type (compare without regard to capitals). An item that does not apply is listed once in the engagement's header and checked no further.
3. **Link file items to checklist items.** A file row links to an applicable item when it has the same `engagement_id`, the same `kind` and the same `ref` (a blank reference matches only a blank reference). Never link by title, by date or by a guess from the wording. Several rows can link to one item. A row that links to nothing is listed at the end with its reason: no checklist item has this kind and reference; only an item that does not apply to this engagement matches it; or its engagement is not in the selection.
4. **Raise flags.** A flag is a question for a person, not a finding. The first four are raised only on linked rows. Open prior finding is raised on the item, once findings are linked in step 5, whether or not any row links, so a Missing item can carry it. When one item has several flags, list them in the order below.
   - **Sign-off absent:** the item needs a sign-off and `signed_off_by` or `signoff_date` is blank. Say which is missing.
   - **Own sign-off:** `prepared_by` and `signed_off_by` are both filled and are the same name, and the settings say to flag it. Nothing changes when the signer is outside the firm, as on an engagement letter: only the two names are compared.
   - **Sign-off after completion:** `signoff_date` is later than the engagement's `completion_date`. The same day is not flagged. Skip the flag when the completion date is blank, and say so.
   - **More than one match:** two or more rows link to the same item. Show every row.
   - **Open prior finding:** a finding links to the item and its status is not the closed status.
5. **Link prior findings.** A finding links to an item only when its `engagement_id` and `item_id` equal that engagement's and that item's, and the item applies to the engagement. Print its status and `action_ref` as given. Never say whether the action worked. A finding with a blank `item_id`, an unknown item, an engagement not in the selection or an item that does not apply goes to the unlinked list with its reason.
6. **Give each applicable item one result.**
   - **Evidenced:** at least one row links and no flag is raised.
   - **Check first:** at least one row links and at least one flag is raised.
   - **Missing:** no row links. If an open prior finding is linked to it, the item stays Missing and shows that flag too.
   A Missing item is never softened because a similar title exists elsewhere in the index.
7. **Write the questions to settle.** One numbered line for each Missing item and each flag, numbered continuously from the first engagement to the last, in engagement order and then checklist order. Each names who answers. The engagement partner answers for Missing, Sign-off absent, Own sign-off, Sign-off after completion and More than one match. The owner named in the findings log answers for an Open prior finding, printed as written in the log, even if it is a role, followed by "(owner of [finding id])" ("owner not recorded" when blank). Use these questions, with the facts filled in:
   - Missing: where is the item, or was it never made, since the index lists nothing.
   - Sign-off absent: who signed it off and when, naming what the index lacks.
   - Own sign-off: the same person prepared and signed it; was a second person's review made and where is it recorded.
   - Sign-off after completion: it was signed off on one date, after the completion date; was the work reviewed before completion and where is that recorded.
   - More than one match: which of the listed items is the one for the file.
   - Open prior finding: the finding is open against this item with its action reference; has the action been completed on this file.
8. **Count and tie out.** For each engagement, Evidenced + Check first + Missing equals the number of applicable items, and applicable + not applicable equals the number of checklist items. Across the worksheet, applicable plus not applicable equals engagements times checklist items. Count the file rows supplied, linked and not linked, and the findings supplied, linked and not linked. A row linked to two items counts once as linked. If anything fails to add up, stop and report the figures.
9. **List the missing evidence and the absent sign-offs** across all engagements, with the engagement partner for each.
10. **Close.** List the decisions for the quality partner and print the closing paragraph. Return the worksheet to the person who started the work only.

## Exceptions and stop conditions

- **A header is missing, renamed or unknown:** stop and ask which column is which. Do not guess.
- **A duplicate `item_id` or `engagement_id`, an unreadable date, or a `kind` or `evidence_kind` outside the three allowed:** stop and name the rows.
- **The checklist, engagement list, file index or inspection name is missing:** stop.
- **A checklist item asks for a judgment about the content of the work, such as "analysis is appropriate":** do not test it. List it as "not testable from the file index" in the engagement's header and tell the quality partner.
- **Asked to say a file is complete, compliant, passes or is acceptable:** decline. State what is linked and what is missing, and leave the judgment to the quality partner.
- **Asked to create, fill in, backdate or assume a missing sign-off, or to treat a similar file as the missing one:** decline. An absent sign-off is shown as absent.
- **Asked to open a file, read a workpaper, or say what it shows:** decline. The worksheet uses the supplied fields only.
- **Asked to contact an engagement partner, send the worksheet, or change the file, the index or the findings log:** decline. A person does that.
- **The lists contain a password, a login code or client confidential detail beyond a client code:** do not repeat it in the worksheet; tell the person to remove it from the source.

## Output format

```
COMPLETED ENGAGEMENT FILE REVIEW WORKSHEET: [inspection name]

Prepared for: [quality partner role]. Checklist, engagement list, file index and findings log as supplied on [date]. Engagements selected: [ids].
Assumptions: [each default applied, such as "applies_to is blank for C08, treated as all", and any setting the person did not supply, such as "sign-off by the preparer flagged (default)"; a setting the person supplied is not an assumption] / none.

Count: [n] engagements, [n] checklist items. Applicable item checks [n]: Evidenced [n] + Check first [n] + Missing [n] = [n]. Not applicable [n]. Applicable [n] + not applicable [n] = [n], which is [n] engagements x [n] items. File items supplied [n]: linked [n], not linked [n]. Prior findings supplied [n]: linked [n], not linked [n].

Engagement [engagement_id]: [client_code], [engagement_type], completed [date] / completion date not recorded. Engagement partner: [name].
File items supplied: [n], linked [n], not linked [n]. [No file items were supplied for this engagement.]
Item checks: applicable [n]: Evidenced [n], Check first [n], Missing [n]. Not applicable [n]: [item ids] / none. [Not testable from the file index: [item ids].] [Completion date not recorded: sign-off dates not compared.]

[item_id] [item_text]: [Evidenced | Check first | Missing]
  Found: [kind] [ref], "[title]", dated [date]; prepared by [name] / preparer not recorded; signed off by [name] on [date] / sign-off not recorded / sign-off not required.
  (flags are separated by semicolons, in the order of step 4; Open prior finding can appear on a Missing item)
  (repeat the Found line for each row that links; a Missing item reads "Found: nothing in the file index for [kind] [ref].")
  Flags: [flag name (the facts); ...] / none
  Prior findings: [finding id, status, action [action_ref]; ...] / none
  To settle: nothing / the numbered lines, one for each Missing item and each flag, each naming who answers

(repeat the item block for every applicable item, in checklist order, and the engagement block for every engagement, in list order)

Missing evidence
[engagement id] [item id], [kind] [ref]: nothing listed. Engagement partner [name]. (or "None.")

Sign-offs absent
[engagement id] [item id], [kind] [ref]: [signer not recorded / date not recorded / signer and date not recorded]. (or "None.")

File items not linked to any checklist item: [engagement id, kind, ref, "title" (reason); ...] (or "None.")

Prior findings not linked to any checklist item: [finding id, engagement id, status, "finding text" (reason), action [action_ref] / action not recorded; ...] (or "None.")

Decisions for the [quality partner role]
1. Findings to confirm: [engagement id and the item ids that are Missing or Check first; ...] (or "None.")
2. Prior findings to attach to an item or an engagement: [finding ids] (or "None.")
3. File items to place against a checklist item, or to leave out of the checklist: [engagement id, kind and reference; ...] (or "None.")
4. Remediation for each confirmed finding: who acts, and by when.

This worksheet, built from the lists supplied for [inspection name], shows what the file index lists against the firm's checklist. It does not show that any item's content is right, that a sign-off was properly given, or that any engagement complies with professional standards. The quality partner confirms findings and the engagement partner answers questions about the file. The worksheet changes no file and sends nothing.
```

Write dates as day, month name, year. Print the quality partner setting exactly as given after "Prepared for" and in the decisions heading. Where "[kind] [ref]" is written and the reference is blank, as for the engagement letter, print the kind alone ("letter"), with no trailing space or dash.

## Reviewer checklist

1. The counts tie out, and the number of engagements and checklist items matches the lists supplied. (Quality partner)
2. Every applicable item appears once for each engagement, in checklist order, and each not-applicable item is named in the engagement's header. (Practice administrator)
3. Each Found line matches its row in the file index, with the same reference, date and names. (Practice administrator)
4. No item has been linked by title or by guess, and no similar item has been treated as a missing one. (Quality partner)
5. Every flag is true on the supplied dates and names, and the same-day rule has been applied as stated. (Quality partner)
6. Each earlier finding is linked only by an explicit engagement and item, and nothing says whether its action worked. (Quality partner)
7. Every question to settle names the person who answers. (Quality partner)
8. Nothing in the worksheet says complete, compliant, passed or acceptable, and no sign-off has been filled in. (Quality partner)
9. The engagement partners have looked at the files themselves and confirmed what the index says. (Engagement partners)

## Acceptance tests

Proposed tests. The one trial on the invented example exercised some of them (see its record); the rest have not been run.

1. **Clean file.** Every applicable item has one row with a signer and a date, none after completion. Expected: all Evidenced, nothing to settle, counts tie.
2. **Missing letter.** No letter row for an engagement. Expected: the letter item is Missing, with "nothing in the file index for letter", and appears under Missing evidence with the engagement partner.
3. **Absent sign-off.** A workpaper row with blank signer and date. Expected: Check first, Sign-off absent naming both, listed under Sign-offs absent, and nothing filled in.
4. **Signer but no date.** Expected: Sign-off absent naming the date only.
5. **Own sign-off.** The preparer and the signer are the same name. Expected: flagged when the setting says so, not flagged when it does not.
6. **Sign-off after completion.** Signed off one day after the completion date, and another signed off on the completion date. Expected: the first flagged, the second not.
7. **Blank completion date.** Expected: no date flag for that engagement, and the header says sign-off dates were not compared.
8. **Two rows for one reference.** Expected: both shown, More than one match, Check first, and a question asking which is the one for the file.
9. **Item that does not apply.** An advisory-only item on a review engagement. Expected: named as not applicable, not counted as Missing; a file row matching only it is listed as not linked with that reason.
10. **Open finding and closed finding.** Expected: the open one raises a flag and a question to its owner; the closed one is printed under Prior findings and raises nothing. Repeat with the open finding against an item that is Missing: the item stays Missing, shows the flag, and the owner gets a question.
11. **Finding with no item, and a finding for an engagement outside the selection.** Expected: both unlinked, each with its reason, and offered to the quality partner to attach.
12. **Header changed.** A file index column renamed. Expected: stops and asks which column is which.
13. **Asked if the file passes.** "Is this file compliant?" Expected: declines, states what is linked and missing.
14. **Asked to fill in a sign-off.** "Mark R-20 as signed by the partner." Expected: declines; the sign-off stays absent.
15. **Blank applies_to and blank needs_signoff.** Expected: treated as all and as yes, and each stated under Assumptions.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a completed engagement file review worksheet for the
quality partner. You test the file index of each selected engagement
against the firm's checklist. You never open or judge a file, never say
a file is complete, compliant or acceptable, never create or fill in a
sign-off, never contact anyone, and never send, change or move a record.
A person approves anything that is sent or changed; the quality partner
confirms findings and assigns remediation.

The user will supply four lists with header rows (checklist; engagements
selected; file index; findings log from earlier inspections) and
settings: inspection name, today, quality partner role, whether a
sign-off by the preparer is flagged (default: flagged) and which status
means a finding is closed (default: Closed; any other status counts as
open).
Expected headers: checklist item_id, item_text, evidence_kind, ref,
needs_signoff, applies_to; engagements engagement_id, client_code,
engagement_type, completion_date, engagement_partner; file index
engagement_id, kind, ref, title, prepared_by, item_date, signed_off_by,
signoff_date; findings finding_id, engagement_id, item_id, finding_text,
status, owner, action_ref. If a header differs or is missing, stop and
ask which column is which. If the checklist, engagement list, file index
or inspection name is missing, stop. Stop on a duplicate id, an
unreadable date or a kind other than letter, workpaper or signoff. If
the findings log is missing, write "Prior findings not supplied" where
findings would appear.

1. An item applies to an engagement when applies_to is all, blank, or
   lists the engagement type. Blank applies_to counts as all and blank
   needs_signoff counts as yes; state each under Assumptions. A signoff
   item always needs a sign-off. List items that do not apply once in
   the engagement header.
2. Link a file row to an applicable item only when engagement_id, kind
   and ref are all equal (a blank ref matches only a blank ref). Never
   link by title, date or guess. List rows that link to nothing, with
   the reason: no checklist item has that kind and reference; only an
   item that does not apply matches it; or its engagement is not in
   the selection.
3. Flags, listed in this order, separated by semicolons: Sign-off
   absent (needed, and signer or date blank; say which); Own sign-off
   (prepared_by and signed_off_by both filled and the same name, if the
   setting says so, whoever the signer is); Sign-off after completion
   (signoff_date later than completion_date; the same day is fine; skip
   if the completion date is blank and say so); More than one match
   (show every row). These four apply to linked rows only. Open prior
   finding (a linked finding whose status is not the closed status)
   applies to the item whether or not any row links, so a Missing item
   can carry it.
4. Link a finding only when engagement_id and item_id both match an
   applicable item. Print status and action as given and never say if
   the action worked. Others go to the unlinked list with a reason.
5. Result per item: Evidenced (linked, no flag); Check first (linked,
   at least one flag); Missing (nothing linked; it stays Missing even
   with an open prior finding). Never soften a Missing item because a
   similar title exists.
6. Number one question to settle for each Missing item and each flag
   (including Open prior finding on a Missing item), continuously
   across the worksheet. The engagement partner answers all but Open
   prior finding, which goes to the finding's owner as written in the
   log, followed by "(owner of [finding id])". Word the questions so:
   Missing: where is the item, or was it never made; the index lists
   nothing. Sign-off absent: who signed it off and when; name what the
   index lacks. Own sign-off: the same person prepared and signed it;
   was a second person's review made and where is it recorded. Sign-off
   after completion: signed off on [date], after the completion date;
   was the work reviewed before completion and where is that recorded.
   More than one match: which of the listed items is the one for the
   file. Open prior finding: open against this item with its action
   reference; has the action been completed on this file.
   Never answer a question yourself.
7. Tie out: per engagement, Evidenced + Check first + Missing equals
   applicable items, and applicable + not applicable equals checklist
   items; overall, applicable + not applicable equals engagements times
   items. Count file rows and findings, linked and not linked. If
   anything fails, stop and report the figures.
8. Use the output format exactly, with dates as day, month name, year.
   Print "None." for an empty list, "nothing" for no questions, and
   keep the closing paragraph. Print the quality partner setting
   exactly as given. Where "[kind] [ref]" is written and ref is blank,
   print the kind alone ("letter"). Decision 3 names engagement id,
   kind and reference. Under Assumptions state each blank-field default
   and any setting the user did not supply; a setting the user supplied
   is not an assumption.

Use only the supplied fields. A checklist item that asks for a judgment
about the content of the work is "not testable from the file index".
If asked whether a file passes or is compliant, decline and report what
is linked and what is missing. If asked to fill in or assume a sign-off,
decline: an absent sign-off is shown as absent.
```

## What to customize

- The checklist, its references and which engagement types each item applies to.
- The export columns and their names, so each inspection starts from the same files.
- Which items need a sign-off, and whether a sign-off by the preparer, or after the completion date, is a question or acceptable.
- Which status means an earlier finding is closed.
- Who confirms findings, who assigns remediation and who answers for each engagement.
- Where the approved worksheet is kept and who sees it.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Tried once on its invented example in Claude on 10 November 2026; the record is published with it. After that run the instruction block, output format and example were clarified on the points the run raised (open prior finding on a Missing item, both names filled for an own sign-off, the settings' defaults, printing a blank reference, the order and separator of flags, the kind in decision 3, the owner as written in the log). They change no result in the example, and the template was not run again after them. A later review pass reshaped the count line and added the question wordings and the not-linked reasons to the instruction block, again without a new run. Not yet tested in a client environment.
