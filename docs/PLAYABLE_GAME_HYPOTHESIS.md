# Hollowlumen — Playable Game Hypothesis: A Living Handmade Home

**Version:** 0.1.0-draft  
**Date:** 2026-11-05  
**Status:** PROPOSED GAME IDENTITY — design synthesis, not client-approved canon or implementation authorization  
**Related:** [Integrated Homestead Vision](INTEGRATED_GAME_VISION.md), [Five-Game Mechanics Sieve](FIVE_GAME_MECHANICS_SIEVE.md), [Client Review](CLIENT_REVIEW.md), [Opportunity Map](GAMEPLAY_OPPORTUNITY_MAP.md)

> Create living companions. Give them a place to belong. Venture into a world that challenges what you have made. Return to a home that remembers what you did.

## 1. What game are we trying to make?

**Working genre:** A creature-crafting homestead adventure with systemic interactions and optional tactical risk.

The proposed player fantasy has five linked promises:

1. **Make:** Learn crochet-inspired patterns and construct individual critters with deliberate visual and functional decisions.
2. **Belong:** Give those creations a warm, editable cottage where they visibly inhabit spaces, express preferences and interact with the player.
3. **Venture:** Select companions and tools to explore a world with real objectives, obstacles, uncertainty and, where appropriate, recoverable risk.
4. **Change:** Use a consistent, small vocabulary of material-inspired operations to resolve problems and alter persistent world state.
5. **Return:** Enjoy the resulting changes in the cottage, relationships, craft knowledge and subsequent possibilities. A favorite critter can eventually appear in a native phone widget.

**The design thesis is not “combine five games”.** It is: give creative construction practical meaning, give adventuring emotional stakes, and give the home world persistent consequences. The cottage is neither a decorative menu nor a competing game mode; it is the living core around which adventures become meaningful.

This direction is a stronger synthesis of the existing cottage prototype and the creature-creation research, **not** an authorization to change their shipped/merged behavior.

## 2. The emotional engine: inhabitants, not inventory

The new hypothesis inspired by the reported repeated play of Animal Crossing is **inhabitation**: a place feels like home because its inhabitants respond to the player, each other, and what the player has built.

A critter is an individual with:
- Stable identity, player-chosen name, pattern version and chosen construction.
- Readable personal expression and a small number of bounded preferences or habits.
- A home presence: it can occupy appropriate spots and react to certain furnishings.
- Optional roles: companion, adventure participant, workshop helper, or favorite-widget subject.
- Persistent personal history separate from progression, currency or combat state.

**Example:** Pip curls up near a cushion by the window. Another critter prefers a yarn basket. Replacing the cushion changes available actions and visible behavior. The player can choose which individual goes on an outing without removing anyone from the household.

**Prototype budget:** One room, two individuals, three interactive furnishings, and a tiny behavior grammar. Start with authored reactions keyed by traits and furniture affordances, not procedural conversational AI, open-ended schedules or a fully autonomous simulation.

**Boundary:** Resident care should not impose compulsory login pressure or permanent neglect penalties. The home remains welcoming after absence; expedition risks may separately be meaningful and recoverable. Ask the client whether a more demanding mode appeals before implementing it.

## 3. The decisions that make it a game

A visually attractive world and pleasant repeated activities are insufficient if player choices have no effect.

The game must repeatedly offer these classes of decisions:

| Decision | Player question | Observable consequence |
| --- | --- | --- |
| **Design** | What should I construct, and why? | The resulting critter looks different and has traceable capabilities |
| **Habitat** | How should I organize this living space? | Residents use it differently; player expression persists |
| **Prepare** | Which companions, tools and supplies do I take? | Encounter strategies and available options differ |
| **Act** | How do I approach an obstacle? | Distinct actions consume resources, change structures, alter risk |
| **Invest** | What should I learn, repair or improve after returning? | New patterns, workshop possibilities or world routes become available |

Not every moment needs strategic play. Petting a critter or admiring a garden can be satisfying without utility. But the *crafting–expedition–return* progression loop must involve observable decisions and not only predetermined tapping or idle currency claims.

## 4. Three nested loops

### A. Hearth loop (a few minutes; no forced calendar duty)

