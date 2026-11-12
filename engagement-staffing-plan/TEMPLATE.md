# Engagement staffing plan

Workflow template, version 0.1.0.

## Purpose

Prepare, for a window of weeks, a capacity comparison for the resource lead and the engagement partners: for each role and qualification, the days the committed engagements need against the days the qualified people actually have free after leave, current assignments and review commitments. The plan names the weeks and engagements where they collide, shows the same comparison with tentative engagements added, and sets out two or three staffing options built only from levers the firm has stated, each with the shortfall it leaves and what it touches. The assistant prepares; it never assigns a person, moves an engagement, changes a booking, contacts anyone or chooses an option.

## When to use it and when not to

Use it when a new engagement is confirmed, when a tentative one is close, at the regular staffing review, and again when leave is approved, a start date moves or an assignment changes.

Do not use it:

- to decide how many people the firm should employ, or to plan roles and cost. That is Headcount plan;
- to score a new proposal against the firm's criteria or to decide whether to take it on. That is Project intake and capacity review, which looks at a proposal beside committed projects;
- to judge how well any person works, rank people, or choose who suits an engagement. The plan counts days and qualifications only;
- to produce employment documents or hiring decisions;
- when the people, assignments or demand files are missing.

## Roles

- **Runs it:** the resource lead, the operations manager or a managing partner.
- **Chooses assignments and agrees any schedule change:** the resource lead and the engagement partners concerned.
- **Confirms that a booking can move:** the partner of the engagement that holds it.
- **Supplies leave and availability:** the people operations or office manager, or each person through their usual route.
- **Receives the plan:** the engagement partners who attend the staffing review.

## Inputs

The assistant works from files and notes the person supplies. It needs no connection to a time system or calendar and never asks for a password or a login code. A date is written YYYY-MM-DD. Lists inside a cell are separated by semicolons.

1. **people.csv.** Default headers: `person,role,qualifications,days_per_week`. Days per week is the most the person can give to engagement work in a standard week.
2. **leave.csv.** Default headers: `person,from,to`. Both dates are inclusive. If there is no leave, the file may have only the header row.
3. **assignments.csv.** Default headers: `person,engagement,kind,start,end,days_per_week,can_move`. Kind is `delivery` or `review`. Can move is `yes` or `no`; yes means the engagement's partner has said the days can slide. If it is blank, treat it as no.
4. **demand.csv.** Default headers: `engagement,status,kind,role,qualification,start,end,days_per_week,earliest_start,latest_start,approved_days`. Status is `committed` or `tentative`. Earliest and latest start are the range in which the line may start. Approved days is the budget in days for that line. If qualification is blank, match on role only and say so.
5. **The settings.** The planning window (first and last date), the days the office is closed, today's date, and notes, such as a partner's agreement that a booking may slide.

If a file's headers do not match the defaults, stop, show the headers found beside the headers expected, and ask which column is which. Never guess a column. If people.csv, assignments.csv or demand.csv is missing, stop. If leave.csv is missing, continue and write "leave not supplied" in the header. If the window or today's date is missing, stop and ask.

If the files contain performance ratings, pay, notes about a person's conduct or health information, do not use or repeat them; tell the person to remove them from the source.

## The procedure

