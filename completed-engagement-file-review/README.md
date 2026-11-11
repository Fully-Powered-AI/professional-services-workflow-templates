# Completed engagement file review

The quality partner gets a worksheet that tests finished engagement files against the firm's own checklist: each item linked to the engagement letter, workpaper or sign-off that answers it, with any open finding, and the missing evidence listed. The quality partner confirms findings and assigns remediation.

*Capability template · Professional services · Quality management · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/completed-engagement-file-review/)*

## The outcome

A file inspection usually starts with a partner opening folders one by one and asking the same questions again: is the engagement letter here, is the planning memo signed, did anyone review this before it went out. This capability asks those questions of every selected file in the same order, from lists you supply, and hands back one worksheet.

For each engagement the worksheet goes down the firm's checklist. Each item ends in one of three states: evidenced, check first, or missing. Evidenced means the file index lists the item and nothing about it raises a question. Check first means it is listed but something needs a person: a sign-off with no signer or date, a sign-off by the person who prepared the item, a sign-off dated after the engagement was completed, two items that both claim to be the one, or a finding from an earlier inspection that is still open. Missing means the index lists nothing for it; if an earlier finding is still open against a missing item, the item stays missing and the finding is shown with it, with a question for its owner.

A line at the top proves the counts add up. The worksheet then lists the missing evidence and the absent sign-offs across all the files, and ends with the decisions that belong to the quality partner.

The worksheet reads only what you supply. It does not open a workpaper, judge whether the work in it is sound, or say that any engagement meets professional standards. An absent sign-off is shown as absent; it is never recreated or filled in.

## Who starts the work, and when

The quality partner, or the practice administrator acting for them, starts it when the engagements for inspection have been chosen. It can be run again after the engagement partners have found what was missing. The quality partner confirms which results are findings and assigns remediation. The engagement partner answers the questions about their own file.

## What they supply

- **The firm's checklist,** one row per item: what must be on the file, what kind of evidence it is, the reference the firm's file standard gives it, whether it needs a sign-off, and which engagement types it applies to.
- **The engagements selected,** with client code, engagement type, completion date and engagement partner.
- **The file index for each engagement:** every item the file holds, with its kind, reference, title, who prepared it, its date, and who signed it off and when.
- **The findings log from earlier inspections,** with status, owner and the corrective action recorded against each.
- **A few settings:** the inspection name, today's date, the quality partner's role and whether a sign-off by the preparer is to be flagged, and which status means an earlier finding is closed.

If an export's columns are named differently from the ones the template expects, the assistant stops and asks which is which.

## What comes out

One worksheet in a fixed order. It opens with the counts and the line that proves them. Then each engagement has its own block: the checklist item by item, what the file index holds against it, any flags, any earlier findings on the same item, and the question for the engagement partner. After the engagements come the missing evidence, the absent sign-offs, the file items and findings that link to no checklist item, and the quality partner's decisions.

The worksheet changes no file and sends nothing. It is not an audit opinion and not a certification of compliance with any standard.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), where the quality partner tests files after the fact and needs the same test applied to each one.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), where the engagement file is the record of how the work was run.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where finished files for accounting, advisory and consulting engagements are inspected against the firm's own standard.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the checklist has been in use for years and the inspection is a regular cycle.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the partners can no longer see every file and need one consistent test.

It stays apart from two neighbours. [Audit evidence index](https://fullypowered.ai/capabilities/audit-evidence-index/) answers an outside request list from a document register. [Quality management review pack](https://fullypowered.ai/capabilities/quality-management-review-pack/) briefs senior leaders on measures. This one tests finished files against your own checklist. What the inspection teaches about the work itself belongs in [Project lessons review](https://fullypowered.ai/capabilities/project-lessons-review/).

## What has to change for your company

Start from your own checklist and your own file standard; the capability adds no items of its own. Fix the export columns once, so each inspection starts from the same files. Decide which engagement types each item applies to and which items need a sign-off. Decide whether a sign-off by the person who prepared the item is allowed, and whether a sign-off after the completion date is a question or acceptable. Say who confirms findings and who assigns remediation. Choose where the approved worksheet is kept and who sees it. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your document system.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it. After that run the instruction block, output format and example were clarified on points the run raised, changing no result in the example, and it was not run again. It has not yet been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three finished files the quality partner already knows well, with cases written in advance: a file with no engagement letter, a sign-off with no date, a planning memo that exists in two versions, a finding from the last inspection that is still open. The quality partner checks every link against the real files before anyone relies on the worksheet. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Audit evidence index](https://fullypowered.ai/capabilities/audit-evidence-index/)
- [Quality management review pack](https://fullypowered.ai/capabilities/quality-management-review-pack/)
- [Project lessons review](https://fullypowered.ai/capabilities/project-lessons-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
