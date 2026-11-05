# Hollowlumen — Integrated Homestead and Adventure Vision

**Version:** 0.1.0-draft  
**Recorded:** 2026-11-05  
**Status:** INTEGRATION PROPOSAL — design direction under exploration; client has not approved this as product canon  
**Audience:** Both Hollowlumen engineering/design efforts and product owner  
**Origins:** Follow-up to [Gameplay Expansion](GAMEPLAY_EXPANSION.md) and [Zero-Sacred-Cows Review](CONCEPT_DEMOLITION_REVIEW.md). The user explicitly challenged the false choice between the cottage simulator and creature-based adventure, then requested a broad, creative design pass.

> Build a home. Make living companions. Explore beyond the doorstep. Use what you learn to change the world. Come home to something that remembers.

## 1. The synthesis

The cottage simulation and the envisioned creature-creation RPG **can be parts of one game**. Their relationship is potentially the project's defining gameplay strength.

- **Cottage:** The player's home, workshop, expressive space and social center. Here the player creates, cares, decorates, experiments, recovers and sees consequences of the wider world.
- **Critters:** Individually named, persistently saved creations, residents, companions and possible participants in adventures. They are not disposable inventory or exclusively battle equipment.
- **Crafting and patterns:** The bridge between home and adventure. Learning techniques changes what players can make and what their creations can accomplish.
- **World:** A place for discovery, quests, narrative, exploration, obstacles, competition and persistent change.
- **Widget:** The selected favorite companion's separate real-device presence; emotionally important, technically its own adapter and acceptance gate.

**Working genre hypothesis:** *A cozy creature-crafting homestead RPG with systemic exploration and optional tactical encounters.*

That description is deliberately a hypothesis; the product owner's experience and tested mechanics choose the final balance. This vision does **not** supersede the smaller [PRODUCT_SPEC.md](PRODUCT_SPEC.md) baseline by itself.

## 2. The playable loop

### Primary loop: Home → Make → Venture → Change → Return

1. **Settle at home:** See favorite companions, decorate or tend a small living space, meet a visitor or choose a goal.
2. **Prepare or make:** Choose patterns, materials and construction options; craft or modify a uniquely identified companion or useful tool.
3. **Venture:** Explore an authored location, fulfill a commission, solve a construction-related problem or enter a tactical encounter.
4. **Act with consequence:** A meaningful decision changes a quest state, passage, resident situation or attainable technique.
5. **Discover:** Gain material, knowledge, a pattern technique, a world change or a relationship experience.
6. **Return:** Use what was learned at home; see visible consequences; decide what to make or explore next.

The player must not be required to perform all six steps every session. Some users will enjoy decoration or companions without combat. Others will want a substantial adventure.

### Supporting loops

| Loop | Player action | Why it can be fun | Boundaries |
| --- | --- | --- | --- |
| **Companionship** | Pet, name, observe, favorite, interact | Emotional attachment and recognizable individual behavior | No default guilt/streak punishment |
| **Construction** | Select pattern, customize, assemble, version a variant | Creativity with understandable consequences | Avoid forced random-roll optimization |
| **Homestead** | Arrange spaces, grow craft plants, welcome residents, tend workshop | Ownership, expression and light systems thinking | No compulsory house-management grind |
| **Exploration** | Find routes, people, materials and techniques | Curiosity and discovery | Not merely resource collection |
| **Threadwork** | Join, anchor, stretch, release, reinforce or mend structures | Small systemic puzzles with multiple approaches | Bounded authored rule model, not full yarn physics |
| **Tactical encounter** | Use companion construction and shared actions in opposition | Strategic choices, tension, mastery | Compare combat and environmental formats |
| **Commission** | Make something satisfying a resident's stated need | Creative application of known techniques | Require actual choices, not just a receipt |
| **Collection/community** | Keep distinct critters, arrange their living space, build relationships | Individual meaning rather than a number counter | Avoid mandatory mass-production |
| **Ambient/widget** | Glance at the favorite outside the game | Companion continuity | Native feasibility independent of mock |

