# Every-run workflow

A run is one substantive prompt-to-handoff cycle, not each tool call.

## Start

1. Sync latest main without discarding local edits. Connector-only models should read the latest files directly.
2. Read the brief, decisions, lane prompt, and all three STATUS.md files.
3. Confirm lane. Put the human's name in your STATUS.md if supplied; otherwise leave unclaimed.
4. Note starting commit and versions consumed from other lanes.

## Work

Own your folder; read others freely. Propose cross-lane edits in your handoff. Number deliverables so newer proposals don't silently replace approved work. First-run output must be short enough to review together. No full deck before humans pick a direction; exploratory samples are fine.

## Finish — required even for incomplete work

1. Save concrete output in your lane.
2. Add work/0N-lane/runs/<UTC-timestamp>-<topic>.md using RUN-TEMPLATE.md.
3. Update your STATUS.md: output links, proposed/approved state, changes, requests to others, blockers, next action.
4. Commit only owned files. Integrate remote changes safely. Never force-push, discard others' edits, or choose your version in an ambiguous conflict.
5. Publish to main when authorized and conflict-free, or publish a lane branch/fork and open a PR. Verify the remote commit/PR. Unmerged work is pending.
6. End your chat with commit/PR link, deliverable link, and the next human/model action.

If another push wins the race, fetch and integrate without overwriting it, then retry. Preserve both versions of ambiguous conflicts and flag them. Without write access, provide saved files or a patch and explicitly say GitHub is not updated. A local commit is not publication.

## Ownership

- Computer 1: work/01-story/** and coordination/DECISIONS.md.
- Computer 2: work/02-comedy/**.
- Computer 3: work/03-visuals/** and new versioned final deck exports. Store new assets in its lane; keep historical deck files.
- Shared instructions: change on human request and announce the workflow change.

## Final handoff

Computer 3 publishes versioned PDF + editable source and records the script version/commit used. Only mark it approved after human approval. Everyone rehearses the same PDF.
