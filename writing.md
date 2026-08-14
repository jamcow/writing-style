# Writing conventions — commits, issues, comments

Conventions for prose written *about* code: commit messages, issue bodies, issue and PR comments. Portable across projects. In-code comments are explicitly out of scope (see Non-scope).

## 1. Ubiquitous language (applies everywhere, no exceptions)

- If the repo has a `CONTEXT.md` (or equivalent glossary), use its terms in **all** artefacts: commits, issues, comments, code, in-code comments, docs.
- One term per concept. Never introduce a synonym for an existing term, even for variety.
- Respect the glossary's Avoid lists.
- If a needed concept has no term, propose one in the glossary first, then use it.

## 2. Sentence rules (STE-derived subset, not full ASD-STE100)

Apply where marked in §3:

- Short sentences. One idea per sentence. Prefer under ~20 words.
- Active voice. Name the actor ("The migration drops the column", not "the column is dropped").
- No metaphors, idioms, or figurative language.
- No -ing nominalisations as sentence subjects ("Retrying causes…" → "A retry causes…").
- One word per meaning within a document. Do not alternate "shows"/"proves"/"demonstrates" unless the epistemic difference is intended — and if it is intended, keep it.
- Concrete verbs over abstract ones ("removes" over "addresses").

Do **not** enforce the STE approved dictionary. The subset above is the whole rule.

## 3. Per-artefact scope

| Artefact | Sentence rules | Register |
|---|---|---|
| Commit subject + body | Full | Terse, factual |
| Issue: repro steps, expected/actual, environment | Full | Procedural |
| Issue: background, analysis, trade-offs | Loose | Normal prose; hedging allowed and meaningful |
| Issue/PR comments | Default habit, not enforced | Conversational; never rewrite others' or existing comments for style consistency |
| In-code comments | **None** | See Non-scope |

## 4. Length budgets (the verbosity lever)

Sentence rules control shape, not length. These control length:

- **Commit body**: explains *why*. Never narrates the diff — the diff is the diff. If the body restates what changed, delete those lines.
- **Issue comments**: conclusion in the first sentence. Supporting detail after. More than ~5 sentences must earn it (new evidence, a decision, a repro).
- **Issue analysis sections**: no hard cap, but structure over stream — lead with the current best hypothesis, then evidence.
- **PR descriptions**: what + why in the first paragraph; testing notes as a list; nothing else mandatory.

## 5. Non-scope

- **In-code comments**: exempt from all sentence rules. Comments that reason at length — about what a test can and cannot prove, why an approach was rejected, invariants — are the point. Do not flatten them. Ubiquitous language still applies.
- **Docs/README prose**: ubiquitous language applies; sentence rules are advisory only.

## 6. For Claude / automated agents

- Apply §1–§4 when writing commits, issue bodies, or comments in this repo.
- Do not retroactively rewrite existing issues or comments for style unless explicitly asked.
- When STE-style certainty would misstate confidence ("X causes Y" when it is a hypothesis), prefer accuracy over compliance: "X likely causes Y" is correct; keep the hedge.
- Hedges are load-bearing in analysis prose. Never strip them during a style pass.
