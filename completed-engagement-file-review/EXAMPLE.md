# Completed engagement file review: an invented example

*Illustrative example with invented data.* The firm, the clients, the people, the files and the dates below are all invented. The firm is an invented 40-person accounting and advisory practice. The quality partner selected three finished engagements for inspection and supplied the lists below; the practice administrator ran the capability. First come the inputs, in full, then the worksheet the capability returned.

## The inputs

### 1. Inspection settings

```
Inspection: Q4 2026 file inspection
Today: 2026-11-10
Quality partner: Quality partner
Own sign-off: flag a sign-off by the person who prepared the item
Finding status: Closed means closed; any other status counts as open
```

### 2. The firm's checklist

```
item_id,item_text,evidence_kind,ref,needs_signoff,applies_to
C01,Signed engagement letter on file,letter,,yes,all
C02,Acceptance and independence form,workpaper,A-10,yes,all
C03,Planning memo,workpaper,B-10,yes,all
C04,Completion checklist with procedures cross-referenced,workpaper,D-10,yes,Review
C05,Work programme for the advisory deliverable,workpaper,D-20,yes,Advisory
C06,Manager review sign-off,signoff,R-10,yes,all
C07,Partner review sign-off,signoff,R-20,yes,all
C08,Client acceptance of the final deliverable,workpaper,F-10,yes,
```

### 3. Engagements selected

```
engagement_id,client_code,engagement_type,completion_date,engagement_partner
E-2601,Client A,Review,2026-06-30,Partner 1
E-2602,Client B,Advisory,2026-08-14,Partner 2
E-2603,Client C,Review,2026-09-30,Partner 1
```

### 4. File index

```
engagement_id,kind,ref,title,prepared_by,item_date,signed_off_by,signoff_date
E-2601,letter,,Engagement letter Client A,Partner 1,2026-02-02,Client A director,2026-02-03
E-2601,workpaper,A-10,Acceptance and independence form,Manager 1,2026-02-04,Partner 1,2026-02-05
E-2601,workpaper,B-10,Planning memo,Manager 1,2026-02-20,Manager 1,2026-02-21
E-2601,workpaper,D-10,Completion checklist,Senior 1,2026-06-25,Manager 1,2026-06-26
E-2601,signoff,R-10,Manager review sign-off,,2026-06-26,Manager 1,2026-06-26
E-2601,signoff,R-20,Partner review sign-off,,2026-07-09,Partner 1,2026-07-09
E-2602,letter,,Engagement letter Client B,Partner 2,2026-03-02,Client B director,2026-03-04
E-2602,workpaper,A-10,Acceptance and independence form,Manager 2,2026-03-05,Partner 2,2026-03-06
E-2602,workpaper,B-10,Planning memo,Manager 2,2026-03-12,Partner 2,2026-03-13
E-2602,workpaper,D-20,Advisory work programme,Senior 2,2026-08-05,,
E-2602,workpaper,X-50,Client correspondence index,Senior 2,2026-03-20,,
E-2602,signoff,R-10,Manager review sign-off,,2026-08-10,Manager 2,2026-08-10
E-2602,workpaper,F-10,Client acceptance of final deliverable,Senior 2,2026-08-14,Partner 2,2026-08-14
E-2603,workpaper,A-10,Acceptance and independence form,Manager 3,2026-04-06,Partner 1,2026-04-07
E-2603,workpaper,B-10,Planning memo,Manager 3,2026-04-14,Partner 1,2026-04-15
E-2603,workpaper,B-10,Planning memo revised,Manager 3,2026-05-12,Partner 1,2026-05-13
E-2603,workpaper,D-10,Completion checklist,Senior 3,2026-09-24,Manager 3,2026-09-25
E-2603,signoff,R-10,Manager review sign-off,,2026-09-25,Manager 3,2026-09-25
E-2603,signoff,R-20,Partner review sign-off,,2026-09-29,Partner 1,2026-09-29
E-2603,workpaper,F-10,Client acceptance of final deliverable,Senior 3,2026-09-30,Partner 1,2026-09-30
```

### 5. Findings log from earlier inspections