Visit residents → pet, decorate or craft → see reactions → save a meaningful change.

Possible activities: position a cushion, work on a pattern, tend a fiber plant, photograph a companion, or accept an optional visitor request.

### B. Maker loop (short to medium)

Discover a technique → choose materials and construction → create a named individual or object → test its effects in the cottage or yard → refine or keep it.

Construction properties can affect both everyday interactions and adventure options. Cosmetic yarn color alone should not determine strength.

### C. Frontier loop (longer, or chunked into short encounters)

Choose goal → prepare → venture → confront obstacles → make tradeoffs → change a place → return to the cottage → see consequences and learn something useful.

The cottage provides recovery and meaning; the frontier provides challenge. These loops share entities, progress and visual identity, not necessarily the same activity intensity.

## 5. A common rule vocabulary

Prototype a **bounded Threadwork interaction grammar**, not a universal textile physics simulator.

Candidate properties: **durability, flexibility, reach, attachment capability**. Candidate actions: **join, anchor, reinforce, release, mend**. Each action has explicit prerequisites, resource costs (when relevant), affected components and resulting state.

The same rules might explain why:
- A reinforced critter can hold a bridge anchor.
- A flexible critter can reach a distant connection.
- Two companions can combine to stabilize a structure.
- A home test fixture demonstrates these capabilities safely.
- A competitive encounter may require opposing use of the same material logic.

**Non-goal:** Every knitted/crocheted physical behavior, unrestricted anatomy, sophisticated rope dynamics, or a giant renderer-neutral engine before finding fun. Actual crochet terminology and structural authenticity should be reviewed by a crocheter; fictional Threadwork must be labelled as such.

## 6. “The First Thread”: proposed demonstrable game slice

**Setting:** One small cottage and garden beside a meadow, one damaged bridge, one visitor, one short expedition.

**Beginning**
- Player chooses one introductory **pattern or crafting discipline** (the framing is an open design comparison), selects yarn/appearance, constructs and names an individual critter.
- A second distinguishable individual or variant is available for testing stable identity and complementary capability.
- The player can pet a resident and place a cushion or basket; different individuals respond differently.

**Inciting reason**
- A visitor cannot cross a bridge. Repairing it could reconnect the village to a workshop or unlock an additional crafting lesson. The request should be optional and intelligible, not an unskippable text chain.

**Preparing**
- The player chooses a companion and one possible tool or material. Their construction determines some valid actions, not a single required answer.

**Encounter**
- The bridge has at least two genuinely different solutions. Examples: spend thread reinforcing an existing anchor; use a flexible attachment to establish a new connection; investigate a secondary route and trade time for materials.
- The encounter presents an actual constraint (available action, supplied material, structural instability or temporary risk). It does **not** simply present differently worded buttons that all advance the same counter.

**Return**
- A repaired bridge remains repaired after a save/reload.
- The visitor can now arrive, a technique becomes available, or a home interaction changes. At least one visible, persistent consequence is mandatory for this experiment.
- Individual critter names, construction and affection history remain intact; the player can revisit the workshop to apply new knowledge.

**Favorite continuation**
- A widget-like **mock** portrays the selected critter at phone sizes; actual native integration requires separate evidence on the selected device. No assumption of continuously animated widgets.

### Acceptance probes (NOT RUN)

| ID | Probe | What failure tells us |
| --- | --- | --- |
| GAME-01 | A new player can state an objective without the reviewer narrating it | The game has no clear motivation |
| GAME-02 | Changing a construction choice changes a recognizable action or constraint | Crafting is cosmetic only |
| GAME-03 | Two encounter approaches differ in prerequisites, cost, risk or world consequences | Encounter is scripted busywork |
| GAME-04 | Reentering after reload preserves critters and completed world changes | The persistence model is inadequate |
| GAME-05 | A resident visibly reacts to the player's selected home arrangement | Cottage is a static inventory screen |
| GAME-06 | The player can choose not to adventure and still enjoy companion or decorating activity | The cozy half is merely a gate |
| GAME-07 | A failed frontier attempt is understandable and recoverable | Risk feels arbitrary or destroys attachment |
| GAME-08 | The client wants to craft, venture or tend the home again voluntarily | The combined loops may not be compelling |

