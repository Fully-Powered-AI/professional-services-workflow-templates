# Engagement staffing plan: tried once on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md`: an invented advisory firm, invented people and invented engagements. No client data was used. The assistant that ran this trial did not write the template.

## Inputs used

The five inputs in `public/example.md` under "The inputs": the settings and notes, `people.csv`, `leave.csv`, `assignments.csv` and `demand.csv`. The instructions followed were the fenced block in `member/template.md` and its output format.

One limit on this trial: the template and the example were read in a single step, so the example's output was in view before the plan was worked out. The weeks, free days, shortfalls and options were then calculated by hand from the input files alone, and compared with the example afterwards. It is not a blind run.

## What came out

ENGAGEMENT STAFFING PLAN: 11 January to 19 February 2027

For: Resource lead, with the partners for Engagement C and Engagement D. Prepared Friday 8 January 2027 from 4 people, 1 leave entry, 6 assignments and 4 demand lines. Weeks counted: W1 11 Jan, W2 18 Jan, W3 25 Jan, W4 1 Feb, W5 8 Feb, W6 15 Feb. Closed days: none.

Demand: 2 committed lines, 2 tentative lines. Lines flagged: 1.

Capacity, committed work only
- Senior consultant, process-review (counted: Odalys, Perrin):
  - W3 25 Jan: needed 4, available 1, short 3.
  - W4 1 Feb: needed 4, available 4, short 0.
  - W5 8 Feb: needed 4, available 3, short 1.
- Partner, partner-review (counted: Ilse):
  - W3 25 Jan: needed 1, available 1, short 0.
  - W4 1 Feb: needed 1, available 1, short 0.
  - W5 8 Feb: needed 1, available 2, short 0.

The collision: Engagement D's delivery line (Senior consultant, process-review, 4 days a week, 25 January to 12 February) is short 4 days: 3 in W3 and 1 in W5. In W3, Odalys has 0 free days (Engagement A 3 days, Engagement C 2 days) and Perrin has 1 free day (Engagement A 4 days). In W5, Perrin is on leave 8 to 12 February (5 days) and Odalys has 3 free days (Engagement C 2 days). Engagement D's review line is not short in any week.

With tentative work added
- Senior consultant, process-review: W3 needed 4, available 1, short 3. W4 1 Feb needed 7, available 4, short 3. W5 8 Feb needed 7, available 3, short 4. W6 15 Feb needed 3, available 8, short 0. Total short 10.
- Partner, partner-review: W3 needed 1, available 1, short 0. W4 needed 2, available 1, short 1. W5 needed 2, available 2, short 0. W6 needed 1, available 2, short 0. Total short 1.

Options
1. Start Engagement D one week later (1 February to 19 February, its latest start). Committed work: senior consultant W4 needed 4 / available 4, W5 4 / 3, W6 4 / 8; partner W4 1 / 1, W5 1 / 2, W6 1 / 2. Short: 1 day (senior consultant, W5). With Engagement F won: senior consultant short 7 (W4 3, W5 4, W6 0), partner short 1 (W4). Touches: Engagement D's dates move one week; the partner of Engagement D to agree.
2. Keep Engagement D's dates and release Engagement C's days in W3 (2) and W5 (2), from Odalys's booking; the 4 days are moved later and not placed. Committed work: senior consultant W3 needed 4 / available 3, W4 4 / 4, W5 4 / 5; partner unchanged. Short: 1 day (senior consultant, W3). With Engagement F won: senior consultant short 6 (W3 1, W4 3, W5 2), partner short 1 (W4). Touches: Engagement C loses 4 days in its window; the partner of Engagement C to agree.
3. Start Engagement D one week later and release Engagement C's 2 days in W5. Committed work: senior consultant W4 needed 4 / available 4, W5 4 / 5, W6 4 / 8; partner W4 1 / 1, W5 1 / 2, W6 1 / 2. Short: 0. With Engagement F won: senior consultant short 5 (W4 3, W5 2), partner short 1 (W4). Touches: Engagement D's dates move one week and Engagement C loses 2 days in W5; the partners of Engagements C and D to agree.

If Engagement F is won, no combination of the levers supplied covers it: Engagement F's start range is a single date and none of its days can be released. The days still short are in the option lines above. Nothing is estimated for outside capacity.

Flags: 1
- Engagement F, delivery line: approved days are 8, but 3 days a week for 3 weeks is 9.

Not counted: Wendell, Senior consultant, holds data-migration and not process-review.

