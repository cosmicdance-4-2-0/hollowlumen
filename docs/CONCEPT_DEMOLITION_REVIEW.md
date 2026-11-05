# Hollowlumen — Zero-Sacred-Cows Concept Review

**Version:** 0.1.0-draft  
**Date:** 2026-11-05  
**Status:** CHALLENGER PROPOSAL — no client approval, implementation or playtest  
**Scope:** Deliberately question the prior [RPG expansion](GAMEPLAY_EXPANSION.md) without erasing its design history.  
**Source:** User-directed challenge to all assumptions and emphasis on independent expression rather than cloning a creature-collecting franchise. This report's hypotheses and example systems are assistant-authored proposals.

> What becomes possible when the player makes living companions from the same material that constructs the world?

## 1. The diagnosis

The existing RPG proposal has a **convergence risk**. Its individually defensible conventions — three starter creature families, role archetypes, turn-based battles, team composition, collection, quests, inheritance and tournaments — could collectively produce the recognizable shape of an existing monster-collecting RPG with crochet art substituted for fantasy monsters.

This is an **originality and product-identity concern**, not a legal finding. Common game mechanics and genre ideas cannot simply be assumed to be free of all patent, copyright, trademark, trade-dress or other legal issues. An independently designed combination matters both creatively and operationally.

**Retain the goals; challenge the mechanisms.** The desired experience still includes living crochet critters, meaningful individuality, gradual creative expansion, a world worth visiting, optionally competitive challenges, and a favorite critter living on the phone.

## 2. Six design assumptions to detonate

### A. Crochet as surface treatment

**Challenge:** A critter with V-stitch textures and conventional RPG statistics may feel like a reskin.

**Alternative:** Give the fictional world a small set of *textile interaction rules*: join, anchor, release, reinforce, stretch, mend, perhaps intentionally unravel. These are game abstractions inspired by crafting materials, **not a claim to accurately simulate physical yarn mechanics**.

**Test:** Can the exact same rule be useful when constructing a critter, exploring a location and solving an encounter?

**Failure signal:** Decorative "thread" language disguises familiar attack/defend/elemental gameplay without introducing distinct decisions.

### B. Species determine abilities

**Challenge:** Fixed creature species and class roles front-load player options into preassigned inventories.

**Alternative:** Construction choices influence capabilities. A dense body might endure pressure but resist stretching; flexible attachments might reach an object; joined components might allow independent manipulation. Use a **bounded, authored set of properties** rather than infinite simulated anatomy.

**Test:** Can players understand why a companion can perform an action by inspecting its construction, without memorizing an arbitrary species table?

**Failure signal:** Best builds become visually identical, color preferences have mechanical penalties, or customization creates content explosion.

### C. Collection means accumulation

**Challenge:** Hundreds of disposable variants can undermine attachment and create an overwhelming care burden.

**Alternative:** A small **workshop community** of individually named, persistent creatures, each available for companionship, adventures and optional collaboration. New creatures broaden the cast and creative possibilities, not merely a counter. No compulsory care schedules or guilt-based absence mechanics.

**Test:** Does the player care which specific critter accompanies them? Are duplicates meaningfully distinct without excessive randomized generation?

**Failure signal:** A player creates creatures merely to satisfy collection gates and then forgets them.

### D. Tactical interaction must mean reducing enemy HP

**Challenge:** Conventional combat can impose genre expectations and overwhelm a cozy creative identity.

**Alternative:** **Threadwork Encounters**, where the objective is to repair, stabilize, connect or deliberately reorganize a dynamic textile structure. A tension-filled knot, a failing bridge, or a spreading tangle can present turn order, scarce actions and multiple possible strategies without requiring a hostile creature.

**Test:** Does an environmental encounter produce legible decisions, uncertainty, and a desire to try another solution?

**Failure signal:** A puzzle reduces to "bring companion with ability X" or a trivial scripted sequence. Conversely, if Threadwork lacks engaging decisions, do not protect it from comparison with traditional battles.

**Competitive variant (distant):** Two players attempt different objectives on one shared material structure. Do not treat this as an approved networking feature.

### E. The opening choice must be three starter species

**Challenge:** Three fixed starter creatures with familiar tank/agility/support roles reinforces the genre silhouette.

**Alternative:** An opening choice of one of three **crafting disciplines**, provisionally **Shape**, **Flow** and **Join**, corresponding to durable volumes, flexible attachments and component connections. The choice determines an initial technique; players construct their own first companion and may eventually learn the other disciplines.

**Test:** Does choosing a technique make the first critter feel *created* rather than selected from a catalog?

**Failure signal:** Discipline choice is too abstract for a new player; the original three visibly distinct starter patterns prove clearer and more delightful. There is no dogma against three choices.

### F. Genetics is the obvious route to deep variation