A mock, pitch or illustrated sequence cannot pass these *gameplay* checks. Only an executable slice and observed interaction can.

## 7. Protect tension without creating obligation

Favorite games include both cozy systems and survival challenges. Do **not** conclude that the client dislikes failure, danger or resource pressure merely because the world is lavender.

Separate two contexts:
- **Home:** Stable, reassuring, expressive; minimal compulsory chores; resident identities safe.
- **Optional frontier:** Stakes, resource tradeoffs, imperfect decisions, recoverable damage and meaningful retreat. Harder modes or permanent loss are possible *questions*, not accepted requirements.

Do not tie world-lighting, timed resource claims, premium purchases or player absence to mandatory disadvantage. The game's difficulty should come from chosen challenges and learnable rules, not hidden clocks.

## 8. Opportunities that this hypothesis makes coherent

| Long-term opportunity | Fits because… | Decision gate |
| --- | --- | --- |
| Gardening and dye craft | Materials, beauty and creature habitats reinforce home-making | Does tending plants create enjoyable choices? |
| NPC commissions and friendships | World activity leads to specific creative goals | Can requests avoid generic material grind? |
| Friendly Stitch-offs | Competitions reuse construction knowledge | Are encounters interesting when no hostile foe exists? |
| Conventional tactical battles | Teams and risk may satisfy strategic players | Compare fairly against Threadwork first |
| Pattern lineage | Player-authored construction variants support creative progression | Does versioning feel expressive rather than technical? |
| Festivals and displays | Resident/community life makes personal creations visible | Do players value showing creations? |
| Sharing/visits | The workshop becomes a meaningful place to show | Requires privacy, security and moderation plan |
| Procedural anatomy/genetics | Possible deep creative space | Independent R&D only |
| Real crochet kits/patterns | Connect in-game companions to physical crafting | Must be tested and constructible by actual makers |
| Paid expansions/cosmetics | Could support complete delightful base product | Commercial research only after experience validation |

Do not build these as prerequisites to the first vertical slice.

## 9. Architecture and cross-team boundary

**Implementation repo:** [Kisuul/hollowlumen](https://github.com/Kisuul/hollowlumen) has the actual React/Vite cottage prototype, persistence, theme and solar work. **Design repo:** [cosmicdance-4-2-0/hollowlumen](https://github.com/cosmicdance-4-2-0/hollowlumen) holds evolving proposed product concepts. They are not the same code branch or automatically synchronized.

Reusable foundation worth protecting: pure game rules, persistence/sanitization, SVG component work, accessible semantic day/night tokens, and independent fictional solar lighting. These must not be casually ripped out because the design expands.

**Highest-impact future data change:** The existing single customizable companion model must not be assumed sufficient for a household of persistent individuals. Propose a versioned save migration, stable IDs, an explicit favorite reference, and separate pattern versus individual records before implementation.

**Source-of-truth constraints:** Contract hierarchy and approved product scope must be reconciled before a coding team converts any of these hypotheses into tasks. Do not merge the forks blindly or overwrite established game saves.

## 10. IP, provenance and approval

**Sources of inspiration:** The user reported the client's favorite games as Stardew Valley, Minecraft, Don't Starve and Pokémon, and separately observed her repeatedly playing Animal Crossing on Switch. This is *evidence of engagement with these games*, not proof of which mechanics she enjoys.

**Core differentiator under test:** The player **makes living companions**; their construction matters in one shared handmade world. No capturing wild creatures in balls. Avoid close imitation of another franchise's overall characters, visuals, iconic systems, progression, UI and lore. Mechanical inspiration is not a legal clearance; commercial IP/trademark/patent review is separate.

**User-established direction:** The cottage and creature adventure belong in the same design exploration; the client is the ultimate product-experience arbiter.

**Proposed by design team:** Inhabited workshop, residents with bounded habits, material-grammar encounters, first bridge story, risk separation and exact implementation sequence.

**Approval status:** No client signoff or new tests implied. This document is a candidate design and contains no application code. Its purpose is to make the game playable enough to *disprove or confirm* the premise.
