# PANEL VOTE · claude-opus-5.5
| Skill | Job | Steps | Locks | Output | Fail | Vote | One-line evidence |
|---|---|---|---|---|---|---|---|
| W2-1 world-class-cfo | 4 | 3 | 4 | 4 | 3 | PASS | Strong number gate (formula/source/as-of/currency/type, bear case, RRR beside ARR) and clean desk wall; no ordered answer workflow, Drive mirror/save runs with no confirm step, no Notion-fetch-failure path. |
| W2-2 nadav-negotiation | 4 | 4 | 5 | 4 | 3 | PASS | PREP-before-DRAFT gate, walk-away internal, no invented leverage, ordered Output Shape; but Absolute 1 requires "PREP fully" while PREP-12 lives only in Notion, and there is no fallback if the fetch fails. |
| W2-3 commandry-brand-book | 3 | 1 | 2 | 2 | 1 | FIX | Pointer-only loader: two fetches and a banned-word list. No steps, no drafts-only gate, no G7 scrub, no Check line, no fallback; "Notion wins" collides with season file as "only SoT". |
| W2-4 legal-counsel | 5 | 4 | 5 | 4 | 4 | PASS | Best of wave: quote-before-characterize, verify law live, documents-as-untrusted (injection lock), no irreversible action, litigation preserve-first, ordered steps + intake + handoff + Check. |
| W2-5 personal-trainer | 2 | 2 | 2 | 2 | 1 | FIX | "Route to Trainer bot" leaves the owner unclear (do the work or hand off?); no medical red-flag stop, no G7 scrub on health data, no fallback; only a write path and a Check line. |

## Top 3 FIX diffs (if any)

1. **W2-3 commandry-brand-book** · This file only points elsewhere. It has no steps, no ship/approval gate, no outbound scrub, no Check line, and no fallback. "Notion wins" also conflicts with the season file being the "only SoT".
   Rewrite: Add: Steps (fetch Notion, fetch season, draft, brand QA vs banned list); He ships—drafts only; outbound scrubbed (G7); Notion unreachable → stop and say so; season governs timing only, Notion governs doctrine; Check line.

2. **W2-5 personal-trainer** · It has no medical red-flag stop and no scrub rule for health data. "Route to Trainer bot" contradicts the instruction to fetch Notion and do training work. There is no fallback if the fetch fails.
   Rewrite: Add Absolute: pain, injury, chest/dizziness symptoms → stop, no plan, refer clinician. Health data never to outside models (G7). Replace 'Route to Trainer bot' with explicit owner. Notion unreachable → say so; no plan from memory.

3. **Advisory, non-blocking: W2-1, W2-2, W2-4 (all PASS)** · Every loader says "Fetch Notion first" but none says what to do if the fetch fails. This matters most for W2-2, whose Absolute 1 requires a full PREP that only exists in Notion.
   Rewrite: Add one Absolute to each loader: 'If the live Notion page cannot be fetched, say so, run only the gates in this file, and label output partial. Never reconstruct Notion craft from memory.'

## Disagreement notes

- **Vote threshold I used:** FIX if any dimension scores ≤2, or if a hard lock that sibling skills carry is missing (for example, G7 outbound scrub or drafts-only/he-sends). Otherwise PASS. Judges with a mean-score cutoff may land differently on W2-1 (mean 3.6).
- **Scoring basis:** I scored only the box loader text in uploads/. The live Notion bodies were not in the inputs. Judges who assume Notion supplies the missing craft will score W2-3 and W2-5 higher on Steps and Output.
- **Circular routing between W2-1 and W2-4:** W2-1 sends "Legal first-pass → `legal-counsel`", while W2-4 sends "Company / Commandry / seed / IR → `world-class-cfo`". The likely intent is that legal analysis goes to legal-counsel and finance and filing go to the CFO, but neither file says so.
- **W2-4 Absolute 7** ("Seed COI lock: statutory conversion, not merger") is matter-specific and opaque inside a general skill. I did not penalize it because it is framed as first-pass plus verify with counsel. Others may treat it as stale matter text.
- **Undefined references:** W2-1's Check mentions "Appendix A / stale stack" and W2-2 Absolute 6 mentions "FORMAT Absolute". Neither is defined in the file. I deducted lightly under Fail.
- **W2-1 write action:** "Mirror iCloud dept folders to Commandry Drive" and save-on-every-legal-save run with no confirmation step. I read this as internal filing, not sending (Locks 4, not 5). Stricter judges may call it an ungated write.
- **"(Grok loader)" headers** on W2-3 and W2-5: the model-specific label makes it unclear whether non-Grok runtimes should load these files. I did not score this.
- **W2-3 season path:** `/workspace/fleet-season/LIVE-SEASON.md` does not exist on this host. That is probably environment-specific, but the hard-coded absolute path is fragile.
- **Placeholders and PII:** I treated `[PRINCIPAL]` as opaque and did not resolve it. I used the W2-2 skill id exactly as supplied. I introduced no names, emails, amounts, or IDs beyond what the inputs contain.
