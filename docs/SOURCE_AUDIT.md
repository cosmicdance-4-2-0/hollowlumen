# Hollowlumen — Original Pitch Audit

**Checked:** 2026-11-05. **Baseline:** [main at ac0317e](https://github.com/cosmicdance-4-2-0/hollowlumen/tree/ac0317e250bef11c1f12abebe7be023aa41ecb47).

## Why this exists

At the inspected commit, the complete repository tree contained **one file: README.md**. Despite statements that it was a "playable prototype", listed npm commands and checked completed roadmap items, it had **no application source, package manifest, test suite, or assets**. The claims of implementation could not be verified.

The first spec reconstruction incorrectly made **cottage decoration, idle resource gathering, wandering, and a shop** the main game. The user then clarified the actual desired direction: **Tamagotchi-like living crochet critters**, collected by unlocking increasingly complex **patterns**, with a **favorite critter living on a phone home-screen widget**. Genetic variation, selective breeding, pure strains, and far-future Spore-like development were framed as possible depth. This correction is the basis of [PRODUCT_SPEC.md](PRODUCT_SPEC.md) v0.2.0-draft.

## Reusable information from the original README

| Original pitch element | Current treatment |
| --- | --- |
| Whimsical crochet/yarn creatures | Keep as the central world identity |
| Living expressive companions ("Lumenettes") | Keep concept; names remain provisional |
| Customizable colors, stitch faces and accessories | Relevant to critter appearance and variation |
| Friendly, relaxed tone | Keep as direction; exact care mechanics undecided |
| Short sessions | A useful option, not a forced genre mandate |
| A chosen companion in the phone widget | Promote as core product experience, subject to native platform feasibility |
| Cottage, garden, burrow, furniture, photo mode | Not part of the current core |
| Short adventure minigames, rare yarn and idle upgrades | Not part of the current core |
| Shop, VIP pack and monetized idle acceleration | Not part of the current core; paid power contradicted the original fairness claim |
| Browser battery level boosts | Not part of the current core; web availability and device incentives were suspect |
| Social visits, gifting, co-op | Not part of the current core |
| Proposed React / TanStack / Tailwind / Zustand stack | Not verified, not selected |
| "Playable prototype" and completed-roadmap checkboxes | Unsupported by the actual repository tree |
| License TBD | Still unresolved; do not imply redistribution permission |

## Product distinctions that matter

- **A crochet Pattern** defines structural possibilities. **A Critter** is a persistent individual created from a pattern.
- **Genetics** is a plausible optional mechanism for controlled variation among individuals, not a prerequisite for the first toy.
- **The favorite widget** is a core aspiration. A web page that displays a fake widget does not fulfill native Android/iOS integration.
- **Spore-like procedural morphology** is intentionally future exploration, not an architectural mandate.

## What the documentation changes prove

The documents can support a review of product intent, open choices and proposed tests. They **cannot** prove that any gameplay exists, that a native widget can already run, or that the product owner has endorsed all details.

The initial README remains available at the pinned baseline above. The new README and specification in the draft PR are revisions for discussion, not a release.
