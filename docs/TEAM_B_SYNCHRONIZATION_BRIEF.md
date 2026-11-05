# Hollowlumen — Team B Synchronization Brief and Design Branch Closeout

**Recorded:** 2026-11-05  
**Status:** DESIGN HANDOFF — exploratory work, not client approval or permission for a runtime rewrite  
**Audience:** Team B implementation agent, project coordinator and design reviewers

> The cottage is the heart. The player-created critters are its inhabitants. Adventures give creations purpose. Returning home gives the adventures meaning.

## 1. The design synthesis

Our new hypothesis is a **creature-crafting homestead adventure**. The player makes living crochet-inspired companions, gives them an expressive home, prepares for excursions, solves problems with material-inspired construction, and returns to a world changed by the experience.

This is **not** an instruction to discard the existing cottage simulator. Earlier research mistakenly opposed the cottage and adventure; the coordinator has explicitly directed us to explore both as complementary systems.

- **Create:** Patterns and construction decisions produce distinct, persistent individual critters.
- **Inhabit:** The critters live in a personalized cottage/workshop with a few observable preferences and behaviors.
- **Venture:** The player selects companions and supplies for challenges with understandable, optional risks.
- **Act:** Bounded Threadwork interactions could connect crafting, puzzles, repair and optional tactical encounters.
- **Return:** Quest outcomes can change a village route, visitor, workshop technique or home interaction.
- **Continue:** The chosen favorite can eventually inhabit a genuine native phone widget; a web mock is not proof.

We have a strong direction to **test**, not a fully accepted specification.

## 2. Two repositories, distinct responsibilities

