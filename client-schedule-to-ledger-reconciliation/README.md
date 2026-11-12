# Client schedule to ledger reconciliation

When a client's subledger schedule and trial balance disagree, the responsible accountant gets one worksheet: both balances proved, every timing difference and unexplained entry listed, and the next step for each. Nothing is posted; every explanation waits for a person.

*Workflow template · Professional services · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/client-schedule-to-ledger-reconciliation/)*

## The outcome

A client sends a receivables or payables schedule, and the control account in its trial balance shows a different figure. The usual response is an afternoon of ticking one list against the other. This workflow template does the matching first and shows the result as a worksheet.

The worksheet proves each side to its own source before comparing them. It then splits the difference into what is explained by timing, such as an invoice the subledger holds and the ledger posted after the reporting date, and what has no explanation yet, such as a manual journal with no schedule entry behind it, or an amount that differs between the two. Each item carries its evidence, what the client has said about it, and the step that would settle it. If the items do not add up to the difference, the remainder is shown, and nothing is added to hide it.

The assistant prepares. The responsible accountant confirms every explanation and agrees any correcting entry with the client. It offers no audit, tax or assurance opinion.

## Who starts the work, and when

The accountant or controller who looks after the client's books starts it when a schedule arrives that does not agree to the ledger: at month end, before a reporting deadline, or when the client's own accountant raises the gap. One run covers one subledger, one control account and one reporting date.

The responsible accountant reviews the worksheet and decides what is accepted. The client's finance contact is asked for whatever only the client can answer.

## What they supply

- **Settings:** the client, the subledger and its control account, the reporting date, the period start, the subledger's opening and closing balances and the ledger's opening balance as the systems report them, the tolerance, the date the files were run, the date up to which to look for late postings, and the client contact.
- **The trial balance extract** with the control account's balance.
- **The subledger schedule** for the period, with each document's reference, date, customer or supplier, type and amount.
- **The journal detail** posted to the control account for the period, plus anything posted after the reporting date.
- **The last reconciliation,** showing the agreed opening position, and any notes from the client.

Files exported from the systems are enough. It needs no access to the client's ledger, and it never asks for a password or a login code.

## What comes out

One worksheet, in a fixed order: the source balances and the checks on them, the result, a proof that walks from the schedule to the trial balance, what matched, the timing differences, the unexplained entries, the investigation steps in order, the correcting entries that may be needed (for a person to agree with the client), the decisions that are the accountant's, and what could not be assessed.

A good worksheet lets the accountant trace every figure to a line in one of the files and see why each item sits where it does.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the reconciliation and the close it feeds.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where an outsourced accounting practice receives schedules prepared by the client and has to agree them to the books.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where marketplace, card and trade receivables schedules often run a few days apart from the ledger.
- [Construction](https://fullypowered.ai/industries/construction/), where progress billing and retentions make subledger and ledger postings fall on different dates.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the reconciliation has lived with one careful person and should be repeatable by anyone.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when transaction volume outgrows the hand-tick method.

It stays apart from [bank reconciliation preparation](https://fullypowered.ai/workflows/bank-reconciliation-preparation/), which agrees the books to a bank statement, and from [receivables exception review](https://fullypowered.ai/workflows/receivables-exception-review/), which decides what to do with individual receipts. This one agrees a client's subledger schedule to its own ledger.

## What has to change for your company

- **Your exports.** The column names the client's systems produce. If a heading does not match, the template stops and asks rather than guessing.
- **Your tolerance.** The size of a difference you still list rather than ignore, and how many days past the reporting date you look for late postings.
- **Your roles.** Who prepares, who is the responsible accountant, who at the client answers questions, and who agrees a correcting entry with the client.
- **Your engagement rules.** How your engagement letter or reconciliation policy treats unsupported manual journals and disputed classifications.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply. Decide which exports the assistant may read and where signed reconciliations are kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. The points that run found open were settled the same day, after an independent review, without a rerun; the record lists them. A second review's small changes were made later the same day, also without a rerun. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month your team has already reconciled by hand, plus hard cases written in advance, each with the expected result: a schedule that does not add to its stated total, a posting dated after the reporting date, a manual journal with no support, two digits swapped in an amount, a file with a heading it does not recognize. The responsible accountant compares every figure with the signed reconciliation before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
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

- [Bank reconciliation preparation](https://fullypowered.ai/workflows/bank-reconciliation-preparation/)
- [Receivables exception review](https://fullypowered.ai/workflows/receivables-exception-review/)
- [Month-end close checklist](https://fullypowered.ai/workflows/month-end-close-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
