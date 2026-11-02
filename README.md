# Baking Notebook

> **Status:** developed in the open as a working record. This is work in progress: contents may change, and nothing here is peer-reviewed unless stated.

This repository is a versioned home-baking notebook. Its purpose is to keep
recipes, bake logs, pantry knowledge, technique notes, and sourced research in
one durable place so methods can improve over time through actual kitchen
experience.

The repo is not primarily a software project. It is a practical working system
for:

- recording recipes that worked,
- keeping experimental versions that are not yet reliable,
- logging what happened during each bake,
- storing sourced research and Codex-assisted advice,
- refining methods from direct human kitchen feedback.

## Working model

This repo assumes a simple division of labor:

- the human baker supplies observations, preferences, and final judgement,
- Codex helps structure notes, compare versions, suggest changes, and summarize
  research,
- the repository serves as the durable memory between baking sessions.

The most important evidence in this repo is not theory. It is what actually
happened in the kitchen.

## Current baseline

These are the starting assumptions for recipe development in this repository.

- Default leavening for yeasted doughs: instant dry yeast.
- Default chemical leavening: baking powder.
- Open to future work with sourdough starter, levain, baking soda plus cream of
  tartar, and unleavened flatbreads.
- Preferred fat: olive oil, unless butter is clearly more suitable.
- Rice flour is on hand mainly for dusting and handling dough.
- Standard yeasted bread format is usually a Dutch-oven loaf built around 750 g
  total flour.
- Standard quick-bread format is usually a cast-iron-skillet bake built around
  500 g to 650 g total flour.

## Current interests and direction

The repository has a few strong thematic preferences that should shape recipe
selection and future research.

- Historical baking is a major interest, especially bread traditions from
  medieval through Georgian periods.
- Recreating historical loaves is part of the intended long-term project.
- Mixed-flour breads are generally preferred over mostly pure white loaves,
  even when added flours appear only in modest percentages.
- Strong white flour often serves as the structural support for wholemeal and
  non-wheat additions rather than being the only flour in the loaf.
- Pure white breads still have a place, especially where style matters, such as
  baguettes and similar classic forms.
- Ancient-grain work is a future direction, including emmer, einkorn,
  khorasan, and related grains.
- Historical bread experiments may eventually range from ancient Near Eastern
  and Egyptian styles through Roman, medieval, and Georgian baking.

## Repository layout

- `inventory/`
  Current pantry and equipment records, including flour inventory and baseline
  baking materials.
- `recipes/`
  Stable recipes, in-progress recipes, and reusable templates.
- `bake_logs/`
  Dated records of individual baking sessions, including what changed and how
  the result was judged.
- `research/`
  Sourced notes from web research and Codex-assisted investigations.
- `techniques/`
  House notes on method, process, and evolving practice.

## How to use this repo

Typical workflow:

1. Create or update a recipe in `recipes/`.
2. Bake from that recipe, even if the result is imperfect.
3. Record what happened in `bake_logs/`.
4. Adjust the recipe only after the log captures the actual result.
5. Add research notes in `research/` when questions arise.
6. Update `inventory/` when new ingredients or equipment arrive.

This keeps evidence, interpretation, and revision separate.

## Kindle and EPUB

Recipes and research notes can be built as Kindle-friendly `EPUB` files.

Useful commands:

```bash
make kindle-list
make epub FILE=recipes/breads/modern/beginner-rustic-poolish-boule.md
make epub FILE=recipes/breads/modern/beginner-rustic-poolish-boule.md INCLUDE_RESEARCH=1
make kindle-init-config
make kindle-preflight FILE=recipes/breads/modern/beginner-rustic-poolish-boule.md
make kindle FILE=recipes/breads/modern/beginner-rustic-poolish-boule.md
```

Generated files land under `build/kindle/` and are not tracked in git. Kindle
delivery uses a local-only config at `.baking.local.yml`, seeded from the
existing creative-writer Kindle config when available. SMTP passwords are read
from the environment or macOS Keychain; they are not stored in this repo.

## Naming conventions

- Bake logs: `YYYY-MM-DD-short-name.md`
- Research notes: `YYYY-MM-DD-topic.md`
- Recipes: short descriptive names such as `basic-sandwich-loaf.md`

## Current pantry highlights

Initial inventory is recorded under `inventory/`, including:

- strong white bread flour,
- wholemeal wheat, rye, and spelt,
- quinoa, buckwheat, chickpea, oaten, and barley flours,
- cornmeal and blue masa harina,
- several commercial bread blends,
- instant dry yeast, baking powder, and baking soda,
- eggs, Greek yogurt, olive oil, and butter.

## What Codex should help with

This repo is intended to work well with Codex. Useful recurring tasks include:

- turning spoken or rough notes into structured bake logs,
- comparing recipe versions and identifying what changed,
- proposing controlled next experiments,
- searching for technique guidance and saving concise sourced summaries,
- helping map historical recipes into practical modern home-baking versions,
- tracking how mixed-flour and historical loaves differ from white-loaf baselines,
- helping turn repeated success into cleaner "house recipes".

## Next sensible steps

- Try the first researched loaf under `recipes/breads/historical/`.
- Record the first actual bake in `bake_logs/`.
- Start a short research note on one current question, such as hydration,
  proofing, shaping, or Dutch oven timing.
- Add a second historical or maslin-style loaf once the first trial is logged.

## Licence

Code is released under the [MIT Licence](LICENSE). Text, figures and data created for this project are released under [CC BY-SA 4.0](LICENSE-CONTENT). Third-party material keeps its own terms where stated.
