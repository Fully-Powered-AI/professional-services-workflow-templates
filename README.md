# AI workflow templates for consulting and accounting firms

FullyPowered Workflow Templates for professional services firms turn the AI your firm already pays for into a team that knows how the work is done: an engagement manager with the client document request list brought up to date, a quality partner with finished engagement files checked against the firm's own checklist, a resource lead with the staffing collision spotted before kickoff. 7 workflow templates, made to be customized and deployed. All plain Markdown, all free, MIT license.

We are FullyPowered AI. We build AI workflows for companies, and these are the templates we start from. We publish them because a good starting point should be open to everyone. Copy one. Change it. Make it yours.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** These are templates, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See more examples for professional services firms](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme) · [Have one built for your team](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme) Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Who this is for**

- Managing partners and firm owners who have paid for AI and want engagements run the same careful way.
- Engagement leads who want a precise worksheet their team can use on the next engagement.
- The accountant or manager who does the work, gets it prepared, and still judges and approves.

**What these are for**

- **Your best way of doing it, for the whole team.** One piece of work, written down precisely enough that an assistant prepares it the same way every time.
- **Work you can check.** Every template says what it needs, what it produces, what it checked and what it could not.
- **A person decides.** Anything that sends, posts, pays or changes a record waits for someone to approve it.
- **Tied into your business systems.** A workflow can be designed to pull from the systems your company already runs, and even push data back into them, with guardrails and a person approving. [Browse the Connectors Directory](https://fullypowered.ai/connectors/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme).
- **Free, open and portable.** MIT-licensed plain instructions that run in the assistant or agent your team already uses: ChatGPT, Claude, Claude Code, Claude Cowork, Codex, Copilot, Gemini, Grok, Perplexity.

**Quick start**

1. **Check what your client has sent, in a few minutes.** Open ChatGPT, Claude, Copilot or Gemini. Copy the text below into a new chat. Replace each square bracket with your own list, file log and messages, then send it. Nothing needs to be downloaded or signed up for.

   ```text
   You help an engagement manager update a client document request list. You prepare; the manager decides. Do not send anything, contact the client, change any file or list, or judge whether a document is enough. Here is the request list: [paste your list with document, period, required yes or no, due date]. Here is what the client has delivered: [paste file names, dates received, period covered, readable yes or no]. Here are the client's messages: [paste emails or call notes]. Today's date is [date]. For each request row, mark it Received, Incomplete, Mentioned only or Missing, and say what is short. List files that were sent but not requested. Write a short follow-up draft to the client, marked as not sent. End with the questions only the manager can answer. If anything is unclear, ask me first.
   ```

2. Read what comes back. It marks what it checked and what is left for you. What comes out, with invented data:

   ```text
   **CLIENT DOCUMENT REQUEST TRACKER: Quarter-three records, Client A**

   For: Engagement manager. Client: Client A. Check date: Tuesday 10 November 2026. Reply requested by: Friday 13 November 2026.
   Supplied: request list (11 rows, 10 required); delivery log (7 files); client messages (2); previous status list (not supplied).

   Position: required rows 10: 3 Received, 3 Incomplete, 2 Mentioned only, 2 Missing. Optional rows 1: 0 Received, 0 Incomplete, 1 Mentioned only, 0 Missing. Received means usable files cover the period; it is not a judgment that they are sufficient.

   **Request list by document**

   *Operating account bank statement*

   - R01, 1 to 31 July 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F01. F01 covers 1 July to 20 August 2026.
   - R02, 1 to 31 August 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F01. F01 covers 1 to 20 August 2026. Not covered: 21 to 31 August 2026, 11 days. Overdue by 4 days.
   ```

3. Stop there. You will know if this is for you. When you want it fitted to your company, or built into your agents, [that is what we do](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme).

The engagement manager, partner or other named person at your firm decides every call on scope, staffing, sufficiency and what goes to a client; the template only prepares and checks.

These are samples and a starting point, made to be changed to fit how your firm works. Your engagement may need something that is not here, and a workflow can be one step or many. We can build the one your firm needs.

## The workflow templates here today

- **[Client document request tracker](client-document-request-tracker/)**: When a client sends its first batch of records, the engagement manager gets the request list brought up to date: each item and period marked received, incomplete, mentioned only or missing, plus a short follow-up draft. The manager judges what is sufficient and approves anything sent.
- **[Client findings validation document](client-findings-validation-document/)**: Before research becomes recommendations, the engagement lead sends the client one document: each material finding beside its evidence, the implication proposed and a clear request to confirm, correct or defer it. Nothing is added that the evidence does not show.
- **[Client schedule to ledger reconciliation](client-schedule-to-ledger-reconciliation/)**: When a client's subledger schedule and trial balance disagree, the responsible accountant gets one worksheet: both balances proved, every timing difference and unexplained entry listed, and the next step for each. Nothing is posted; every explanation waits for a person.
- **[Completed engagement file review](completed-engagement-file-review/)**: The quality partner gets a worksheet that tests finished engagement files against the firm's own checklist: each item linked to the engagement letter, workpaper or sign-off that answers it, with any open finding, and the missing evidence listed. The quality partner confirms findings and assigns remediation.
- **[Quality of earnings adjustment evidence schedule](earnings-adjustment-evidence-schedule/)**: When management proposes adjustments to a target's EBITDA, the deal team gets one schedule: each adjustment tied to its ledger entries, explanation and documents, with repeats, overlaps and gaps flagged and every gap written as a question. The engagement lead decides what is accepted.
- **[Engagement margin review](engagement-margin-review/)**: Midway or at close, the partner and finance lead get one worksheet for an engagement: recorded time, agreed fee, billed to date and supplied costs by workstream, the gaps that limit it, and the questions the team must answer. No cost rate is invented.
- **[Engagement staffing plan](engagement-staffing-plan/)**: When several engagements want the same people, the resource lead sees the collision before kickoff: role needs against free days, leave and competing assignments, week by week, with two or three staffing options. The resource lead and partners choose.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

To take the whole collection, press **Use this template** at the top of this page: it copies every folder into a repository in your own account, yours to change.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The workflow template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More workflow templates

The [FullyPowered Workflows Directory](https://fullypowered.ai/workflows/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme) lists every workflow template across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

For the work these templates come from, by area of the business and by task, see [AI workflow examples for professional services firms](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the workflow template drew on. Published by [FullyPowered AI](https://fullypowered.ai/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-readme&from=gh-professional-services-readme).