### Session scales (design hypotheses, not measured behavior)

- **~1–2 minutes:** Visit favorite, pet, rearrange one item, see changes at home.
- **~5–15 minutes:** Craft, do a commission, complete a small quest, try a pattern variant or friendly contest.
- **~20+ minutes:** Explore a region, solve connected problems, finish a restoration arc or undertake an expedition.

Neither active play nor extended absence should be punished merely because of the player's schedule. Existing day/night rendering should not control the authoritative reward clock.

## 3. The cottage is a functional space, not just a collection of decorations

Potential home spaces (these may be represented by a few UI zones at first; **do not** implement every room):

| Space | Candidate play | Connection outside |
| --- | --- | --- |
| **Workshop** | Make critters, tools, accessories; try assembly techniques; mend | Construction unlocks interaction capabilities |
| **Pattern library** | Learn, organize, revise and branch construction patterns | Quests and experiments reveal knowledge |
| **Garden** | Tend fictional fiber plants, dye ingredients and flowers | Materials, visiting characters, changing scenery |
| **Crafting room** | Create functional or purely decorative furnishings | Home interaction opportunities and expressiveness |
| **Living room** | Watch critter residents, pet, socialize, photograph | Relationships and personal memories |
| **Yard** | Test reach, anchors, reinforcement on tiny obstacles | Low-pressure ability tutorial |
| **Attic/observatory** | Discover clues and admire changing light | World hints and atmospheric simulation |
| **Porch** | Hear requests, receive visitors, view deliveries and gifts | Quest and commission hub |

**Design distinction:** Some furnishings should create new interactions (workbench, play area); others should remain **purely expressive**. Do not make decorating aesthetically worse because of statistically optimal furniture.

## 4. Critters as residents, not only party members

Each created companion has stable identity, name, visual construction and saved preferences/history. A resident may favor a space or activity, interact with peers or react to the player's return. The proposal is a *small observable cast*, not a full autonomous social simulator or a mandate for advanced AI.

A companion may be selected for an expedition, used in a workshop activity or made the active phone-widget favorite. Those roles should not erase or split individual identity.

**Life principle:** Companions remain welcoming after absences. No automatic permanent loss, neglected-pet guilt, or mechanically mandatory daily attention. The client may prefer more simulation, but that requires informed review.

## 5. Crochet is part of the fictional world's material logic

Take crochet more seriously than a visual motif. **Material-inspired properties** such as durability, flexibility, reach and connections may make crafting decisions meaningful in quests, construction and tactical challenges.

- A densely constructed companion might secure an anchor.
- A flexible attachment might reach across a gap.
- Joined components might manipulate several connected objects.
- A crafted tool could offer a different solution without forcing a certain critter build.

These are deliberately simplified *game mechanics*, not real physical simulations. Material rules must be learnable, deterministic where promised and intelligible from the UI.

**Crochet authenticity gate:** Consult a person who actually crochets about visual stitch construction, terminology and real-world patterns. Existing prototype's “Knit / Purl” activity uses knitting rather than crochet terminology. If retained, it should be explicitly about knitting, not presented as crochet instruction. Distinguish fictional Threadwork from actual craft education.

## 6. A world that responds

Authored regions can contain repair, exploration, rescue, commissions, friendly competitions and encounters. **World changes should sometimes come back home.** For example:
- Repairing a bridge opens a route and allows a merchant to visit the cottage.
- Restoring a workshop reveals a construction technique.
- Helping a garden changes its plants and enables a resident's commission.
- A collaborative project changes the visible village rather than adding only currency.

Potential world regions in earlier drafts include Thimble Meadow, the Tangled Grove, Patchwork Marsh and the Great Loomworks. Names, geography and lore remain provisional.

### Conflict need not always equal combat

Possible activity styles:
- **Environmental Threadwork:** Manipulate connected structures under understandable constraints.
- **Direct tactical contest:** Companion versus opponent, subject to the same construction rules when feasible.
- **Stitch-offs and festivals:** Friendly timing, technique, creativity or team challenges.
- **Non-combat route:** Alternate solutions to an authored problem where advertised.

