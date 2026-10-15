### W8-1-tasks-db-hygiene.md
VOTE: PASS
EVIDENCE: One job (Tasks DB safe-write) with anti-job in description, 3-check create gate, mutate table, never-delete/never-invent-Due locks, schema traps named; 3.4KB.
IF FIX: none

### W8-2-who-method-hiring.md
VOTE: PASS
EVIDENCE: CEO-reserved hire/fire/offer/send, no invented names/comp/scores, must-have-below-min = Out with no averaging, 7-section pack that names gaps; 3.2KB.
IF FIX: none

### W8-3-atlas-hebrew-english.md
VOTE: FIX
EVIDENCE: Loader is only 6 locks plus a Notion fetch; no steps, no fallback if fetch fails, no anti-jobs, no sample, so a dry run without Notion has nothing to execute.
IF FIX: Add "Fetch fails → English-only draft, flag Hebrew skipped" plus a 2-line sample (one inner-circle line vs one investor line in transliteration only).

### W8-4-founder-context.md
VOTE: FIX
EVIDENCE: Gate 2 offers full/short/micro, but Step 2 only reads BLOCKS-FULL or BLOCKS-SHORT, so micro has no source; Step 4 scan misses family names, health, addresses, CUI, and deal terms from Gate 3.
IF FIX: Step 2 add "micro = trim of BLOCKS-SHORT, no new facts"; Step 4 scan the full Gate 3 list (family names, health/labs, addresses, phone, email, IDs, CUI, amounts/valuation/terms).

### W8-5-token-efficient-output.md
VOTE: FIX
EVIDENCE: Sprint example breaks its own rules: "- 1." / "- 2." are redundant ordinals (cut order), and it has 2 bullets while the Sprint budget says goal + 3.
IF FIX: Rewrite the example as plain "- " bullets with no ordinals and 3 bullets, or change the Sprint row to "goal + ≤3 bullets".

### W8-6-BLOCKS-NOTE.md
VOTE: PASS
EVIDENCE: One-line stub marking BLOCKS canon private (CISO G7); leaks nothing, makes no claims, 49B.
IF FIX: none

PANEL_SUMMARY: PASS=3 FIX=3 · TOP_FIX=W8-4-founder-context.md