```
finding_id,engagement_id,item_id,finding_text,status,owner,action_ref
F-014,E-2601,C07,Partner review recorded after the engagement was delivered,Open,Engagement partner,CA-22
F-011,E-2602,C05,Work programme steps not cross-referenced to workpapers,Open,Manager 2,CA-19
F-012,E-2603,C01,Engagement letter template out of date,Closed,Practice administration,CA-20
F-016,E-2603,,Retention date not recorded on the file,Open,Practice administration,CA-24
F-009,E-2599,C03,Planning memo not updated after scope change,Closed,Manager 4,CA-17
```

## The output

**COMPLETED ENGAGEMENT FILE REVIEW WORKSHEET: Q4 2026 file inspection**

Prepared for: Quality partner. Checklist, engagement list, file index and findings log as supplied on 10 November 2026. Engagements selected: E-2601, E-2602, E-2603.
Assumptions: applies_to is blank for C08, treated as all.

Count: 3 engagements, 8 checklist items. Applicable item checks 21: Evidenced 14 + Check first 4 + Missing 3 = 21. Not applicable 3. Applicable 21 + not applicable 3 = 24, which is 3 engagements x 8 items. File items supplied 20: linked 19, not linked 1. Prior findings supplied 5: linked 3, not linked 2.

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
  Flags: Own sign-off (Manager 1 prepared and signed off this item)
  Prior findings: none
  To settle:
  1. Partner 1: Manager 1 prepared and signed off B-10. Was a second person's review made, and where is it recorded?

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
  Flags: Sign-off after completion (signed off on 9 July 2026; completion date 30 June 2026); Open prior finding (F-014).
  Prior findings: F-014, Open, action CA-22
  To settle:
  2. Partner 1: R-20 was signed off on 9 July 2026, after the completion date of 30 June 2026. Was the work reviewed before completion, and where is that recorded?
  3. Engagement partner (owner of F-014): F-014 is open against this item, action CA-22. Has the action been completed on this file?

C08 Client acceptance of the final deliverable: Missing
  Found: nothing in the file index for workpaper F-10.
  Flags: none
  Prior findings: none
  To settle:
  4. Partner 1: Where is workpaper F-10, or was it never made? The file index lists nothing.

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
  Flags: Sign-off absent (signer and date not recorded); Open prior finding (F-011).
  Prior findings: F-011, Open, action CA-19
  To settle:
  5. Partner 2: Who signed off D-20, and when? The file index records neither a signer nor a date.
  6. Manager 2 (owner of F-011): F-011 is open against this item, action CA-19. Has the action been completed on this file?

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
  7. Partner 2: Where is signoff R-20, or was it never made? The file index lists nothing.

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
  8. Partner 1: Where is the engagement letter, or was it never made? The file index lists nothing.

C02 Acceptance and independence form: Evidenced
  Found: workpaper A-10, "Acceptance and independence form", dated 6 April 2026; prepared by Manager 3; signed off by Partner 1 on 7 April 2026.
  Flags: none
  Prior findings: none
  To settle: nothing

C03 Planning memo: Check first
  Found: workpaper B-10, "Planning memo", dated 14 April 2026; prepared by Manager 3; signed off by Partner 1 on 15 April 2026.
  Found: workpaper B-10, "Planning memo revised", dated 12 May 2026; prepared by Manager 3; signed off by Partner 1 on 13 May 2026.
  Flags: More than one match (2 items for workpaper B-10).
  Prior findings: none
  To settle:
  9. Partner 1: Two items match workpaper B-10: "Planning memo" (14 April 2026) and "Planning memo revised" (12 May 2026). Which is the one for the file?

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

Prior findings not linked to any checklist item: F-016, E-2603, Open, "Retention date not recorded on the file" (no checklist item named), action CA-24; F-009, E-2599, Closed, "Planning memo not updated after scope change" (engagement not in this selection), action CA-17.

Decisions for the Quality partner
1. Findings to confirm: E-2601 C03, C07, C08; E-2602 C05, C07; E-2603 C01, C03.
2. Prior findings to attach to an item or an engagement: F-016, F-009.
3. File items to place against a checklist item, or to leave out of the checklist: E-2602 workpaper X-50.
4. Remediation for each confirmed finding: who acts, and by when.

This worksheet, built from the lists supplied for Q4 2026 file inspection, shows what the file index lists against the firm's checklist. It does not show that any item's content is right, that a sign-off was properly given, or that any engagement complies with professional standards. The quality partner confirms findings and the engagement partner answers questions about the file. The worksheet changes no file and sends nothing.