**Challenge:** Breeding poses a fiction problem in a world where companions are consciously crocheted into existence, and may incentivize repetitive random rolls.

**Alternative:** **Pattern lineage**: players modify a learned pattern and save a named derivative. Improvements or experiments become part of the player's creative tradition. Multiple individuals can still derive from the same versioned pattern; none lose their individual identities. Conventional inherited traits can remain a separate research track if they later prove valuable.

**Test:** Is branching a pattern personally rewarding and understandable? Can it create meaningful differences with a manageable art budget?

**Failure signal:** The player experiences lineage merely as editing technical parameters; genetically inherited surprises may be emotionally more engaging. Compare, don't presume.

## 3. Proposed replacement loop: make → understand → intervene → return

| Phase | Activity | Player reward |
| --- | --- | --- |
| **Learn** | Discover a technique or see a problem in the world | Curiosity and a new possibility |
| **Construct** | Craft a companion or modify a versioned pattern | Authorship, appearance, capabilities |
| **Connect** | Name, pet, observe and choose a companion | Personal attachment |
| **Intervene** | Resolve a Threadwork encounter, help a resident or explore | Meaningful application of craft decisions |
| **Discover** | Recover a technique, pattern insight or place | Expanded expressive vocabulary |
| **Return** | Revisit the workshop and favorite widget | Continuity and satisfaction |

This is a **challenge to the previous adventure loop**, not an approved replacement. A player interested only in companionship should have worthwhile interactions without participating in tactical encounters.

## 4. The world: one modest fiction with mechanical consequences

**Example only:** The Hollow is a world of stitched materials. Sections become tangled, seams loosen, paths fray, and former construction methods are forgotten. Its inhabitants need intervention, not necessarily conquest.

**The Bridge That Forgot Its Knot** is a candidate first encounter. A damaged bridge separates a villager from the workshop. Plausible solutions depend on what the player understands:
- Use an **anchor** to stabilize remaining strands and reconnect the route.
- Use a **flexible companion** to reach another attachment point.
- **Trace the loose thread** downstream and find an alternative route or a recoverable technique.

These must not silently collapse to equivalent button presses. Each solution needs discernible tradeoffs, feedback and consequences within a small authored simulation. A no-combat solution should be a real route, not a disguised mandatory fight.

No claim is made that these interactions are unique in all games, physically authentic to actual crochet, or already validated as fun.

## 5. Minimal interaction model, not a universal yarn engine

The strongest architectural opportunity is a **shared, small construction vocabulary** used by creation, exploration and optional competition.

**Candidate minimal domain concepts:**
- **Part:** authored body or environmental component with a stable identifier.
- **Connection:** explicit relationship between parts; may be anchored, joined or loosened.
- **Property:** small documented set such as durability, flexibility, reach and attachment capability.
- **Action:** a verified operation such as join, anchor, release, reinforce or mend.
- **Encounter state:** the set of components, constraints and goal conditions at one moment.
- **Critter identity:** separate from parts and pattern versions; persistent regardless of component modifications.

Start with a fixed set of parts and a small number of deterministic actions. This is not a mandate for rope simulation, procedural mesh construction, physics solvers, a large ECS, a node editor, or an open-world simulation.

**Key invariants to test, not yet implemented:**
1. An individual critter ID is stable across save/load, pattern revisions and non-destructive encounters.
2. Legal actions change only explicitly modeled state; invalid actions do not corrupt ownership or history.
3. The same action and preconditions produce the same outcome when repeated with the same explicit inputs and random seed, if randomness is used.
4. Rendering and widget snapshots cannot silently mutate authoritative critter or encounter state.
5. Undo/recovery rules are explicit and testable where actions can damage cherished creations.
6. Player-chosen appearance remains possible without a forced competitive handicap.
7. Encounter goals can have more than one authored solution where promised.

If an elegant construction system creates no useful fun, remove it. **The rules earn their complexity through observed play.**

## 6. Comparison experiment rather than premature commitment

Build two **deliberately tiny** interactive encounter sketches sharing the same creature, art budget and interaction time:

| Test | A: Conventional battle | B: Threadwork encounter |
| --- | --- | --- |
| Player objective | Defeat one opponent through legal actions | Stabilize a bridge or resolve a knot via material interactions |
| Shared assets | Same critter, visual quality, device and onboarding effort | Same critter, visual quality, device and onboarding effort |
| Mechanics | Simple deterministic turn/action exchange | Small deterministic connection/property action set |
| Observe | Clarity, strategy, satisfaction, replay interest | Clarity, strategy, satisfaction, replay interest |
| Differentiation | Familiarity may make onboarding easier | Material rules may create more distinctive gameplay |
| Key failure | Feels like a genre reskin | Feels like a forced puzzle or opaque simulator |

