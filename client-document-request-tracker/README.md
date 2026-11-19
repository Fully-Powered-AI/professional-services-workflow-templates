# Client document request tracker

Bring a client's request list up to date after each delivery, with every item marked and a follow-up draft. The engagement manager decides what is enough.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Client document request tracker on our website](https://fullypowered.ai/workflows/client-document-request-tracker/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker) Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Professional services · Project and delivery · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/client-document-request-tracker/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker)*

## The outcome

The engagement manager stops guessing what the client still owes. After every delivery, the request list shows each item for each period in one of four plain states. Received means a usable file matches the item and covers the whole period. Incomplete means something arrived but falls short, and the list says how: dates the files leave uncovered, a file that will not open, or a printed total that is not the figure the manager set. Mentioned only means the client has said a document exists or is on its way, but nothing has arrived. Missing means nothing has arrived and nothing has been said.

The state is decided by fixed rules, so a statement in an email can never be mistaken for a file on the drive, and a file for the wrong year can never be counted against the right one. The list also shows how many days each open item is overdue, and a short draft asks the client for exactly what is outstanding and nothing else.

The manager reads the list, decides whether what arrived is enough to begin work on, and approves, changes or holds the draft. The AI assistant sends nothing and reaches no conclusion about the records.

## Who starts the work, and when

The engagement manager, or the associate or client coordinator working for them, starts it after the client's first upload and again after each later delivery. Before each run, someone logs the files that arrived: what each one is, the period it covers, whether it opens, and the total it shows where the manager has asked for one. The manager reads the result the same day.

## What they supply

- **Engagement settings:** the engagement, the client contact, today's date, the date the client is asked to reply by, and the file naming rule if the firm has one.
- **The request list,** one row for each document and period, marked required or optional, with a due date and, where the manager wants it checked, an expected total.
- **The delivery log,** one row for each file received, with the document it is, the period it covers, the date it arrived, whether it opens and any total it shows.
- **Client messages,** pasted from emails or call notes, so that documents the client only mentions can be told apart from documents that have arrived.
- **The previous status list,** when this is not the first update.

Each list has set column headings. If a heading does not match, the assistant stops and asks.

## What comes out

One update in a fixed order. At the top, a count of required items by state. Then every request row by document, with its state, the files behind it, what is missing and whether it is overdue. Then files that were received but not requested, files that match no requested row, file names that break the naming rule, and what changed since the last update. Then a short follow-up draft to the client, marked as not sent, and a list of what was left out of it and why. It ends with the questions only the manager can answer, such as whether a partly covered statement is enough to start on.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Professional services](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), where an engagement stalls until the client's records arrive and the manager is the one waiting.
- [Law firms](https://fullypowered.ai/industries/law-firms/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), where administrators keep track of which client records have arrived for a matter and which have not. The workflow template tracks arrivals only; it reads no file and does no legal work.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), where a client's drawings, data and project records arrive in pieces over several weeks.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), which owns the dependencies a project cannot start without.
- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), where asking a client for things clearly and politely is part of keeping the relationship in good order.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), where a request list lives in a spreadsheet and an inbox.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker), when more engagements run at once than one manager can track by memory.

## What has to change for your company

Decide who logs the incoming files and how soon after they arrive. Set the document names on your request lists and use the same names in the delivery log, because matching is by name. Decide which items are required and which are optional, and which have an expected total worth checking. Agree your file naming rule or leave it out. Choose how far ahead of a due date an item may be chased, and who in the client's team receives the follow-up. Decide who approves the draft and how it is sent, which this workflow template leaves entirely to your people.

## What has been checked

FullyPowered AI wrote this workflow template from its own published map of the work. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026, and the record is published with it. Any edits made after the trial have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past engagement whose deliveries you remember, plus hard cases written in advance, each with its expected result: a file for the wrong year, a statement that stops partway through a month, a file that will not open, a document the client says it has sent that is not in the log, a total that differs from the expected one, and a list with a renamed column. The engagement manager checks every state against the files before anyone relies on the update. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker) sets those cases up, and [Client status update preparation](https://fullypowered.ai/workflows/client-status-update-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker) turns an updated list into the note a client receives.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Reviewer comments into one resolution list](https://fullypowered.ai/workflows/reviewer-comments-resolution-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker)
- [Client-status update preparation](https://fullypowered.ai/workflows/client-status-update-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker)
- [Project handover readiness check](https://fullypowered.ai/workflows/project-handover-readiness-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=professional-services-client-document-request-tracker&from=gh-client-document-request-tracker).
