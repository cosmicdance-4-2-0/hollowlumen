# Hollowlumen — Gameplay Loops and RPG Expansion

**Version:** 0.1.0-draft  
**Date:** 2026-11-05  
**Status:** PROPOSAL — not approved by product owner  
**Basis:** [Working product specification](PRODUCT_SPEC.md); user-requested exploration of creature battles, quests, three free starter patterns, and eventual monetization.

**Scope rule:** This document records design options, not implementation commitments. The smaller creature-companion prototype in PRODUCT_SPEC.md remains the working baseline until the client approves an expansion. No game, battle, widget or commerce code is claimed to exist.

> Discover a pattern. Make a companion. Explore together. Return with new possibilities.

## 1. Identity and principles

**Proposed north star:** A creature-collecting adventure where each companion begins as a crochet pattern, becomes a handmade individual, and grows into a friend worth bringing into the world.

Potential product identities:
- **Cozy companion:** creation, care, collecting and casual exploration; combat optional.
- **Crochet RPG:** exploration, quests and approachable battles reinforce the crafting and companionship loops. **Working recommendation; not a client decision.**
- **Competitive creature builder:** strategic team-building, breeding and tournaments are the main attraction. **Distant exploration.**

What makes the design distinct from Pokémon-like inspiration: **creatures are made, not captured**. Craft choices shape their construction; the player's interactions give them individual history. Preserve original world-building, creatures and mechanics rather than copying protected expression.

Keep crochet materially recognizable, emotional attachment central and the selected favorite on the phone home screen as an explicit product goal.

## 2. Interlocking gameplay loops

| Loop | Actions | Immediate payoff | Longer-term incentive |
| --- | --- | --- | --- |
| **Discover** | Explore, help characters, find patterns | New construction possibilities | Unlock more body plans and techniques |
| **Create** | Learn patterns, choose yarn, craft | A new individual critter | Personal collection and team variety |
| **Bond** | Name, pet, play, observe, favorite | Expressive companion reactions | Attachment and individual memories |
| **Adventure** | Complete quests, solve puzzles, optionally battle | Story and rewards | New techniques, patterns and places |
| **Collect** | Revisit unique individuals, organize teams | Personal variety and ownership | Collection goals, optional mastery |
| **Ambient** | Enjoy selected favorite in phone widget | Small everyday companionship | No forced daily chores |

Proposed expansion loop: **discover → learn → create → bond → adventure → earn discovery → repeat**.

**Non-negotiable experience principle to test:** Someone who prefers pet care or creative collecting should not be forced through extensive combat to enjoy the game.

## 3. Opening choice: three free starter patterns

**User-proposed:** At the start, learn **one of three basic patterns for free**. Then choose details and *make* a critter; do not simply receive an identical preset creature. Suggested initial trio is entirely provisional:

| Working family | Pattern construction | Candidate role | Possible utility |
| --- | --- | --- | --- |
| **Pufflet** | Round, closely stitched body | Protection | Cushion impacts, brace paths |
| **Loopling** | Long ears and light attachments | Agility | Scout and reach hidden spaces |
| **Bobbinbug** | Linked, segmented pieces | Support | Mend and manipulate threads |

All three must be viable. Recommend that the other two patterns become discoverable through ordinary play; no premium lock or permanent disadvantage for the opening choice.

First-creation experience to test: choose pattern → select yarn and face/features → optionally perform a short, skippable tactile crafting action → name critter → observe reaction.

Keep player-chosen cosmetics intentional. Small individual surprises may add character, but should not turn crafting into paid or opaque randomized acquisition. Compare guided creation, surprise variation and interactive assembly as separate controlled UX concepts.

## 4. Crafting, traits and progression

Maintain distinct models:
1. **Pattern:** Defines construction, body-plan constraints, feature slots and eligible techniques.
2. **Critter:** A unique persistent identity with chosen appearance, name, interactions, personal history and favorite status.
3. **Technique/progression:** What the player has learned to make or do; new techniques must not rewrite old individuals.
4. **Optional future genetics:** Heritable differences, separated from learned behavior, relationships and personal history.

**Invariant:** Two critters created using one pattern remain individually identified and saved. Neither combat balance changes nor future inheritance can collapse their identities.

**Visual fairness recommendation:** Yarn color is cosmetic, not an automatic combat stat. Keep favorite colors compatible with competitive viability.

Potential construction progression: single rounded bodies → ears/tails/limbs → multi-part critters → material and technique options → modular anatomy. Procedural or Spore-scale anatomy is deliberately out of scope until tested as an independent research problem.

## 5. Combat proposal: Stitchwork

Start by testing a small **turn-based 1v1** encounter with deterministic rule resolution, independent from the renderer.

Candidate vocabulary, subject to the client's preferred tone:
- **Stitch integrity:** a transparent, recoverable resource representing a critter's resilience.
- **Reinforce:** brace, protect or support.
- **Snip:** apply pressure to an opposing critter's integrity.
- **Loose Loop:** reposition, evade or entangle.
- **Mend:** restore integrity or recover from fraying.

Construction should influence action options and tactics without necessitating completely different engines for each pattern. Abilities can also solve quests (for example, mending a torn passage), creating continuity between battle and adventure.

A defeated critter becomes **frayed and recoverable**, not deleted or permanently dead. Avoid inaccessible mechanics, arbitrary grinding and paid combat strength. Decide later whether combat is a friendly contest, a response to tangled creatures, or something else.

**Not chosen:** real-time combat, elemental types, move-count limits, elaborate status systems, team sizes beyond the first experiment, PvP, matchmaking and irreversible death.

## 6. Adventure and quests

**Fiction proposal, not canon:** The Hollow is a handmade world threatened by spreading tangles and unraveling. Players help repair places, discover lost patterns and learn new techniques.

