# Engagement staffing plan: an invented example

*Illustrative example with invented data.* The firm, the people, the engagements, the dates and the days below are all invented. The firm is an invented advisory firm with two senior consultants qualified for process review and a partner with a few days a week for review. First come the inputs the resource lead supplied, in full, then the plan the workflow template returned.

## The inputs

### 1. Settings and notes

```
Planning window: Monday 11 January 2027 to Friday 19 February 2027
Weeks: Monday to Friday
Closed days: none
Today: Friday 8 January 2027
Notes:
- Engagement C's partner has said C's days can slide later. Any days
  released go after 19 February.
- Engagement F is not signed. It is tentative.
```

### 2. people.csv

```
person,role,qualifications,days_per_week
Odalys,Senior consultant,process-review,5
Perrin,Senior consultant,process-review,5
Wendell,Senior consultant,data-migration,5
Ilse,Partner,partner-review,3
```

### 3. leave.csv

```
person,from,to
Perrin,2027-02-08,2027-02-12
```

### 4. assignments.csv

```
person,engagement,kind,start,end,days_per_week,can_move
Odalys,Engagement A,delivery,2027-01-11,2027-01-29,3,no
Odalys,Engagement C,delivery,2027-01-11,2027-02-19,2,yes
Perrin,Engagement A,delivery,2027-01-11,2027-02-05,4,no
Wendell,Engagement B,delivery,2027-01-11,2027-02-19,5,no
Ilse,Engagement A,review,2027-01-11,2027-02-05,1,no
Ilse,Engagement B,review,2027-01-11,2027-02-19,1,no
```

### 5. demand.csv

```
engagement,status,kind,role,qualification,start,end,days_per_week,earliest_start,latest_start,approved_days
Engagement D,committed,delivery,Senior consultant,process-review,2027-01-25,2027-02-12,4,2027-01-25,2027-02-01,12
Engagement D,committed,review,Partner,partner-review,2027-01-25,2027-02-12,1,2027-01-25,2027-02-01,3
Engagement F,tentative,delivery,Senior consultant,process-review,2027-02-01,2027-02-19,3,2027-02-01,2027-02-01,8
Engagement F,tentative,review,Partner,partner-review,2027-02-01,2027-02-19,1,2027-02-01,2027-02-01,3
```

## The output

**ENGAGEMENT STAFFING PLAN: 11 January to 19 February 2027**

**For:** Resource lead, with the partners for Engagements C and D. Prepared Friday 8 January 2027 from 4 people, 1 leave entry, 6 assignments and 4 demand lines. Weeks counted: W1 11 Jan, W2 18 Jan, W3 25 Jan, W4 1 Feb, W5 8 Feb, W6 15 Feb. Closed days: none.

**Demand:** 2 committed lines, 2 tentative lines. Lines flagged: 1.

**Capacity, committed work only**

- **Senior consultant, process-review** (counted: Odalys, Perrin):
  - W3 25 Jan: needed 4, available 1, short 3.
  - W4 1 Feb: needed 4, available 4, short 0.
  - W5 8 Feb: needed 4, available 3, short 1.
- **Partner, partner-review** (counted: Ilse):
  - W3 25 Jan: needed 1, available 1, short 0.
  - W4 1 Feb: needed 1, available 1, short 0.
  - W5 8 Feb: needed 1, available 2, short 0.

**The collision:** Engagement D's delivery line (Senior consultant, process-review, 4 days a week, 25 January to 12 February, 12 days) is short 4 days: 3 in W3 and 1 in W5. In W3 Odalys has no free day (Engagement A 3, Engagement C 2) and Perrin has 1 free day after 4 on Engagement A. In W5 Perrin is on leave from 8 to 12 February and Odalys has 3 free days after 2 on Engagement C. Partner review for Engagement D fits in every week.

**With tentative work added** (Engagement F)

- **Senior consultant, process-review:** W3 needed 4, available 1, short 3. W4 needed 7, available 4, short 3. W5 needed 7, available 3, short 4. W6 15 Feb needed 3, available 8, short 0. Total short 10.
- **Partner, partner-review:** W3 needed 1, available 1, short 0. W4 needed 2, available 1, short 1. W5 needed 2, available 2, short 0. W6 needed 1, available 2, short 0. Total short 1.

**Options**

1. **Start Engagement D one week later,** 1 February to 19 February, which is its latest start. Committed work: senior consultant W4 needed 4 / available 4, W5 4 / 3, W6 4 / 8; partner W4 1 / 1, W5 1 / 2, W6 1 / 2. Short: 1 day (senior consultant, W5). With Engagement F won: senior consultant short 7 (W4 3, W5 4), partner short 1 (W4). Touches: Engagement D's dates move one week; the partner of Engagement D to agree.
2. **Keep Engagement D's dates and release Engagement C's 2 days in W3 and 2 in W5** (4 days, from Odalys's booking; the booking's full 2 days a week, though the line is short only 1 day in W5, which the rule allows; they land after 19 February and are not placed here). Committed work: senior consultant W3 needed 4 / available 3, W4 4 / 4, W5 4 / 5; partner unchanged. Short: 1 day (senior consultant, W3). With Engagement F won: senior consultant short 6 (W3 1, W4 3, W5 2), partner short 1 (W4). Touches: Engagement C loses 4 days in W3 and W5; the partner of Engagement C to agree.
3. **Start Engagement D one week later and release Engagement C's 2 days in W5** (the booking's full days a week, where the line is short 1). Committed work: senior consultant W4 needed 4 / available 4, W5 4 / 5, W6 4 / 8; partner W4 1 / 1, W5 1 / 2, W6 1 / 2. Short: 0. With Engagement F won: senior consultant short 5 (W4 3, W5 2), partner short 1 (W4). Touches: Engagement D's dates move one week and Engagement C loses 2 days in W5; the partners of Engagements C and D to agree.

If Engagement F is won, no combination of the levers supplied covers it. The days still short are in the option lines above. What to do about them, such as outside capacity or a later start for F, is for the resource lead and the partners to raise; no cost has been estimated.

**Flags: 1**

- Engagement F, delivery line: approved days are 8, but 3 days a week for 3 weeks is 9.

**Not counted:** Wendell, Senior consultant, holds data-migration and not process-review, so his days are not in the process-review supply.

**Decisions for the resource lead and partners: 3**

1. Which way to cover Engagement D's 4 short days: a one-week later start (1 day still short, W5), releasing Engagement C's days (1 day still short, W3), or both (none short)? Engagement D's partner would agree the start; Engagement C's partner has said its days can slide.
2. Whether Engagement F is staffed if it is won, given that 5 to 7 delivery days stay short under every option and 1 review day is short in W4.
3. Whether Engagement F's approved budget is 8 days or 9.

Draft for the resource lead. Nothing has been assigned, moved, sent or changed. Every figure traces to the files supplied.
