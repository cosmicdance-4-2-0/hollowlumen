# Hollowlumen — Gameplay Opportunity Map / Kitchen-Sink Register

**Version:** 0.1.0-draft  
**Date:** 2026-11-05  
**Status:** Idea inventory and dependency analysis; **not** a roadmap or implementation authorization  
**Companion:** [Integrated Game Vision](INTEGRATED_GAME_VISION.md), [Client Review](CLIENT_REVIEW.md)

The user asked what more could be done and where, without treating the cottage and the adventure as alternatives. This document captures the broad design space **while separating a fun possibility from a justified engineering investment**.

## 1. Organizing principle

A feature is attractive if it supports at least one of these player desires:

1. **Make:** Express creativity through creatures, patterns, objects and spaces.
2. **Care:** Build attachment to particular companions and a lived-in home.
3. **Discover:** Learn what is possible and where to go next.
4. **Act:** Make informed choices with visible consequences.
5. **Share (optional):** Show work or collaborate without making social play compulsory.

Prefer mechanics that connect multiple locations. Reject features that exist solely to fill a genre checklist.

## 2. At home: opportunities and risks

| Location/system | Possible gameplay | Useful connection | Question / failure risk |
| --- | --- | --- | --- |
| **Workshop** | Critter construction, component assembly, repair, accessories, pattern experiments | Mechanics used in exploration | Does making feel like creativity or a tedious sequence? |
| **Pattern library** | New patterns, comparisons, versioned variants and lineage | Discoveries become craft choices | Is it intuitive to non-crocheters? |
| **Garden** | Fictional fiber plants, dye ingredients, habitat choices, gentle harvesting | Material supply and resident stories | Does it devolve into a harvesting chore? |
| **Crafting room** | Decorations, furnishings, tools, commissions | Useful rooms and expedition options | Does every craft become a currency transaction? |
| **Living room** | Petting, observing individual quirks, social interactions, display | Stronger identity and personal history | Is behavior meaningful or random wallpaper? |
| **Yard/test area** | Practice anchors, reach, reinforcing and simple obstacles | Low-pressure onboarding for Threadwork | Is it fun or only a tutorial? |
| **Attic/observatory** | Exploration clues, collectable observations, day/night spectacle | Discovery and presentation | Does astronomical detail add play or only costs? |
| **Porch** | NPC visits, optional commissions, postcards, gifts | World events return home | Are requests varied without demanding check-ins? |
| **Furniture layout** | Expressive placement; some pieces host interactions | Visible personalization | Avoid statistically optimal ugly decor |

**Possible early winners:** workshop + resident interactions + porch request + one expressive decoration. Others remain expandable content slots.

## 3. Out in the world: activity catalog

| Activity | Example objective | Shared mechanic | Candidate session |
| --- | --- | --- | --- |
| **Threadwork puzzle** | Repair a bridge or redirect loose fabric | Anchor, join, reinforce, release | Short or extended |
| **Exploration** | Discover a route, hidden pattern or rare material | Traversal, observation, construction | Medium |
| **Commission** | Make something fitting a resident's constraints | Pattern selection and creative tradeoffs | Short |
| **Rescue** | Reach someone through a failing structure | Companions and world state | Medium |
| **Restoration** | Rebuild a path, garden or district | Persistent quest outcomes | Medium to long |
| **Tactical contest** | Outmaneuver an opponent in a shared structure | Deterministic encounter rules | Short to medium |
| **Creature battle** | Friendly 1v1 or more elaborate encounter | Construction-derived actions if warranted | Short |
| **Expedition** | Choose equipment, companions and route | Preparation and authored challenges | Long |
| **Festival** | Enter creative displays or friendly Stitch-offs | Creation + optional mastery | Short |
| **Guild/craft lesson** | Learn a regional construction tradition | Techniques and content progression | Medium |
| **Photography/diorama** | Pose critters against restored scenery | Renderer, appearance, saved snapshot | Short |

