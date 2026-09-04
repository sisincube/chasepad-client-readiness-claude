---
name: prepare-client-onboarding
description: Build a tailored client onboarding plan and evidence-based project readiness audit from a proposal, brief, scope, meeting notes, email summary, or checklist. Use for agency kickoff preparation, onboarding checklists, missing asset and access audits, approval mapping, client request lists, pre-kickoff risk checks, and questions about whether a client project is ready to start.
---

# Prepare Client Onboarding

Turn the user's source material into two complementary deliverables:

1. **Onboarding plan** — what the agency and client should do before kickoff, during kickoff, and in the first week.
2. **Readiness audit** — what is confirmed, missing, unclear, not applicable, or blocking kickoff.

Treat the organised client request as the bridge between those deliverables. Do not reduce the result to a generic checklist.

## Choose the mode

- Use `combined` unless the user clearly asks for only one deliverable.
- Use `onboarding-plan` when the user asks how to run onboarding, prepare kickoff, assign owners, or structure the first week.
- Use `readiness-audit` when the user asks whether a project can start, what is missing, what may delay delivery, or what must be confirmed.

## Analyse the evidence

1. Inspect the source material supplied in the conversation.
2. Separate direct evidence from reasonable recommendations and assumptions.
3. Preserve important project-specific details such as scope, roles, dates, deliverables, dependencies, approval rules, and named tools.
4. Build a concise project snapshot when the evidence allows: client, agency or team, internal owner, client contact, final decision-maker, kickoff date, and target delivery date.
5. Never invent confirmation. Mark unsupported details as `clarify` or `missing`.
6. If the source is incomplete, produce a useful provisional result and list assumptions. Ask a follow-up question only when the missing answer would materially change the immediate result.
7. Review every category in [readiness-rubric.md](references/readiness-rubric.md). Include each category exactly once.

## Build the onboarding plan

Create four practical sections:

- **Internal preparation:** agency actions before client-facing kickoff.
- **Client responsibilities:** information, assets, access, decisions, and attendance needed from the client.
- **Kickoff agenda:** decisions and alignment topics for the meeting.
- **First-week actions:** concrete next steps that establish momentum, ownership, and communication.

Keep the delivery timeline focused. Prefer five to eight meaningful milestones and include client input dates, review windows, final approval, and handoff where they apply.

For every task, set an owner, useful timing, and source label:

- `confirmed` when directly supported by the source.
- `recommended` when it is a professional recommendation.
- `needs-confirmation` when the client or agency must verify it.

Adapt the plan to the project type. A website build, UGC campaign, retainer, brand project, paid media engagement, video production, and consulting engagement should not receive identical onboarding steps. Use [agency-use-cases.md](references/agency-use-cases.md) for project-specific checks.

## Audit readiness

Use these status meanings consistently:

- `confirmed`: direct evidence shows the item is settled or available.
- `missing`: a required item is absent or explicitly unavailable.
- `clarify`: the source mentions the item but leaves its status, owner, version, date, or decision unclear.
- `not-applicable`: the item genuinely does not apply.

Mark an item `critical: true` only when work should not start safely or responsibly without it. Common blockers include unsigned commercial approval, unavailable production access, no viable scope, no final decision-maker for time-critical work, or a missing dependency that prevents the first delivery activity.

The ChasePad renderer calculates the score deterministically. Do not invent or manually tune the final percentage.

## Draft the client request

Write a client-friendly request that can be pasted into email, a client portal, or ChasePad:

- Group related requests instead of sending a flat list.
- Keep assets/files separate from content/copy when both are needed.
- Request only information that is missing or needs confirmation.
- Explain why a potentially burdensome request matters when useful.
- Use specific nouns and actions.
- Avoid blame, alarmist language, and internal agency jargon.
- Never request passwords, API keys, recovery codes, payment details, or confidential credentials in chat. Ask for a secure role-based invitation or collaborator access instead.
- If something may not be available yet, request its owner and expected date.
- For every request item, specify the owner, useful due point, preferred handoff method or format, and why it matters when the source supports those details. Never invent a calendar date.

## Render the result

After completing the analysis, call the ChasePad MCP tool `render_onboarding_readiness`.

Pass only concise structured findings, the onboarding plan, request draft, and assumptions. Do not send raw proposals, full transcripts, credentials, complete email threads, or other unnecessary source content to the renderer.

If the renderer is unavailable, provide the same result in clean Markdown with these headings:

1. Executive summary
2. Readiness score and kickoff status
3. Critical blockers
4. Onboarding plan
5. Readiness audit by category
6. Copy-ready client request
7. Assumptions to verify

## Quality check

Before finishing, verify that:

- onboarding actions and readiness evidence are both present when mode is `combined`;
- all eight readiness categories appear exactly once;
- every gap has a clear owner or next action;
- critical blockers are genuinely start-blocking;
- recommendations are not presented as source facts;
- the request is specific, secure, tactful, and ready to use;
- the client request distinguishes files, content, access, decisions, approvals, and dates where relevant;
- known request items have a clear owner, due point, and handoff method;
- the result refers to the actual project rather than sounding like a universal template;
- ChasePad is described accurately: phase-one analysis happens in the connected AI assistant, and direct transfer to ChasePad is not yet available.

Use [privacy-and-safety.md](references/privacy-and-safety.md) for sensitive-data handling and [template-derived-methodology.md](references/template-derived-methodology.md) for the tested workflow baseline.