Do not declare conventional battles forbidden or Threadwork automatically superior. Compare two small examples using the same critter, equal visual treatment and comparable onboarding.

## 7. Distinct rewards, not one dominating number

| Reward class | Examples | Purpose |
| --- | --- | --- |
| **Materials** | Yarn, dyes, fiber, components | Support crafting and expression |
| **Knowledge** | Patterns, techniques, construction insights | Expand valid creative actions |
| **Relationships** | Critter history, familiarity and interactions | Make individuals significant |
| **World change** | Repaired bridges, reopened routes, resident visits | Give agency visible consequences |
| **Home expression** | Furniture, arrangements, photos, accessories | Let the player establish a place |
| **Mastery (optional)** | Completion records, efficient solutions, contests | Offer challenge without mandating grind |

**Idle activity may coexist** as a light source of materials or atmospheric resident behavior, but should not become the dominant path to progression. Avoid a loop where the best strategy is to wait, claim, and upgrade timers.

Avoid tying favorite yarn *color* to combat superiority; distinguish cosmetic preference from meaningful structural choices.

## 8. First integrated vertical slice — “The First Thread” (proposal)

**Purpose:** Prove that the cottage, crafting, critters and world actually depend on each other. It is not a feature-count milestone.

**Ingredients:**
- One little cottage/workshop with a small garden, a few movable decorations and one NPC visitor.
- One chosen starter from a set of three basic patterns **or** crafting disciplines (compare with the client).
- One player-created, named, persistent critter with at least one construction decision.
- One short authored outing to a damaged bridge.
- One meaningful Threadwork challenge with at least two distinct possible solutions (not merely different button labels).
- One saved world consequence, a newly accessible technique or pattern, and a visible home consequence.
- Petting, selecting a favorite, saved progress and a **clearly labeled widget-style preview**. A real native widget remains a separate device proof.

**Example:** “The Bridge That Forgot Its Knot.” A visitor needs to cross a damaged bridge. The player can reinforce an anchor, use a flexible connection to reach a far point or obtain material by taking another route. A successful solution updates world state; upon returning home, the visitor or a new commission becomes available. The player can use what was learned to change the next construction.

**Proposed acceptance probes, not executed:**
1. The player understands why their construction choice matters.
2. At least two encounter approaches have different preconditions/outcomes or costs.
3. The quest is not just a predetermined sequence of taps.
4. A meaningful persistent change is visible at home or in the world after reload.
5. The critter's name, identity and favorite status survive save/load.
6. A player without interest in battling still has worthwhile companionship/creation play.
7. The client voluntarily wishes to make another critter or go on another outing.
8. The widget preview is not misrepresented as a native device widget.

**Counterexample gate:** If the scenario is merely chores interleaved with tapping, it does not validate the integrated loop. Cut to the smallest single satisfying activity and retest.

## 9. Architectural integration rather than a giant rewrite

**Conceptual boundaries** to preserve or introduce incrementally:

| Domain | Owns | Important invariant |
| --- | --- | --- |
| Critter identity/collection | Stable IDs, names, history, favorites | An individual cannot be erased by renderer or pattern updates |
| Pattern/technique catalog | Construction definitions and learned knowledge | A learned pattern does not imply a pre-made companion |
| Construction/interaction rules | Parts, connections, legal material actions | Invalid actions don't corrupt canonical state |
| Cottage/residents | Furnishings, placements, activities, optional relationships | Decoration cannot silently modify unrelated game state |
| World/quests | Locations, progress, authored changes | Completed rewards are not duplicated after reload |
| Encounters | Rules, state transitions, deterministic resolution | No rendering/payment dependencies |
| Economy (optional) | Materials and bounded reward rules | Time preview cannot manipulate earning |
| Persistence | Versioned serialization, sanitation, migration, recovery | Old saves preserved or explicitly migrated |
| Presentation | Component visuals, scene lighting, accessibility | Visual settings never rewrite game progress |
| Native widget | Favorite-state projection, device integration | Mock is not proof of native capabilities |
| Commerce (future) | Explicit entitlements | Does not determine critter worth or competitive stats |