1. **Check the files.** Confirm the headers, count the rows in each and list the people, roles and qualifications found. Stop and ask on a duplicate person, an unreadable date, or an end date before its start.
2. **Build the weeks.** Weeks run Monday to Friday. Number them W1, W2 and so on from the Monday on or before the window's first date, with the date of each Monday. List any closed day inside the window and remove it from that week's working days; a closed day reduces each person's days that week by one, to no less than 0.
3. **Count each person's free days per week.** Free days = the person's days per week, minus working days of leave falling in that week (closed days are not counted twice; leave takes at most the person's days per week, so a part-time person on a full week of leave has 0 days left, not a negative number), minus the days per week of every assignment that touches the week. An assignment touches a week if any working day of that week lies between its start and end; count the full days per week it states. If it starts after a Monday or ends before a Friday, flag it "part week counted in full". If the result is below zero, set free days to 0 and flag "over-booked by n days" with the person and the week, measured against the days left after leave. If leave takes the person's whole week and an assignment still touches it, flag "booked during leave" with the person, the week and the engagement instead.
4. **Group the demand.** A group is one role, one qualification and one kind. For each demand line, the same rule marks the weeks it touches. Needed days in a week = the sum of days per week of all lines in the group touching that week, separated into committed and tentative.
5. **Find who counts.** A person counts toward a group only if their role equals the group's role exactly and the group's qualification appears in their qualifications. A person who counts in two groups with demand in the same week is flagged "shared supply, do not add". List separately, under "Not counted", every person with the right role but not the qualification, and every person with the qualification but a different role, with the reason. Never widen a role or qualification.
6. **Compare, committed work only.** For each group and each week with committed demand: needed, available (the sum of free days of the people who count) and short = needed minus available, or 0. Add the shortfall days for each group.
7. **Name the collision.** For every short week, say which line is short, how many days and in which weeks. Then say what holds the days: for each person who counts, the assignments and leave that take their days in that week, by engagement and number of days. Name the assignments and engagements as facts. Do not suggest that any of them is less important.
8. **Add tentative work.** Repeat step 6 with committed and tentative demand together, as a separate comparison. Never merge the two in one figure.
9. **Find the levers.** A lever exists only where the inputs allow it: (a) a demand line whose earliest and latest start differ may start in any whole week between them, all lines of one engagement moving together by the same number of weeks (if their ranges disagree, ask); (b) an assignment marked `can_move` yes may release its days, but only in the weeks where the line being covered is short, and no more than the booking's days per week in any one week; where the days released exceed the shortfall in that week, say so. List the weeks and the days released so the resource lead can confirm or change them; the days are listed as moved later and are not placed by the assistant. Options are built against the committed shortfall only; the same levers are then recomputed with tentative work added, and no further days are released for it. No other lever exists. A shifted line that would end after the window is shown only to the window's end, with a note that the weeks after it are not counted.
10. **Build two or three options.** Each uses a different combination of levers and is recomputed in full, committed work and then with tentative work added. For each option, give the changes it makes, the needed and available days per group per week, the days still short, the days short with tentative work won, and what it touches: engagements whose dates move, assignments that lose days, partners who must agree. Never say who should take the work. If no lever exists, say there are no options from the inputs and ask what the resource lead can change. If no option removes the shortfall, say so and give the days still short; outside capacity is a question for the resource lead, with no cost estimated.
11. **Check the budget.** For each demand line, count the working days from its start to its end (closed days removed, a part week counted by its working days), multiply by days per week and divide by 5; that should equal approved days. Flag each difference with both figures.
12. **Write the decisions.** One numbered decision per question only the resource lead or the partners can answer, with the facts. Recommend nothing unless the resource lead asks.
13. **Return the draft** to the person who ran it, for the resource lead. The resource lead and the partners choose assignments and agree schedule changes; a person tells the people concerned.

## Exceptions and stop conditions

- **Headers that do not match, a missing required file, or an unreadable date:** stop and ask.
- **A group with demand and nobody who counts:** show needed days, available 0, short equal to needed, and list who was not counted and why.
- **Lines of one engagement with disagreeing start ranges:** ask before building any option.
- **Over-booked person:** flag it and continue with free days at 0.
- **A tentative line marked committed in one file and tentative in another:** ask.
- **Asked to assign a person, choose an option, move an engagement, change a record, notify anyone, rate or compare people, or recommend a hire:** decline and name the role that decides.
- **Asked to treat tentative work as committed:** decline; show it as a separate comparison.
- **The files contain contact details, a password or a login code:** do not repeat them; tell the person to remove them.

## Output format

```
ENGAGEMENT STAFFING PLAN: [first date] to [last date]

For: [Resource lead], with the partners for [engagements]. Prepared [weekday date] from [n] people, [n] leave entries, [n] assignments and [n] demand lines. Weeks counted: [W1 date, W2 date, ...]. Closed days: [list, or none].

Demand: [n] committed lines, [n] tentative lines. Lines flagged: [n].

Capacity, committed work only
- [Role, qualification] (counted: [people]):
  - [W# date]: needed [n], available [n], short [n].
[One group per line group. If no committed demand: None.]

The collision: [Line with its role, qualification, days a week, dates and approved days; days short, weeks, and what holds the days: person, engagement, days, leave. If none short: No committed shortfall.]

With tentative work added ([engagement])
- [Role, qualification]: [W# date] needed [n], available [n], short [n], for every week that committed or tentative demand touches. Total short [n].
[If no tentative lines: None.]

Options
1. [Lever and the change]. Committed work: [group week needed / available, for every group; write "unchanged" for a group the option does not change]. Short: [n days, where]. With [engagement] won: [short by group and week]. Touches: [dates moved, days released by week, the partner of each engagement touched to agree].
2. [As above.]
3. [As above, if there are three.]
[If there is no committed shortfall: No committed shortfall; no option needed.]
[If no lever: No option can be built from the inputs. Then the shortfall remaining and a question.]
[Line on what no lever covers, if anything.]

Flags: [n]
- [Line, what is wrong, with both figures.]
[If none: None.]

Not counted: [Person, role, why.] [If none: None.]

Decisions for the resource lead and partners: [n]
1. [Question, with the facts.]

Draft for the [resource lead]. Nothing has been assigned, moved, sent or changed. Every figure traces to the files supplied.
```

## Reviewer checklist

1. Each file's row count matches the source. (Resource lead)
2. Free days for two people in two weeks, recomputed by hand from days per week, leave and assignments, match. (Resource lead)
3. Needed days for each group and week match the demand lines, with committed and tentative kept apart. (Engagement partner)
4. No person is counted for a role or qualification they do not hold. (Resource lead)
5. Every option uses only a start range or a movable assignment that is in the inputs, and its figures are recomputed in full. (Resource lead)
6. No option assigns a person or ranks one engagement above another. (Engagement partner)
7. Every engagement an option touches is named, with "its partner to agree"; the inputs carry no partner's name, so the plan does not supply one. (Resource lead)
8. Each budget difference shows both figures. (Engagement partner)
9. Nothing in the plan comments on how well any person works. (Resource lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal run.** One group, two people, no leave, one committed line that fits. Expected: no short weeks, "No committed shortfall", options section reads "No committed shortfall; no option needed."
2. **Leave in the start week.** A person on leave for a whole week of a line. Expected: their free days are 0 that week and the week is short.
3. **Qualification missing.** A role with the right title but no one holding the qualification. Expected: available 0, everyone listed under Not counted with the reason.
4. **Tentative apart.** A tentative line that would double a week's load. Expected: committed table unchanged; tentative shown only in its own comparison.
5. **Movable booking.** A booking marked yes with a partner's note. Expected: used as a lever; days listed as moved later, not placed.
6. **Booking not marked movable.** Expected: never used as a lever.
7. **Header mismatch.** `people.csv` has `name` instead of `person`. Expected: stops and asks.
8. **Over-booked.** Assignments add to more than days per week. Expected: flag with person and week; free days 0.
9. **Budget mismatch.** Approved days differ from days times weeks. Expected: flag with both figures.
10. **Asked to pick.** The user asks which option to take or who should staff the line. Expected: declines and names the resource lead and partners.
11. **Ratings in the file.** A column of performance ratings. Expected: not used or repeated; the person is told to remove it.
12. **Part-time person on leave.** A person with 3 days a week on leave for a full week. Expected: free days 0, no "over-booked" flag.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the engagement staffing plan for the resource lead. You never
assign a person, move an engagement, change a booking or record, contact
anyone, or choose an option. The resource lead and the engagement partners
choose and approve every assignment and schedule change.

The user will supply people.csv (person, role, qualifications,
days_per_week), leave.csv (person, from, to), assignments.csv (person,
engagement, kind, start, end, days_per_week, can_move), demand.csv
(engagement, status, kind, role, qualification, start, end, days_per_week,
earliest_start, latest_start, approved_days) and the settings: window,
closed days, today's date, notes. If a file's headers differ from these,
stop, show the headers found and expected, and ask which column is which.
If people, assignments or demand is missing, or the window or today's date
is missing, stop. If leave is missing, say "leave not supplied" and go on.
Stop and ask on a duplicate person, an unreadable date or an end date
before its start. Never ask for a password or a login code. Do not use or
repeat ratings, pay, conduct notes or health information; tell the user to
remove them. A blank qualification means match on role only; say so. A
line marked committed in one place and tentative in another: ask. A
shifted line that would end after the window is shown only to the
window's end, with a note that the weeks after are not counted. Do not
repeat contact details, passwords or login codes found in the files; tell
the user to remove them.

1. Weeks run Monday to Friday, numbered W1 onward, each with its Monday's
   date. Remove closed days; a closed day reduces each person's days that
   week by one, to no less than 0.
2. Free days per person per week = days_per_week - working days of leave in
   that week (leave takes at most the person's days_per_week) -
   days_per_week of every assignment touching that week. Count an
   assignment in full for any week it touches; if it starts after a Monday
   or ends before a Friday, flag "part week counted in full". If below
   zero, use 0 and flag "over-booked by n days"; if leave takes the whole
   week and an assignment still touches it, flag "booked during leave"
   instead.
3. A group is one role, qualification and kind. Needed days per week = sum
   of days_per_week of the lines touching that week, committed and
   tentative kept apart.
4. A person counts toward a group only if their role equals the group's
   role exactly and they hold the qualification. List everyone else with
   the right role or the qualification under "Not counted" with the reason.
   A person who counts in two groups with demand in the same week is
   flagged "shared supply, do not add".
5. For each group and week: needed, available, short (needed minus
   available, minimum 0). Do committed work alone first, then committed
   plus tentative as a separate comparison.
6. Name the collision: which line is short, how many days, which weeks, and
   what holds the days, by person, engagement and days, and leave. State
   facts only.
7. Levers are only these: a line whose earliest_start and latest_start
   differ may start in any whole week between them, all lines of one
   engagement moving together (if one engagement's start ranges disagree,
   ask before building any option); an assignment marked can_move yes may
   release days only in the weeks where the line being covered is short,
   up to its days_per_week in any week (say so where the days released
   exceed the shortfall that week); list those weeks and days so the
   resource lead can confirm them, as moved later and not placed. Build
   two or three options, each recomputed in full, committed and then with
   tentative work added, with the same levers and no further days released
   for tentative work; options cover the committed shortfall only. For
   each give: the change, needed and available
   per group per week, days still short, days short if tentative work is
   won, and what it touches, naming each engagement touched and "its
   partner to agree". Never say who should take the work. If there is no committed
   shortfall, write "No committed shortfall; no option needed." in place
   of options. If no lever exists, say no option can be built from the inputs and ask what the
   resource lead can change. If no option clears the shortfall, say so and
   give the days still short; estimate no cost for outside capacity.
8. Check each line: working days from start to end (closed days removed)
   times days_per_week divided by 5, against approved_days. Flag
   differences with both figures.
9. Write the decisions as questions with their facts. Recommend nothing
   unless asked.
10. Use the output format exactly. Where a section is empty, print None, or
    the stated fallback line. End with: "Draft for the [resource lead].
    Nothing has been assigned, moved, sent or changed. Every figure traces
    to the files supplied."

Decline to assign anyone, to rate or compare people, to recommend a hire,
to treat tentative work as committed, or to choose an option. Name the role
that decides. Never adjust a figure to make an option fit.
```

## What to customize

- Your roles and qualifications, spelled the same way in every file.
- Whether a person may cover a line for a neighbouring role, such as a senior consultant on a consultant line. As written, no one does.
- The unit of time. As written, whole Monday to Friday weeks and whole days.
- Which bookings may move, and who confirms it.
- Standard days per week for part-time people and how much of a week a partner has for review.
- Your review lines: whether review is its own role, as in the example, or a share of delivery time.
- Whether a line with a start range that crosses the end of the window should be tested beyond it.
- Where the approved plan is kept and who tells the people concerned.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026, with the record published. Edits to the pasted instructions, the output format, the checklist and the example were made after that run and have not been run again; the trial record lists them. Not yet tested in a client environment.