**First experiment:** One authored objective with at least two mechanically different approaches, plus a directly comparable traditional encounter to test whether combat belongs.

## 4. Critter systems: make individuals matter

| Concept | Potential value | Dependency / caution |
| --- | --- | --- |
| Stable individual IDs and names | Persistence and attachment | **Foundational** collection/save design |
| Personal reactions and preferences | Companionship | Requires bounded behavior grammar, not LLM or autonomous AI |
| Favorite widget projection | Emotional continuity across app boundary | Real device integration separate from UI preview |
| Household routines | Sense of a living cottage | Avoid punishment, excessive ticking or state complexity |
| Social bonds | Observable small interactions | Avoid combinatorial relationship simulation |
| Expedition roles | Practical value for construction choices | Must not reduce companions to equipment |
| Pattern lineage | Player-made versions and creative history | Pattern schema versioning and source provenance |
| Fictional genetics | Emergent inheritance, selective traits | Compare against lineage before building |
| Procedural anatomy | Deep expressive possibility | High technical and art risk, isolated R&D |
| Physical crochet correspondence | Real maker community and potential kits | Human testing and actual stitch feasibility |

**Important:** More creatures is not automatically better. A smaller household of meaningful individuals may be a stronger emotional product than a large disposable inventory.

## 5. Reward ecology

| Reward | Feeds | Anti-pattern to avoid |
| --- | --- | --- |
| Materials | Crafting, dyes, décor, tools | Single all-powerful resource that turns game into farming |
| New techniques | Construction and problem-solving | Generic +5% upgrades presented as knowledge |
| Pattern variants | New personal creations | Cosmetic-only unlock disguised as major progression |
| Relationships | Expressions, behaviors, memories | Guilt over time away |
| World changes | Open routes, residents, services | Quest flag with no noticeable consequence |
| Aesthetic home progress | Creative freedom, community display | Optimization forcing players to reject their tastes |
| Optional mastery | Tournaments, puzzle scores, competitions | Competitive grind gatekeeping cozy play |

**Idle-system adaptation:** Residents can perform small optional household actions while away. Separate the passage of time from the player's worth, the world lighting from rewards, and material availability from paid relief. No unapproved economy rewrite follows from this inventory.

## 6. Social, community and commercial possibilities (later)

| Idea | Why it might fit | Gate before committing |
| --- | --- | --- |
| Asynchronous workshop visits | Show individual craft work without live networking | Privacy, moderation and user consent |
| Cooperative Threadwork | Players combine material techniques | One compelling solo encounter first |
| Sharing authored patterns | Creative community and lineage | Content validation, abuse/moderation, attribution and versioning |
| Decorating showcases | Visual expression and photography | Accessible capture/export and user-control |
| Cosmetic packs | Distinct looks, no combat advantage | Demonstrated value and clear commercial policy |
| Premium full-game unlock | Simple, predictable pricing | Complete enjoyable free slice and market testing |
| Story/region expansions | Ongoing authored adventures | A proven base game and sustainable production |
| Real crochet patterns/kits | Connect digital critters to physical craft | Legitimate, human-tested patterns and licensing |

Avoid paid power, paid randomized traits, coercive scarcity, compulsory subscriptions and punitive idle timers. No commercial or networking feature is an approved MVP requirement.

## 7. Shared foundations and dependency order

These are **candidate interfaces**, not a command to construct a mega-framework:

| Foundation | Supports | Earliest proof |
| --- | --- | --- |
| Stable critter identity + safe save migration | Cottage residents, collection, adventure, widget | Two named individuals survive reload |
| Pattern/technique data | Critter creation, commissions, discoveries | One new pattern produces a distinct build |
| Bounded construction action rules | Crafting, Threadwork and tactical contests | Same legal action helps in workshop and encounter |
| Explicit quest/world flags | Repair/restoration, returning visitors | Bridge stays repaired after reload |
| Scene/theme presentation | Cottage ambience, exploration, widget art | Readable day/night on actual screens |
| Reusable rendering contract | Avatar, workshop preview, portrait, widget | One critter stays recognizable at multiple sizes |
| Material rewards, if needed | Optional idle, exploration, decorating | Progression does not require passive grinding |
| Separate external adapters | Native widget, possible sharing, commerce | No app/game rules modified by visual state |