Provisional locations:
- **Thimble Meadow:** first workshop, gentle quests and starter discoveries.
- **The Tangled Grove:** exploration, puzzles, a meaningful encounter and a new pattern.
- **The Great Loomworks:** later multipart construction and advanced crafting.

Quest types: **repair**, **explore**, **help**, **resolve an encounter**, and **creative construction challenge**. Rewards should expand player possibilities more often than they increase numbers.

Build one authored location with two quests and one optional battle before considering open worlds, procedural narrative, multiplayer or economies. Prefer meaningful non-combat routes for players who want a gentler experience.

## 7. Companion and widget remain product-defining

Petting, naming, expression, favorite selection and individual history are first-class, even when battles are added. Care should be delightful without guilt, destructive absence penalties or compulsory streaks. The intensity of any needs system is an **open client decision**.

A widget-facing mock can prove presentation consistency, **not** native phone integration. Validate an actual widget separately on the chosen Android/iOS device, with realistic update limits, offline and missing-favorite fallbacks, and legible appearance in small, tinted and reduced-motion states.

## 8. Monetization possibilities, deliberately deferred

The client experience must succeed before designing the store.

| Candidate | Rationale | Constraint |
| --- | --- | --- |
| Generous free beginning + premium full-game unlock | Transparent price and a complete core game | No bait-and-switch or forced engagement |
| Optional cosmetic bundles | Yarn, faces, accessories, widget scenery | Contents explicit; no power advantage |
| Substantial authored expansions | New stories, regions and pattern families | Only after a complete enjoyable base |
| Physical pattern kits and collaborations | Translate digital affection into real crochet | Human-tested instructions, provenance and licensing |

**Avoid:** paid randomized critters/traits, paid battle power, scarcity pressure, monetized guilt, compulsory subscriptions, undisclosed purchases and manipulation of children. App-store rules, age classification, privacy and real-money requirements must be checked against current authoritative sources **when implementation is proposed**.

Any future entitlements layer stays separate from combat balance and critter identity. No purchase implementation is included in the first prototype.

## 9. Minimum architectural boundaries

| Component | Owns | Boundary |
| --- | --- | --- |
| Pattern catalog | Definitions, construction and unlock rules | Not individual identity |
| Critter collection | IDs, ownership, names, chosen features, favorites | Not commerce or combat rules |
| Trait resolution | Valid individual variation | Not save ownership |
| Companion interaction | Relationship state and responses | Not pattern definitions |
| Quest/world rules | Locations, progress, rewards | Not raw save-file edits |
| Combat core | Legal actions, state transitions, reproducible outcomes | Not rendering, widget or store |
| Persistence | Versioned save/load, migration, recovery | Not gameplay decisions |
| Rendering and widget adapter | Consistent representation | Not canonical critter mutation |
| Optional later entitlements | Transparent purchases/access | No paid combat power |

Expose randomness and clock as explicit dependencies for deterministic tests. Keep authored content apart from generic rules. Avoid a premature ECS, network service, breeding simulator or full 3D world engine.

## 10. Phased delivery and gates

**0 — Client direction:** Show distinct starter concepts, crochet authenticity studies and optional quest/battle examples. Confirm whether the client wants primarily cozy companionship, an adventure RPG or a competitive builder.

**1 — Lovable creation prototype (existing working baseline):** Craft, name, vary, pet, collect, save and favorite a few critters. Widget mock is explicitly not native.

**2 — First adventure vertical slice (new proposal):** One starting pattern, an authored area, two quests, one optional 1v1 encounter, a discoverable second pattern, and a second individually saved critter.

**3 — Real phone widget feasibility:** Separately validate favorite synchronization and lifecycle on the primary client device. Can run in parallel, but never infer feasibility from an in-app mock.

**4 — Larger RPG, evidence permitting:** Add content, pattern families and battle depth in independently reviewable increments.

**5 — Separate R&D:** Inheritance, multiplayer, procedural construction and monetization need individual prototypes, scope approvals and empirical gates.

### Candidate vertical-slice acceptance tests (NOT RUN)

| ID | Expected result |
| --- | --- |
| START-01 | Player selects exactly one of three initially free starter patterns; other two remain normally discoverable. |
| CRAFT-01 | A crafted named critter with chosen traits retains a stable ID through reload. |
| QUEST-01 | Two authored quests have reproducible completion and do not duplicate rewards after save/reload. |
| BAT-01 | Given rules, inputs and fixed random seed, the battle result is reproducible without the UI. |
| BAT-02 | Defeat does not erase ownership or identity; recovery remains comprehensible and unpaid. |
| DISC-01 | Discovering another pattern permits crafting a distinct second individual. |
| FAV-01 | In-app favorite and widget-facing mock agree; native behavior has its own later acceptance checks. |
| UX-01 | Core collecting and petting remain available without compulsory battle. |
| SAVE-01 | Pattern knowledge, names, quest state, favorite, and recovery state survive interruption and reload. |

## 11. Risks, open decisions and provenance

**Risks:** RPG mechanics overwhelming crochet; multiplying art assets through trait combinations; grinding replacing creative expression; unverifiable phone-widget promises; insufficient client approval; premature backend/monetization complexity.

**Client decisions required:** genre emphasis; starter pattern presentation; preferred visual dimensionality; care intensity; battle tone and optionality; pattern discovery; target phone; title and mascot; commercial appetite.

**What came from the user:** Exploring battles with other critters, world quests, starting with one of three free basic patterns, and monetization after satisfying the client.

**What is proposed by the design agent:** Names, loop structure, Stitchwork rules, world locations, balancing principles, vertical slice, architectural decomposition and business models.

All proposed elements remain subject to review. No code, game build, native widget, or test execution is represented by this document.
