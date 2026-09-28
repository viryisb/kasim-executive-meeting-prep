# Kasim Executive Meeting Prep

A reusable AI skill for preparing concise, sourced Executive Meeting Briefs for Kasim Aslam. It turns participant and company research into meeting-relevant context, questions, potential opportunities and explicit unknowns.

The skill addresses a common preparation problem: extensive background research can obscure the actual meeting objective, while plausible connections can turn into premature recommendations. It filters information for decision relevance and keeps proposed actions proportional to the evidence.

## Structure

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Discovery metadata, invocation criteria, input handling, workflow and quality checks. |
| [executive-profile.md](references/executive-profile.md) | Kasim-specific research leads and thematic context; not a verified biography. |
| [executive-preferences.md](references/executive-preferences.md) | Default briefing standards, explicitly treated as working assumptions rather than confirmed personal preferences. |
| [research-rules.md](references/research-rules.md) | Source standards, recency, research budgets, stopping criteria and limited-evidence fallback. |
| [relevance-rules.md](references/relevance-rules.md) | Objective-based filtering and evidence requirements for recommendations. |
| [briefing-template.md](references/briefing-template.md) | Output structure, optional sections and practical brevity limits. |
| [examples/](examples/) | Included sample brief. |

## Inputs

- Participant name(s), plus an organization, role or profile link sufficient to establish identity.
- Meeting objective or desired outcome.
- Meeting date, if known, and any relevant context or materials.

The skill asks for missing objectives or ambiguous identities. A date is optional, and an organization may remain unknown if identity is otherwise clear. A provisional objective is used only when the user requests proceeding without one.

## Usage

Ask an AI assistant with access to this repository to follow `SKILL.md` and its linked references. Provide the participant and objective, for example:

> Use the Kasim Executive Meeting Prep skill in SKILL.md. Kasim Aslam is meeting with Job van der Voort, CEO and co-founder of Remote, to explore potential collaboration between Pareto Talent and Remote. Prepare the Executive Meeting Brief.

The repository contains instructions and reference material, not a standalone application. External research requires research tools available to the assistant. The default brief targets 350–500 words, with a 550-word maximum excluding a compact source list; shorter briefs are appropriate when evidence is sparse.

## External research

Research prioritizes primary sources and uses reputable independent reporting where useful. It verifies relevant roles, records a research cutoff and cites sources actually consulted. Recent developments normally cover the preceding 90 days, expanding to 12 months when needed; older foundational facts must have present relevance.

Search and source-read budgets prevent open-ended research. When tools or reliable sources are unavailable, the skill produces a clearly labeled limited-evidence brief based on accessible material, without implying current verification.

## Key guardrails

- The meeting objective takes precedence over Kasim's general thematic profile.
- Verified facts, user-provided context, inferences and unknowns remain distinct.
- Specific recommendations require supporting evidence. Unverified demand, budget, fit or sponsorship means actions are framed as hypotheses or options to explore.
- Sources, facts and tool use must never be invented; material contradictions and gaps are disclosed.
- Irrelevant biography, gossip and personal details are excluded. Working assumptions are not presented as confirmed facts or private preferences about Kasim.

## Testing and example

The skill was iteratively reviewed, tested with meeting-preparation scenarios and refined through feedback. Refinements clarified input handling, research limits, brevity and the threshold for commercial recommendations. These exercises do not establish the accuracy of every future output; each brief requires its own evidence checks.

See the [Remote / Job van der Voort example brief](examples/remote-job-van-der-voort-brief.md). It illustrates the output format and conditional collaboration options. It is a dated example, not evidence that a meeting or partnership occurred, and its research should be refreshed before reuse.