**Do not hard-code "B wins".** Ask whether the client voluntarily wants to repeat each. Observe without coaching. A third possibility remains valid: **neither**, with the game remaining primarily about making, bonding and exploring.

Other small comparisons:
- **Three starter species/patterns vs. three crafting disciplines.** Evaluate clarity and authorship.
- **Random traits vs. versioned pattern lineage.** Evaluate delight and comprehension without creating unnecessary art.
- **Large inventory vs. small workshop cast.** Evaluate attachment and management effort.

Define the task and observation notes in [CLIENT_REVIEW.md](CLIENT_REVIEW.md). No tests have yet been executed.

## 7. What survives, what changes, and what remains open

| Existing direction | Provisional disposition | Reason |
| --- | --- | --- |
| Crochet companions with individuality | **Retain** | Central emotional foundation |
| Favorite living on phone home screen | **Retain** | Product-defining aspiration; native feasibility still unproven |
| Patterns and gradual unlocking | **Expand** | Strongest original progression hook |
| Purple/pastel Lavender & Loop art | **Retain as visual candidate** | Client aesthetic preference, not a signed-off brand |
| Three prebuilt starter families | **Challenge** | May be less authored than choosing techniques |
| Standard HP battle loop | **Test against Threadwork** | Could make the game feel derivative |
| World quests and exploration | **Retain; rebuild around material rules** | Opportunity to unify fiction and mechanics |
| High creature count | **Question** | A meaningful cast may work better |
| Genetic breeding | **Defer; compare to pattern lineage** | Fiction, scope and random-grind risks |
| Multiplayer and procedural anatomy | **Defer** | No evidence warrants infrastructure |
| Monetization | **Later validation only** | Should not distort the core experience |
| Real crochet pattern tie-ins | **Research opportunity** | Must be physically constructible and independently tested |

## 8. IP differentiation and legal boundary

**User intention:** Avoid directly cloning an existing franchise's creative expression, distinctive product direction and recognizable combined choices. In particular, **do not use a system of capturing wild critters in balls** as the default acquisition method.

**Design implications:**
- Companion origin is **making**, not capture.
- Original names, creature silhouettes, animations, interface vocabulary, lore, world geography, combat expression and visual identity must be developed independently.
- Do not reproduce another franchise's signature creature presentation, progression, badges, battle framing, iconic devices, or other recognizable combined expression merely with new yarn artwork.
- Track references and design rationale so similarities can be consciously identified and challenged during review.
- Avoid assuming that a single cosmetic change (such as removing capture balls) is a guarantee of differentiation.
- Mechanics may inspire independent design, but **no legal non-infringement guarantee** follows from calling an idea a mechanic. Copyright, trademarks, trade dress, patents and applicable jurisdictions may raise distinct questions.

**Commercial gate:** Conduct appropriate independent IP/trademark/patent clearance with qualified counsel before release. This document is product-design analysis, not legal advice or an assertion that any specific competitor owns or infringes any right.

## 9. Monetization with the emotional core intact

Commercial possibilities remain: transparent full-game unlock after a meaningful free opening, optional plainly described cosmetics, substantive authored expansions, or genuinely tested physical crochet patterns/kits with proper licenses and maker involvement.

Reject a business design where battle power, preferred physical appearance, desired critters, crafting creativity, recovery from loss or avoidance of guilt are sold as artificial relief.

The client should first enjoy the game; then test actual willingness to pay. The prototype requires no store, payment SDK, account service or monetized timers.

## 10. What to show the product owner

The client need not read this document. Show concrete, neutral comparisons: starter selection, one tangible critter, one environmental Threadwork problem, one simple conventional battle, and a widget preview honestly marked as a mock. Record what she actually chooses and returns to, not what the team hopes she'll endorse.

We are testing **what makes Hollowlumen itself**, not whether it can technically contain every popular genre mechanic.

## 11. Decision and handoff

**Observed from prior dialogue:** The user asked to question every earlier choice, avoid direct cloning and recognizable combined franchise direction, while allowing exploration of common gameplay mechanics. Capture balls were explicitly rejected.

**Proposed by design review:** Material-driven interaction rules, construction-derived abilities, a workshop community, Threadwork encounters, technique-focused starters, pattern lineage, and paired A/B prototype experiments.

**Not approved:** The challenger direction is **not** the new product canon, and does **not** deprecate the [previous RPG proposal](GAMEPLAY_EXPANSION.md) or [small companion baseline](PRODUCT_SPEC.md). The three are deliberately preserved for comparison.

**Next reviewable checkpoint:** Create two tiny comparable interaction prototypes and an accessible client review, ideally with one visually authentic crochet critter and a single clear objective in each. Preserve the original favorite-widget promise. Select the next implementation only after feedback and risk review.

**Outcome:** Concept analysis recorded; no runtime built, no test executed, no client approval inferred.