| Repo | Function | State at preparation |
| --- | --- | --- |
| [cosmicdance-4-2-0/hollowlumen](https://github.com/cosmicdance-4-2-0/hollowlumen) | Product/design hypotheses and prototype SVG branding | Documentation only; no runnable game |
| [Kisuul/hollowlumen](https://github.com/Kisuul/hollowlumen) | Team B implementation | React/Vite cottage prototype, pure rules, local save, theme/solar integration |

**Team B snapshot:** Main revision cb209918e3f6fe6793564e4cb011b76854b65a1d, 2026-11-05. Re-fetch current HEAD before doing anything. PRs #1 through #6 were merged as of this review.

Team B has Home/Wander/Idle/Yarn/Shop routes; a customizable Pip SVG; persistence; day/night design tokens; independently configurable lighting and theme preferences; and a fictional solar calculation. On the PR #6 head, GitHub Actions reported **28/28 tests, 138 design checks, successful Vite build and Chromium smoke at 1280, 390 and 320 pixels**.

Outstanding review issues at the time of inspection:
- Designer signoff on the **rendered** Home/Pip appearance is not established by GitHub PR reviews. Palette acceptance alone is insufficient.
- A verified dependency lockfile was generated in CI, but had not been committed to main.
- Team B currently represents **one customizable Pip**, not an arbitrary collection of independently identified handmade critters.
- Battery/widget UI is a web demonstration, **not** an installed native widget.

Neither repository's current branches automatically import or override the other's source.

## 3. Design reading order and authority

Read these documents **as hypotheses**, not requirements:
1. [Playable Game Hypothesis](PLAYABLE_GAME_HYPOTHESIS.md) — small integrated game and concrete player decisions.
2. [Integrated Homestead and Adventure Vision](INTEGRATED_GAME_VISION.md) — the combined cottage, crafting, critter and frontier loops.
3. [Five-Game Mechanics Sieve](FIVE_GAME_MECHANICS_SIEVE.md) — interpretations of Stardew Valley, Minecraft, Don't Starve, Pokémon and Animal Crossing.
4. [Gameplay Opportunity Map](GAMEPLAY_OPPORTUNITY_MAP.md) — ideas, constraints, dependencies and falsifiable experiments.
5. [Client Review](CLIENT_REVIEW.md) — unanswered questions and approval provenance.
6. [Concept Demolition Review](CONCEPT_DEMOLITION_REVIEW.md) and [Gameplay Expansion](GAMEPLAY_EXPANSION.md) — competing encounter and progression proposals.
7. [Product Specification](PRODUCT_SPEC.md) — the **earlier** minimal, creature-first baseline. Its cottage exclusion was scope containment, not a permanent product veto.

User-directed expansion and the client's preferences define design exploration; **client-observed review and explicitly accepted decisions** define what is approved. A merged document or green build is not gameplay acceptance. The user reports the client enjoys five games, but the specific mechanics she prefers remain unknown.

## 4. B-01: proposed first engineering assignment (analysis only)

**Objective:** Design the smallest safe transition from one saved, customizable Pip into a **household of two independently identified critters** with a few furniture interactions. This checkpoint requests a proposal, not implementation.

### A. Review the existing architecture

Inventory each relevant source module, its responsibilities, persistence dependencies and interfaces. Mark what should remain stable: pure rules, React routes, existing saves, tests, palette system, solar presentation and SVG art approach. Separate actual blockers from simply missing functionality.

### B. Propose minimal data contracts

Define, without speculative engine complexity:
- **Pattern definition:** Stable pattern ID/version and allowed construction options.
- **Critter instance:** Unique ID, name, pattern reference, appearance, construction, bounded preferences and optional history.
- **Household:** Resident IDs, placements and furniture interaction affordances.
- **Favorite:** Stable reference to an existing critter and a minimal widget-facing projection.
- **World:** Optional separate quest/encounter state, without coupling to cosmetics or economy.

Do not conflate a learned pattern with an already created individual. Avoid an all-purpose state blob, hidden mutable variables, and premature AI behavior simulation.

### C. Write a save-migration outline

The existing single-Pip schema must migrate **without loss** of player name/color/face/accessory, yarn and upgrade economy, timers, decor, wander counters and existing saved preferences. Propose stable first-critter ID assignment, valid favorite reference, schema/version discipline, sanitation and idempotent restoration.

**Do not change the live save schema during B-01.** Include migration tests in the next implementation proposal.

### D. Propose the smallest inhabitation test

One room, two named critters, and three furnishings that support observable reactions (for example rest, inspect and play). Interactions should be authored/deterministic where necessary, visibly distinguishable, accessible and safe to reload.

The product question: **Does a reactive, individually inhabited space make the cottage worth revisiting more than a purely decorated room?** No LLM agents, full autonomous schedules, or relationship mega-system required.

### E. Map regressions and the next checkpoint

List threatened code/interfaces and tests, especially saving, economy, theme/solar separation, responsive routes and character rendering. Propose a narrow reviewable implementation PR only **after** B-01 approval. Identify blocked product decisions for the coordinator/client.

**B-01 exit artifact:** Short gap analysis; domain model and interfaces; save migration plan; tiny inhabitation implementation plan with tests; risks, open questions and scope tradeoffs. **No gameplay code change is authorized by this document.**

## 5. Frontier and later mechanical experiments (not B-01)

Future experiments can compare:
- One **construction-dependent** capability versus cosmetic-only customization.
- A Threadwork repair obstacle versus simple conventional tactical battle.
- A home consequence (visitor/route/new technique) versus currency-only rewards.
- An expedition with recoverable supply/fraying consequences versus a low-pressure version.
- Starter **patterns** versus introductory **crafting disciplines**.
- A small actual device widget versus an in-app widget preview.

The client may prefer a relaxed home, difficult exploration, or both. Do **not** infer a dislike of danger from lavender colors, or an appetite for harsh permanent loss from Don't Starve. Keep the cottage welcoming after absence; frontier stakes are an open design test.

## 6. Boundaries for synchronization

1. Fetch both repositories' **current heads** before any branch or file integration.
2. Port only consciously selected documentation/contracts; **never merge divergent forks wholesale**.
3. Preserve the Team B playable application, save format and established tests until a reviewed migration exists.
4. Keep UI theme, solar preview, gameplay timers and economy authority independent.
5. Distinguish **user direction, agent hypothesis, client approval, code implementation and verified tests**.
6. Review all artwork, identity, mechanics presentation and IP risks holistically. No direct imitation of another franchise's characters, iconic systems or creature-catching in balls.
7. No commerce, networking, native widget, procedural anatomy or expansive combat implementation is approved by this handoff.
8. Return Team B's B-01 assessment to the coordinator. Agree on shared minimum interfaces before opening parallel feature branches.

## 7. Closeout decision boundary

This document and its companion research complete **the exploratory design branch's documentation milestone**. It does **not** complete product specification, client evaluation or runtime implementation.

**Next cross-team synchronization checkpoint:** Compare Team B's B-01 architecture assessment with the design team's proposed critter collection, household and construction contracts. Choose a deliberately small gameplay experiment and create a separately authorized implementation milestone.

*The stage is built. We are starting to discover the play.*
