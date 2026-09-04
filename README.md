# ChasePad Client Readiness for Claude

ChasePad Client Readiness turns client proposals, briefs, scopes and kickoff notes into a tailored onboarding plan and an evidence-based readiness audit.

It helps agencies and client-facing teams identify missing assets, content, access, approvals, owners, dates, dependencies and true kickoff blockers before work starts.

## What the plugin provides

- A tailored client onboarding plan
- An evidence-based project readiness audit
- Clear kickoff blockers and next actions
- A copy-ready client request for outstanding items
- Project-specific checks for websites, UGC, retainers, brand, video, paid media, consulting and e-commerce work
- Secure access guidance that avoids requesting passwords or sensitive credentials

## How it works

The skill analyses the user's source material in Claude, separates confirmed evidence from assumptions, and prepares concise structured findings. The included remote MCP connection sends only those structured findings to ChasePad's renderer, which validates the result and calculates the readiness score deterministically.

The plugin does not create or update ChasePad records, log users into ChasePad, or require a paid ChasePad account.

## Remote MCP server

The plugin connects to ChasePad's hosted MCP endpoint through `.mcp.json`.

The renderer should receive only concise structured findings. Do not send raw proposals, full transcripts, credentials, passwords, tokens, or complete email threads to the MCP tool.

## Privacy

Source documents and project content are analysed in the connected AI assistant. The ChasePad renderer receives only the structured findings needed to produce the readiness result. See the bundled privacy and safety reference for handling rules.

## Plugin structure

- `.claude-plugin/plugin.json` — Claude plugin metadata
- `.mcp.json` — ChasePad remote MCP connection
- `skills/prepare-client-onboarding/SKILL.md` — onboarding and readiness workflow
- `skills/prepare-client-onboarding/references/` — readiness rubric, privacy rules, project adaptations and evaluation prompts

## Homepage

https://chasepad.com/client-onboarding-readiness

## Publisher

ChasePad — built by Sisi Ncube.
