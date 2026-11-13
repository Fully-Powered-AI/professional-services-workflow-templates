# Quality of earnings adjustment evidence schedule

When management proposes adjustments to a target's EBITDA, the deal team gets one schedule: each adjustment tied to its ledger entries, explanation and documents, with repeats, overlaps and gaps flagged and every gap written as a question. The engagement lead decides what is accepted.

*Workflow template · Professional services · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/earnings-adjustment-evidence-schedule/)*

## The outcome

Management's list of adjustments arrives with a reported EBITDA, a higher adjusted figure and a folder of support. Before the team can form a view, someone has to tie each line to the ledger and the documents. This workflow template does that tying and lays it out as one schedule.

Each adjustment shows the ledger entries management cites and whether they add up to the amount, management's explanation, and each supporting document matched to its entry. Estimates, such as an owner's salary brought to the cost of a replacement, have their arithmetic recomputed and every figure that is not from the ledger listed with its document, or marked as having none. The facts a reviewer would challenge are flagged: the same supplier paid in the prior year for an item called one-off, one ledger entry claimed by two adjustments, an entry outside EBITDA, an entry dated outside the test period. Each adjustment gets an evidence status (traced, traced with flags, or not traced), and every gap becomes a plain question for management.

The schedule proposes no adjustment of its own, states no adjusted earnings of its own, and gives no valuation and no opinion. The engagement lead decides which adjustments the firm accepts and which questions go to management.

## Who starts the work, and when

A member of the deal team, such as the manager or senior on the engagement, starts it when management's proposed adjustments arrive with the ledger detail and supporting documents. It runs again each time management answers questions or sends more documents, and marks each earlier question answered, partly answered or still open. One run covers one target and one test period.

The engagement lead reviews the schedule, decides what the firm accepts, and decides which questions are sent. The target's finance contact answers what only the business can answer.

## What they supply

- **Engagement settings:** the target, the test period, a look-back period (by default the year before), the currency, reported EBITDA, management's adjusted EBITDA, the tie tolerance, and which of management's categories count as one-off and which as estimates.
- **Management's adjustment list,** with each adjustment's reference, description, category, amount and the ledger entries it cites.
- **Ledger detail** for the accounts the adjustments cite, covering the test period and the look-back period.
- **An account map** showing which accounts sit inside EBITDA.
- **Management's explanations,** one per adjustment.
- **The supporting documents,** or the data room index that lists them, with each document's counterparty and amount.
- **Earlier questions and answers,** on a second run.

Files exported from the ledger and the data room are enough. If a column heading does not match, the template stops and asks. It needs no access to the target's systems, and it never asks for a password or a login code.

## What comes out

One schedule, in a fixed order: management's bridge from reported to adjusted EBITDA, as management states it; a summary of the adjustments by evidence status, with totals that add back to management's total; one block per adjustment showing ledger, calculation, explanation, documents, prior-year look-back, flags and questions; the questions for management, as a draft for the engagement lead; the decisions that are the engagement lead's; and what was not assessed.

A good schedule lets the engagement lead pick any adjustment and see in one place what supports it, what does not, and what to ask next.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), filed under mergers and acquisitions, where diligence on earnings is done.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where transaction-advisory and accounting firms test management's adjustments for a buyer, a seller or a lender.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where an investment team reviews a target's adjustments before it relies on an adviser's report.
- [Acquisitions & integration](https://fullypowered.ai/situations/acquisitions-and-integration/), when a business is being bought and its earnings are the basis of the price.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where a portfolio company's adjusted EBITDA is tested before an add-on purchase or an exit.

It stays apart from [client schedule to ledger reconciliation](https://fullypowered.ai/workflows/client-schedule-to-ledger-reconciliation/), which agrees a client's schedule to its own books, and from the [client document request tracker](https://fullypowered.ai/workflows/client-document-request-tracker/), which tracks what a client has sent. This one tests management's proposed earnings adjustments against their evidence.

## What has to change for your company

- **Your exports.** The column names your ledger exports and data room index produce. If a heading does not match, the template stops and asks rather than guessing.
- **Your categories.** Which of management's categories your firm treats as one-off and which as estimates, and the tie tolerance.
- **Your look-back.** One prior year by default; longer where the files allow.
- **Your roles.** Who runs it, who the engagement lead is, and who sends questions to the target.
- **Your question style,** so the list can go into your request tracker once the lead has reviewed it.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply. Given the confidentiality of a deal, decide which files the assistant may read and where the signed-off analysis is kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 11 November 2026. It was tried on its invented example in Claude on 11 November 2026; the record is published with it. After the run its wording was tightened following review; the example's inputs and figures were not changed. A later review pass made small further edits, including writing every date in the example's schedule in one style; the example was not run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a completed engagement whose adjustments your team has already worked through, plus hard cases written in advance, each with the expected result: an entry cited by two adjustments, a cost paid to the same supplier the year before, an estimate with no document for its assumption, an entry dated before the test period, a file with a heading it does not recognize. The engagement lead compares every tie and flag with the signed-off work before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 11 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 11 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Client schedule to ledger reconciliation](../client-schedule-to-ledger-reconciliation/)
- [Client document request tracker](../client-document-request-tracker/)
- [Client findings validation document](../client-findings-validation-document/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