Decisions for the resource lead and partners: 3
1. How to cover Engagement D's 4 short days: a one-week later start (1 day still short, W5), releasing Engagement C's days in W3 and W5 (1 day still short, W3), or a later start with C's W5 days released (none short). Engagement D's partner would agree the start; Engagement C's partner has said its days can slide.
2. Whether Engagement F is staffed if it is won, given that 5 to 7 delivery days stay short under every option and 1 review day is short in W4.
3. Whether Engagement F's approved budget is 8 days or 9.

Draft for the resource lead. Nothing has been assigned, moved, sent or changed. Every figure traces to the files supplied.

## What was observed

- Every required part was produced, in the order of the output format. No stop condition applied. All headers matched, the window and today's date were given, and nothing in the files called for a refusal.
- All the figures match the example: the free days, the short weeks, the tentative comparison, the three options, the one budget flag and Wendell under "Not counted".
- Differences from the published example, all in wording or layout:
  - The closing line follows the instruction block word for word, "the files supplied". The example says "the five files supplied".
  - The example adds a parenthetical under the committed heading ("needed days / available days; weeks with no demand are left out") and under Options. The output format has neither, so they were left out.
  - The example's options say "nothing else changes" or list no partner. This run names the partner of each touched engagement, because the reviewer checklist asks for it. The inputs name no partner, so they are called "the partner of Engagement D".
  - The example's decision 1 puts the three ways in a slightly different order and words.
- No fact in this run's output is outside the inputs. In the example, the introduction says the firm has "three people who can do process-review work". The inputs give two people with that qualification (Odalys and Perrin), and the output counts two. That sentence is wrong. It is outside the output but inside the public page.

## Where the template was ambiguous or needed a guess

- **Which weeks a movable booking releases.** The procedure says a movable assignment "may release its days in named weeks" but not who names them or how many days. This run released the weeks where the line was short, W3 and W5, and the full 2 days in each. That is a choice the template does not settle. It is close to deciding how to staff, so the resource lead should name the weeks.
- **The partner's name.** The template asks for partners to be named for every touched engagement, but the inputs have no column for an engagement's partner. The "For:" line has the same gap.
- **Spare days.** Step 10 of the procedure says to "list the spare days of the people who count as facts". The fenced instruction block and the output format have no place for this, so it was left out.
- **Budget check on part weeks.** Step 11 counts "the weeks it touches", not working days. That gave 9 for Engagement F, but the template does not say what to do for a line that starts mid-week.
- **Tentative comparison format.** The format puts each group on one line and does not say whether to show weeks with no committed demand. This run showed every week that either kind of demand touches.
- **Option figures.** The format asks for needed and available "per group per week", and does not say whether to repeat unchanged groups, such as the partner group in option 2. This run wrote "partner unchanged".

## Shortcomings of this trial

- It is one run, by one model, on one invented example. It shows the instructions can be followed to the published result. It does not show the template is right for a real firm or a real time system.
- The example's output was visible before the plan was worked out, as described above.
- The template's version notes still say "Not yet tried on its example". That line needs updating by the template's author.

## Edits made after this run

These were made after the run above by the template's author, in response to an independent review. They have not been run again. None changes a figure on the invented example, because the example has no closed days, no part-time person on leave and no booking that starts mid-week; the recorded output above is unchanged.

- The version notes and the profile now say the template was tried once on its example.
- The example's introduction now says two senior consultants and a partner, correcting the sentence noted above. Its two parentheticals are removed, its closing line says "the files supplied", and its options now say "the partner of Engagement X to agree" as this run did.
- Movable bookings: the instructions now say days are released only in the weeks where the line being covered is short, up to the booking's days per week, with the weeks listed for the resource lead to confirm. This is what this run did.
- Closed days now reduce each person's days in that week by one, to no less than 0; the output format has a fallback line "No committed shortfall; no option needed."; the collision line and the tentative heading now carry the details the example shows; options are stated to cover the committed shortfall only, with the same levers recomputed for tentative work; the instructions say when released days exceed a week's shortfall; and the pasted instructions gained the blank-qualification, committed-or-tentative, window-end and contact-details rules. None changes a figure on the example.
- Spare days: the sentence asking for them is removed from the procedure.
- Leave is capped at a person's days per week, and a booking during a full week of leave is flagged "booked during leave". The budget check counts working days. The format says which weeks the tentative comparison shows and how unchanged groups are written.
- The pasted instructions now carry the part-week, shared-supply, duplicate-person, start-range, no-lever, no-clearing-option and health-information rules from the procedure, and the paste line before the block.
