# Lumenette Hollow (working title)

**Project status: concept development / proposed specification.**  
**Repository:** hollowlumen  
**Implementation:** No runnable game, package manifest, or executable prototype is currently present in this repository.

> A gentle, craft-centered rural fantasy life sim about living yarn companions, cozy spaces, and short adventures. Designed to fit into real life rather than compete with it.

## The idea

In a quiet valley of mossy burrows and cottages lives a community of **Lumenettes**: expressive, glowing, living-yarn creatures. Players personalize a companion and a home, gather and craft materials, and optionally wander into the valley for small, curious adventures.

The original pitch suggested brief (1–5 minute) visits, optional (1–3 minute) excursions, bounded offline progress, friend visits, cosmetics, and a companion on a phone's home screen. Those ideas remain **concepts**, not evidence of implemented features.

## Product principles (proposed)

- **Respect the player's time.** Progress can be meaningful without daily obligations or punishment for absence.
- **Craft and express.** The home and the companion feel personally made.
- **Companionship over optimization.** Expressive character moments matter more than stat inflation.
- **Adventure by choice.** Outings complement the cozy game; they do not gate it.
- **Earn trust.** Platform capabilities, monetization, privacy, and feature status must be described accurately.

## Current design documents

| Document | Purpose | Status |
| --- | --- | --- |
| [Product and systems specification](docs/PRODUCT_SPEC.md) | Candidate requirements, core loop, technical boundaries, phased milestones, acceptance checks | Draft; product-owner review required |
| [Source audit and decision triage](docs/SOURCE_AUDIT.md) | Evidence, contradictions and decisions left unresolved by the original pitch | Documented findings |

The [original pitch is preserved at this pinned revision](https://github.com/cosmicdance-4-2-0/hollowlumen/blob/ac0317e250bef11c1f12abebe7be023aa41ecb47/README.md). Its claimed playable prototype, npm commands, completion checkboxes, and selected framework list were **not verified** because the tree contains no app source.

## Proposed first playable milestone

A single, complete loop: meet one Lumenette, decorate one cottage area, gather materials over time, craft one item, play one optional outing, save, and return. The first code milestone will not imply real multiplayer, purchases, or native battery widgets.

Before implementation, the product owner should resolve the key questions in the specification: core delight, target platform, how crochet works, visual style, battery integration, and any commerce boundary.

## Contributing and execution

This repository is at the **specification** stage. There is no currently supported install, test, or run command. Implementation instructions will be added only alongside a real build and verified checks.

Propose changes to the specification through reviewable branches or pull requests. Distinguish product decisions from engineering assumptions and do not mark features complete without runnable evidence.

**License:** Not selected. Do not assume code or art redistribution rights from the absence of a license.
