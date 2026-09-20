# Read the repo. Route by name. Start the work.

This file is the entrypoint for a model whose user gives this GitHub URL and says their name.

Repository: https://github.com/patrick-finley/starship-retreat-pitch

## Name routing — authoritative

Match first or full name, case-insensitively. These are the latest explicit human assignments and supersede earlier chat proposals.

| Human says | Your job | Read and execute | Write in |
| --- | --- | --- | --- |
| Parker / Parker Tenney | Story | [01-story.md](prompts/01-story.md) | work/01-story/ |
| Patrick / Patrick Finley | Comedy | [02-comedy.md](prompts/02-comedy.md) | work/02-comedy/ |
| Nadav / Nadav Shoval | Brand + Deck | [03-visuals.md](prompts/03-visuals.md) | work/03-visuals/ |

Don't ask a named human to choose a lane again. If no name is supplied, ask only which of the three people you are working with.

## Read before producing anything

1. [AGENTS.md](AGENTS.md): repository instructions.
2. [BRIEF.md](BRIEF.md): actual prompt, tone, and latest human input.
3. [DECISIONS.md](coordination/DECISIONS.md): what is chosen, rejected, or open.
4. [RUN-RULES.md](coordination/RUN-RULES.md): sync and handoff rules.
5. All three status files: [Story](work/01-story/STATUS.md), [Comedy](work/02-comedy/STATUS.md), [Brand + Deck](work/03-visuals/STATUS.md).
6. Your lane prompt from the table, and any current deliverables it references.

Fetch current files from main, not an old cached summary. If you cannot read the repository, say exactly what access is missing; do not pretend to have read it.

## Execute

If your lane has no completed first pass, do its FIRST RUN assignment. If it already has outputs, continue the next action in its STATUS.md using current human decisions. Do not restart blindly or overwrite newer work.

- Parker produces premise options, then the chosen story and script; records human decisions.
- Patrick produces jokes and punch-ups, including the Forbes/YC material.
- Nadav produces funny names and logos, then visual identity and the PDF. His stronger Grok access belongs in this lane.

The original deck was rejected. Do not use it as a template. Exact jokes and brand ideas remain proposals until the team chooses them.

## End every run

Save concrete files, add a run note, update your STATUS.md, publish a commit/PR, and verify publication. Return links and the next handoff. Work that exists only in chat is not handed off. Missing write access does not excuse losing the work: save files or a patch, and clearly state that publication is pending.