This is not a mandate for a new engine, ECS, live service or universal physics solver. The current React/Vite prototype's pure rule functions, local-save sanitation, SVG rendering experience, semantic day/night tokens and independent solar presentation are potentially useful. Reconcile actual interfaces and migration before adapting code.

**Existing implementation context (2026-11-05):** [Kisuul/hollowlumen](https://github.com/Kisuul/hollowlumen) has a playable web-prototype codebase and cottage, wandering, idle, yarn and shop routes. Its design system and solar/theme foundation are materially ahead of the documentation-focused [cosmicdance-4-2-0/hollowlumen](https://github.com/cosmicdance-4-2-0/hollowlumen) branch. These repositories are *not* automatically synchronized; this document is not a code integration.

## 10. Boundaries: depth, trust and originality

- **No IP cloning:** Original creature origins (making, not capturing in balls), names, silhouettes, animations, world, interface, progression and combined presentation. Familiar mechanics can be studied; avoid copying a recognizable ensemble of expression and conduct appropriate commercial legal review.
- **No monetization-first design:** A meaningful free opening and possible premium unlock, cosmetics, expansions and physically tested crochet kits are research options. Avoid paid combat power and random paid trait rolls. No payment code in this milestone.
- **No unproven scale promises:** Breeding, procedural anatomy, live co-op, tournaments, vast worlds and player marketplaces require their own experiments and approvals.
- **No hidden simulated player obligations:** Optional idle progress is not daily attendance, and world lighting isn't a progression gate.
- **No premature optimization of delight:** Test whether players enjoy making, petting, decorating and exploring before building large systems.

## 11. Decisions and authority

**Established user direction:** Expand design without treating cottage and adventure as rivals; preserve creature making, individual attachment, the phone-favorite ambition, an interest in quests/battles and possible later monetization; avoid direct IP cloning.

**Agent design proposals:** The exact material-action vocabulary, region names, first quest, workshop room taxonomy, alternative activity loops, economic breakdown and suggested first vertical slice.

**Client approval:** Not recorded for this integrated vision. The client has final product-experience authority. Earlier user-reported approval of the *other team's day/night palette direction* does not imply approval of this gameplay, integrated UI, characters or implementation.

**Implementation:** No code or native widget is created by this document. Existing shipped/merged code is not to be destroyed to make this proposal convenient.

**Next design checkpoint:** Review the [Gameplay Opportunity Map](GAMEPLAY_OPPORTUNITY_MAP.md) and [Client Review](CLIENT_REVIEW.md), choose the smallest comparative interaction sketches, and gather observed reactions before expanding engineering scope.

## Addendum — Five-game sieve and inhabited home hypothesis (2026-11-05)

The later reports that the client enjoys **Stardew Valley, Minecraft, Don't Starve and Pokémon**, plus observed repeat play of **Animal Crossing**, motivate an additional design hypothesis: the cottage should feel **inhabited by player-created residents**, not only decorated. This is an interpretation to test, not evidence that any particular subsystem is preferred.

- See [Playable Game Hypothesis](PLAYABLE_GAME_HYPOTHESIS.md) for the proposed game identity, player decisions, loops, single integrated scenario, and falsifiable acceptance criteria.
- See [Five-Game Mechanics Sieve](FIVE_GAME_MECHANICS_SIEVE.md) for a mechanics-level keep/transform/compare/park analysis, including the possibility that **a cozy home and dangerous expeditions can strengthen one another**.
- Earlier RPG and Threadwork proposals remain preserved. The new documents **do not** approve a resident simulator, survival mode, combat system, exact starter format or new implementation scope.

**New strongest candidate loop:** Construct a companion → give it a place in the home → prepare for a meaningful outing → use what was built → return to a home changed by the result. The player may also choose a short purely cozy visit.
