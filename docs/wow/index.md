# WoW

[Git Instructions](https://github.com/fanduel/sports-product-hub)

## Pod Charters
How to create:

1) Use the `/pod-charter` skill (interactive evaluation in Claude Code) <br>
Pressure-tests your problem statement <br>
Validates evidence <br>
Refines hypothesis <br>
Defines 2-3 success metrics <br>
Generates the charter PR <br>
2) Manual: Edit `templates/pod/charter.md` with: <br>
Mission type (product/platform/enablement) <br>
Customer problem (specific, not vague) <br>
Evidence and hypothesis <br>
Primary/secondary metrics with targets <br>
Pod lead and members <br>

What happens: Merged PR = pod officially created and appears in `pods/_registry.yaml`

## Initiatives

How to create:
Use the `/initiative-create` skill (scaffolding tool) <br>
Prompts for name, primary area, secondary areas <br>
Creates folder structure automatically <br>
Manual: Copy `templates/initiative/` to `surfaces/my-bets/initiatives/2026-q2-my-name/` <br>
Key: Tie initiatives to pods via `pod: pod_slug` in frontmatter

Structure: Initiative folder has 7 standard files:

| File | Purpose |
|---|---|
| `README.md` | Overview, problem statement, success metrics, links, frontmatter with status/RACI/pod |
| `spec.md` | Functional requirements, user stories, edge cases |
| `research.md` | User research, data analysis, competitive intel |
| `design.md` | UX/UI decisions, Figma links, interaction notes |
| `qa.md` | Product Q&A log — questions with resolved answers |
| `decisions.md` | ADR-style decision records |
| `status.md` | Current phase, timeline, blockers |

## How to Pick a Home for a New Initiative

| Question | Place it in |
|---|---|
| Is it a customer-facing screen or a feature on one specific screen? | `surfaces/<screen>/` |
| Is it a feature that appears on multiple screens? | `horizontal-experiences/<feature>/` |
| Is it backend or infrastructure with no direct UI? | `platform/<area>/` |
| Is it a staff-only tool (traders, risk ops, content ops)? | `internal-tools/<tool>/` |
| Is it tied to a time-bounded event or season? | `seasonal/<event>/` |

## Initiative file guide:

| File | Purpose |
|---|---|
| `README.md` | Overview, problem statement, success metrics, links, frontmatter with status/RACI/pod |
| `spec.md` | Functional requirements, user stories, edge cases |
| `research.md` | User research, data analysis, competitive intel |
| `design.md` | UX/UI decisions, Figma links, interaction notes |
| `qa.md` | Product Q&A log — questions with resolved answers |
| `decisions.md` | ADR-style decision records |
| `status.md` | Current phase, timeline, blockers |

____________________

## Available Skills

Skill	Purpose
|---|---|
|`/pod-charter`	| Create a pod interactively |
|`/initiative-create`	|	Scaffold a new initiative |
|`/one-sheeter`	|	Generate stakeholder summary |
|`/epic-refinement`	|	Decompose initiatives into epics |
|`/refinement-prep`	|	Pressure-test Jira stories |
|`/templates/initiative/`	| The canonical template for a new initiative. Copy this to start. |
|`/templates/example-initiative/`	| A fully worked example showing how a mature initiative looks. |