**Engineering priorities:** Preserve stable save behavior, test determinism, and avoid binding the renderer to the economy. Current [Kisuul/hollowlumen](https://github.com/Kisuul/hollowlumen) work provides potentially reusable pure state helpers, theme tokens, SVG rendering, and solar lighting. Specific API changes require an implementation proposal and regression tests against current saves.

## 8. Proof before scale: ranked experiments

| Experiment | Smallest artifact | What it could falsify |
| --- | --- | --- |
| **E1: Make one critter** | One chosen pattern, two meaningful structural options, name/save | Construction choices may not be enjoyable or clear |
| **E2: Meaningful encounter** | Bridge problem with two distinct solutions | Threadwork may be trivial, opaque or not replayable |
| **E3: Comparative combat** | Same critter/art, simple 1v1 alternative | Traditional combat may fit better or worse than expected |
| **E4: Return home** | Quest result affects an NPC, location or workshop ability | Adventure might not strengthen the cottage loop |
| **E5: Resident character** | Two individuals with distinguishable reactions | Extra critters may feel like interchangeable inventory |
| **E6: Starter framing** | Three patterns versus Shape/Flow/Join entry | Technique choice may be too abstract |
| **E7: Widget glanceability** | Favorite mock at small sizes, then native device spike | Appearance or platform may not support the desired promise |
| **E8: Garden/idle utility** | One resident household action, one optional material source | Idle loop may distract from active play |
| **E9: Pattern lineage** | Save two named variants of one pattern | Iteration may feel like editing parameters, not discovery |

The experiments need not run in this order and can reuse assets. They should be **reviewable individually**. Favor the first that reveals whether the integrated loop is fun.

## 9. Avoid the kitchen-sink trap

An idea remains **PARKED** until it has:
- A player motivation and a clear place in the loop.
- A visible action/feedback/reward or emotional payoff.
- A concrete minimal demonstration.
- Dependencies and failure conditions.
- Product-owner direction and scope approval.
- A regression-aware implementation plan if it touches established code.

No early commitment to massive open world, universal yarn simulation, procedural creature meshes, social graph engines, live PvP, dynamic marketplaces, subscriptions, or a scripted campaign containing dozens of quests.

**The goal of this register is to preserve possibilities without converting possibility into technical debt.**

## 10. Provenance and open status

**User-established:** The cottage and adventure should be considered together; design can expand while client approval remains the final gate; the user's two teams may share a coherent product direction; originality must be preserved.

**Assistant-proposed:** Home locations, specific gameplay catalog, encounters, experiments and architectural order.

**Not approved or tested:** All individual features in this document except for any separately established existing prototype functionality in the implementation repository. This document does not alter either repository's code or mean the other team has accepted these ideas.

## Addendum — cross-game mechanics and resident inhabitation (2026-11-05)

The [Five-Game Mechanics Sieve](FIVE_GAME_MECHANICS_SIEVE.md) adds inspiration from Stardew Valley, Minecraft, Don't Starve, Pokémon and Animal Crossing, with the last serving as a **hypothesis about inhabiting a personal space**, not simply decorating one. The [Playable Game Hypothesis](PLAYABLE_GAME_HYPOTHESIS.md) turns that into a minimal, testable game loop.

**Additional candidate experiments:** A room with two critters and three furnishing affordances; meaningful construction capability versus cosmetic-only choices; an expedition with recoverable risk; direct battle versus Threadwork; and returning home to a visible consequence.

**Dependency warning:** Before expanding residents, implementable identity must change from one customizable mascot to a persistent collection of individuals using explicit IDs and versioned save migration. This is an architectural recommendation, not approval to change the implementation repo.

These are **hypotheses under client review**, not accepted milestones.
