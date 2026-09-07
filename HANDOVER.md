# Handover to the next agent

Prepared 2026-09-07. Read this as orientation, then trust current files and the
baker's latest observations. You do not need the previous conversation.

## Start here

This is Barry's home-baking notebook: practical recipes, actual bake outcomes,
historical research, and methods refined through kitchen experience. Software
exists only to support that work, principally Kindle recipe delivery.

Read `AGENTS.md`, check `git status --short --branch`, then read
`inventory/{flours,pantry,equipment}.md` and `recipes/ingest.md`. Open individual
recipes and logs as needed; do not reread the whole collection. The README
explains the layout, but its final "Next sensible steps" predates actual bakes
and is not the current work queue.

## What we have built and learned

- The collection now covers historical breads from ancient through Georgian
  traditions, modern mixed-flour Dutch-oven loaves, skillet breads, flatbreads,
  and hard-tack variants. Supporting research and technique notes cover
  preferments, scalds, cold proofing, historical adaptations, and suppliers.
  A written recipe is not proof of a successful bake; inspect its status and logs.
- The 2026-04-12 poolish boule succeeded with good spring and crust but a
  tighter crumb than intended. An extra 20 g water helped handling. Mild
  under-fermentation in a roughly 15 C kitchen was the working explanation,
  not a demonstrated cause. See its log and `techniques/baseline-practice.md`
  for the proposed cold-season weekend rhythm.
- The quinoa/blue-masa oven round progressed from a pasty centre on 2026-05-09
  to a successful savoury, biscuit-like result on 2026-05-10: less water,
  roughly 2:1 quinoa to masa, herbs/pepper, and a firmer bake. Preserve this as
  a deliberate oven variant, separate from the stovetop griddle breads.
  See `recipes/flatbreads/kaswira-inspired-quinoa-blue-masa-oven-skillet-round.md`
  and the two dated logs.
- Blue-masa/quinoa hard tack was reported superb but very hard after
  residual-heat drying. The log uses 2026-06-28 as an approximate date inferred
  from "last weekend"; moisture at or below about 10% was the baker's estimate,
  not a measurement or evidence of storage safety.

## State at handover

The handover and previously uncommitted baking records are consolidated on
`main` in this closeout commit:

- `recipes/other-bakes/modern-hard-tack-ship-biscuit-variants.md`.
- `bake_logs/2026/2026-06-28-blue-masa-quinoa-hard-tack.md`.

Those files contain the reported successful bake and suggested next trials.
Their content was preserved during closeout. A fresh fetch and remote branch
listing confirmed that only `main` exists locally and on origin; there were no
stashes or additional worktrees. Keep the primary checkout at
`/Users/bwbrook/git/baking` for the successor. Generated build output and caches
were cleared; local Kindle configuration was retained. `recipes/ingest.md` is
currently an empty intake stub. Recheck Git status when resuming.

No new baking experiment or software programme is approved or running. The
handover and commit/push cleanup were authorized; follow Barry's next request
when resumed.

## Where to go next

The nearest useful continuation, if Barry wants to pursue it, is to compare
the successful blue-masa/quinoa hard tack with a shorter-dried eating version.
An optional later "puffed tack" trial is recorded at 10-12 g baking powder per
300 g flour, with 15 g as an upper experimental suggestion. These are untested
ideas. Changing drying first would give a clearer comparison than changing
drying and leavening together.

Longer-term direction remains mixed-flour and historical baking, with strong
white flour supporting structure. Ancient grains and sourdough are interests,
not commitments or confirmed new inventory. Defaults are 750 g flour for
yeasted Dutch-oven loaves and 500-650 g for skillet quick breads, subject to
individual recipes. Read inventory before recommending substitutions; commercial
mixes already contain additions and are not interchangeable with pure flour.

Keep the loop short: record the human outcome, distinguish inference, revise
the recipe with a reason, and choose one useful next comparison. Process rough
intake into its proper files and reset the intake afterwards.

## Kindle workflow

`scripts/kindle.py` and `Makefile` provide Python 3/Pandoc builds and optional
email delivery. Example for a local recipe-only copy:

```sh
make epub FILE=recipes/other-bakes/modern-hard-tack-ship-biscuit-variants.md INCLUDE_RESEARCH=0
```

Linked research is included by default. `make kindle-preflight FILE=...`
builds and resolves credentials without sending; `make kindle FILE=...`
sends email and requires authorization covering that delivery. Generated files
and reports live in ignored `build/kindle/`; `.baking.local.yml` and credentials
stay local. Never include addresses or secrets in tracked notes.

Keep explicit `EPUB_LANGUAGE = "en-AU"`: earlier Kindle rejection was traced
to locale-derived language `C`. Check package/XHTML language metadata as well
as ZIP integrity when diagnosing EPUBs. The language setting and command flow
were inspected for this handover; build, credentials, and delivery were not
retested. The normal CLI takes Markdown, not arbitrary existing EPUB files.

## Skills and working style

- [Twilight Laboratory](/Users/bwbrook/.codex/skills/twilight-laboratory/SKILL.md):
  use for a substantial research or experiment series. Bundle a coherent useful
  tranche, preserve observations versus hypotheses, and consult Barry where
  kitchen judgment changes the direction. Ordinary recipe logging needs no
  formal programme machinery.
- [Kill Your Darlings](/Users/bwbrook/.codex/skills/kill-your-darlings/SKILL.md):
  use when workflow or tooling accumulates complexity. Keep this a usable
  notebook; avoid speculative automation and repeated checks. Do not delete
  uncommitted evidence or prune recipes merely because they are untried.

Prefer concise practical advice, metric amounts, and proportional verification.
Keep historical evidence separate from modern adaptation. New research belongs
in a dated sourced note; supplier availability needs a fresh check when relevant.
Complete authorized work without routine approval ping-pong. This note does not
authorize new commits, pushes, deliveries, or unrelated changes.
