# Hollowlumen — Crochet Creature Game Specification

**Version:** 0.2.0-draft  
**Status:** Working concept, not product-owner approved  
**Updated:** 2026-11-05  
**Basis:** [Original repository pitch](https://github.com/cosmicdance-4-2-0/hollowlumen/blob/ac0317e250bef11c1f12abebe7be023aa41ecb47/README.md), followed by a direct user clarification on 2026-11-05.  
**Provenance:** The clarification supersedes the earlier interpretation that this was principally a cottage-decoration/life-simulation game. See [source audit](SOURCE_AUDIT.md).

> **A Tamagotchi-like collection of living crochet critters. Discover increasingly complex crochet patterns, bring new critters to life, care for them, and keep a favorite with you on your phone.** Inherited traits and selective breeding are potential later features; Spore-scale creature evolution is future exploration, not today's scope.

## 1. What the game is

A cozy *crochet-creature collection and companionship* game, working title **Hollowlumen** (the original README calls it *Lumenette Hollow*). Players inhabit a whimsical **Crochet World**, fill a collection with handmade living yarn critters, and select one favorite to accompany them through a phone home-screen widget.

**User-directed core concept (confirmed as direction, not finished feature design):**

1. **Collect critters** that inhabit a crochet-themed world.
2. **Discover patterns** of increasing complexity, which enable creating new critter types.
3. **Raise and enjoy critters** with a Tamagotchi-like relationship.
4. **Choose one favorite** from the collection to inhabit the phone widget.
5. **Possibly explore genetics**: random traits, inherited traits, selective breeding, and pure strains.
6. **Perhaps eventually explore Spore-like complexity**, but explicitly not now.

**Removed from core scope:** cottage decoration, farm work, resource-idle generators, minigame adventures, shop/VIP packs, live social visits, battery-based reward boosts, and an elaborate campaign. These were in the original pitch but are **not accepted as required features**. Keep them as unprioritized ideas, not deliverables.

The player's main object of attachment is the **individual critter**, not a house, inventory economy, or progression clock.

## 2. Core play loop [candidate]

**Find or unlock a pattern → create a critter → discover its appearance/personality → interact and bond → grow the collection → pursue another pattern or variation.**

The player can designate any owned critter as favorite. The favorite appears in the game and, when platform integration is available, in a phone home-screen widget. Switching favorites changes the widget's companion.

The loop should work even when the player is only interested in pet care, only interested in collecting variants, or only interested in making visually interesting creations.

### Design pillars

- **Living crochet, not crochet instruction.** Crochet patterns are the imaginative in-world recipes/blueprints of living critters; the game does not need to teach real stitches unless expressly designed later.
- **Individuals matter.** The same pattern can yield recognizably different critters.
- **Progress unlocks possibility.** More advanced patterns allow more interesting anatomy, silhouettes, traits, or combinations—not simply bigger numerical stats.
- **A favorite goes with you.** The widget is a product-defining feature, not a decorative afterthought.
- **Delight without obligation.** Care should be engaging and expressive without punishing normal absences. Whether explicit hunger, mood, aging, or mortality exists is an *open design decision*, not an assumed Tamagotchi copy.
- **Expandable, not overbuilt.** Make content and traits extensible, but do not build hypothetical evolution engines today.

## 3. The smallest playable toy

The first prototype should answer **one question**: *Is it enjoyable to make, collect, personalize, and care about these little crochet critters?*

Suggested toy content (illustrative, not a fixed art/content budget):

- One starter critter, with a name and a small set of expressive reactions.
- Two or three visually distinct crochet patterns, each creating a recognizable critter body.
- A few visible variations such as yarn colors, ear shapes, or stitched facial expressions.
- A **collection screen** to revisit individual critters rather than treating them as disposable items.
- **Favorite selection** as a first-class operation.
- One or two companion interactions (e.g. pet and play), giving a visible response.
- Local persistence of critters, patterns, favorite selection, and interaction state.
- A **widget-like mock display** that mirrors the selected favorite in the prototype; a separate early **native-widget feasibility spike** should validate actual Android/iOS delivery before claiming a shipping phone widget.

No breeding, social networking, paid shop, gardening, idle production, outing minigames, or generative anatomy is needed to answer the first question.

### Candidate acceptance checks

| ID | Requirement | Verifiable result |
| --- | --- | --- |
| COL-01 | Unique critter identity | Two critters created from the same pattern remain separate named individuals with separate saved IDs. |
| PAT-01 | Pattern unlocks | Locked patterns cannot create critters; unlocking one enables its defined critter structure. |
| PAT-02 | Pattern distinction | At least two toy patterns yield recognizably different critter silhouettes or components. |
| VAR-01 | Per-critter variation | Configured appearance differences persist and do not modify other critters. |
| CARE-01 | Companion response | A simple player interaction produces understandable feedback from the selected critter. |
| FAV-01 | One favorite | Any owned critter can be selected as favorite; switching favorite is reflected in every in-app view of that selection. |
| SAVE-01 | Persistence | Reload preserves collection, pattern unlocks, each individual's traits and name, and favorite selection. |
| WID-01 | Widget simulation | A testable widget-facing view model displays the same favorite and a safe fallback when none exists; do not represent a mockup as a native widget. |
| UX-01 | Gentle interaction | Prototype remains usable after a long absence without irreversible pet loss or resource penalties. |
| TEST-01 | Repeatability | Fixed random seed and content inputs reproduce the same created critter, and invalid creation/unlock/save operations fail safely. |

A native widget is an eventual **product acceptance criterion**, not evidence supplied by the toy.

## 4. Pattern system

A **Pattern** is a definition of what can be crocheted, not an individual critter.

A pattern may specify a base body, allowed body features, topology/silhouette, base materials, optional accessories, and which trait slots can visibly express. An individual **Critter** is one persistent creation produced from a pattern with its own ID, name, visual traits, and relationship state.

Illustrative progression, **not an approved content list**:

| Complexity | Pattern possibility | Illustration |
| --- | --- | --- |
| 1 | Single compact body | Round pom-pom friend with face stitches |
| 2 | Added features | Creature with ears, tail, or limbs |
| 3 | Composite construction | Multi-piece critter with distinct body and head |
| Future | Modular construction | Composable silhouettes, unusual appendages, procedural shapes |

Progression should unlock **new types of possibilities**, not merely increase output rates. The initial prototype can use hand-authored patterns and asset combinations. Nothing requires generating real crochet instructions or physical crochet patterns.

**Open:** How are patterns discovered: exploration, finding pattern pages, exchanging duplicates, completing collections, or automatic progression? Choose a single simple mechanism for the toy.

## 5. Genetics: promising experiment, not initial implementation

**User-proposed possibility:** each critter carries random traits; pairings may pass traits to offspring; selective breeding may yield pure strains.

Keep three things conceptually separate:

- **Pattern / construction:** determines which structural features are possible.
- **Heritable trait state:** determines variations that can be expressed within those allowed features, such as yarn coloration, ear style, glow, markings, temperament, etc.
- **Individual state:** chosen name, relationships, earned cosmetics, and care history; these should not be inherited by default.

A basic future trial can start with **one or two independent inheritable loci**, discrete alleles, predictable inheritance, and a visible distinction between expressed appearance (*phenotype*) and underlying trait combination (*genotype*). For example, a simple two-allele color locus can demonstrate a predictable pure-breeding line without pretending that all genetic traits work the same way.

A “pure strain” might mean an individual is **homozygous at a particular locus**, so descendants from a compatible matching line reliably express that trait. Do not equate “pure” with inherently better, more powerful, or more valuable. Real-world genetics is more complex; this would be a deliberately simplified fictional inheritance system.

**Design fork left open:** Does breeding create a newborn critter directly, or result in a new crochet blueprint/thread to craft? The fiction and interface must reconcile breeding with the idea that all critters are made from crochet patterns.

**A small genetics experiment would test:**
1. Can players predict outcomes after a few pairings?
2. Does selective breeding offer meaningful collection goals without imposing chores?
3. Can pattern complexity and inherited variation coexist without combinatorial art explosions?

Do not implement mutations, procedural anatomy, population simulation, dominant/recessive traits across dozens of loci, or a whole family-tree database before this succeeds.

## 6. Favorite critter and phone widget

This is a **core aspiration**, not a peripheral feature.

**Desired experience:** Choose a favorite from the collection; that same individual appears on the phone home screen as a small living crochet companion. The widget may reflect simple mood/expression and provide a route back into the game. Specific tap behavior and animation depend on platform capabilities and design choices.

**Platform boundary:** a responsive website does not automatically supply a native Android/iOS home-screen widget. The product requires a native bridge/app, supported platform-specific extension, or another verified delivery mechanism. The stack is therefore **not selected**. Validate platform support and data-sharing/update behavior early rather than designing the whole game around an unproven assumption.

**Candidate widget requirements after platform decision:**
- WID-02: Favorite changes in-app are reflected in the widget within a specified, platform-realistic update bound.
- WID-03: The widget remains meaningful if the app is closed, offline, or the device restarts.
- WID-04: Removed or missing favorites fall back safely; widget actions never corrupt collection state.
- WID-05: Widget presentation is readable in common sizes and respects platform updates, battery use, privacy and accessibility constraints.

**Not assumed:** direct battery monitoring, earning resources when charged, animation at arbitrary frame rates, or running full game logic continuously in a widget.

## 7. Architecture principles (keep simple)

Do not choose a programming language or framework based on the README, which only described an unverified prototype stack.

Separate only the boundaries needed to preserve the product's future:

| Model | Responsibility |
| --- | --- |
| **Pattern catalog** | Definitions, complexity/unlock states, available morphology and trait slots |
| **Critter collection** | Stable individual IDs, ownership, names, appearance, favorite ID |
| **Companion interactions** | Care events and player-facing response/state |
| **Persistence** | Versioned save/load, migrations, corruption handling |
| **Renderer and widget adapter** | Consistent representation of one critter in the game or on phone home screen |
| **Optional genetics module — future** | Trait generation, genotype/phenotype and inheritance without replacing core critter identity |

Keep content data and simulation rules apart. Expose random source and clock via explicit interfaces for repeatable tests. A missing native widget must not cause collection gameplay to fail. No multiplayer server, shop, gameplay currency, idle economy, or giant ECS is required merely to create the toy.

**Key invariant:** a critter is an **individual** with identity independent from the pattern used to make it. Future genetics cannot quietly change or overwrite that identity model.

## 8. Delivery sequence

**Checkpoint A — The creature is lovable.** Create, name, vary, view, and pet a critter in a local minimal prototype. Confirm the character and visual style work.

**Checkpoint B — The collection is satisfying.** Implement small pattern progression, multiple persistent critters, favorites, and a consistent widget-facing presentation model.

**Checkpoint C — Phone widget is real.** Choose the phone target and validate native widget integration, lifecycle, favorite synchronization, and test-device behavior. This is necessary before claiming the central product premise works.

**Checkpoint D — Inheritance experiment.** Independently prototype tiny trait inheritance and selective breeding. Promote into the game only if players find it understandable and rewarding.

**Someday — Procedural complexity.** Spore-like anatomy combinations, advanced breeding systems, and broader world interactions only if the proven core needs them.

Each checkpoint needs a working artifact and evidence relevant to its claim. A written spec does not mark code complete.

## 9. Design-language candidate

The proposed [Lavender & Loop design language](DESIGN_LANGUAGE.md) establishes purple/pastel surfaces, darker readable controls, tactile amigurumi construction, collectible critter presentation, and widget-first scaling. It is **proposed**, not product-owner approved. It answers an aesthetic direction without locking 2D versus 3D rendering or an art technology stack.

## 10. Decisions we actually need next

1. **Critter visual form:** confirm whether Lavender & Loop's tactile amigurumi creatures should be illustrated 2D, sprite/rigged 2D, or small 3D plush. This determines how cheaply patterns and traits can combine.
2. **Initial target phone:** Android, iOS, or both? This affects the widget experiment.
3. **Care intensity:** merely expressive petting/play, or actual Tamagotchi needs and consequences?
4. **Pattern discovery:** what enjoyable action unlocks a new body plan?
5. **Genetic trial timing:** after widget validation, or as a small independent experiment sooner?
6. **Working name:** Hollowlumen versus Lumenette Hollow, and whether “Lumenette” remains the creature name.

These are questions, not blockers for concept exploration. Do not substitute implementation guesses for the product owner's choices.

## 11. Definition of done for this document

**This draft is useful** when it distinguishes the essential creature experience from possible future extensions and can guide a cheap prototype.

**It is approved** only when the product owner accepts the scope, decisions, and acceptance criteria.

**Software features are implemented** only when source exists and corresponding checks have actually run. On the inspected source baseline, the project remains at concept stage.
