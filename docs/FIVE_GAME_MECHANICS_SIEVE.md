# Hollowlumen — Five-Game Mechanics Sieve

**Version:** 0.1.0-draft  
**Recorded:** 2026-11-05  
**Status:** INSPIRATION ANALYSIS — no imported feature is approved merely by appearing here  
**Companion:** [Playable Game Hypothesis](PLAYABLE_GAME_HYPOTHESIS.md)

## 1. Evidence and its limitations

The user reports that the client particularly enjoys **Stardew Valley, Minecraft, Don't Starve and Pokémon**. The user has also *personally observed* her playing **Animal Crossing** frequently on Nintendo Switch. This is not a measured playtime sample or a breakdown of what activities she prefers; it is a useful direction for hypothesis formation.

**We must not project one single kind of “cozy player” onto her.** Someone who enjoys Animal Crossing may also like high-stakes preparation and risk from Don't Starve. The next step is to ask about individual activities and to observe actual choices.

## 2. Sort by motivations rather than copying presentation

| Game | Broad player appeals to investigate | Candidate Hollowlumen mechanics | What not to blindly copy |
| --- | --- | --- | --- |
| **Stardew Valley** | Homestead progress, friendships, routines, diverse goals, community change | Workshop/cottage development, NPC commissions, fiber garden, festivals, restoration | Strict daily chores, identical calendar/social structures, skill-stat treadmill |
| **Minecraft** | Player authorship, reusable construction rules, experimentation, exploration and persistence | Pattern construction, join/anchor/reinforce vocabulary, authored building interactions, discoverable affordances | Infinite voxel simulation, identical recipe grid, unlimited world generation |
| **Don't Starve** | Preparation, scarcity, hazard management, discovery, learning from failure | Optional expeditions with tradeoffs, recoverable fraying, resource constraints, retreat/retry, escalating danger | Opaque punishment, hunger/sanity meters by default, irreversible loss before client consent |
| **Pokémon** | Companions, personal attachment, team composition, strategic matchups, discovery | Named player-created individuals, complementary construction roles, paired tactical experiments | Ball capture, recognizable starter/types/gym/badge/encounter ensemble, cloned battle UI |
| **Animal Crossing** | Inhabiting a personal place, decor, residents, collections, seasonal atmosphere, return visits | Living workshop, resident preferences, furniture affordances, pattern archive, visitors, snapshots | Lookalike villagers, museum/debt economy duplication, exact calendar/gifting systems, compulsory real-time schedules |

These are **analysis hypotheses**, not descriptions of the client's actual reasons for playing.

## 3. Sieve by practical fit

**KEEP IN FOUNDATION** means a compelling candidate for the first integrated experiment, not a production-approved feature. **TRANSFORM** means preserve the player motivation while inventing original mechanics. **TEST** means potentially valuable but unproven. **PARK** means high-cost or distant.

| Mechanic | Disposition | Why |
| --- | --- | --- |
| Persistent personalized home | **KEEP IN FOUNDATION** | Gives the player somewhere worth returning to |
| Distinct named companions | **KEEP IN FOUNDATION** | Makes creation emotionally consequential |
| Meaningful player construction choice | **KEEP IN FOUNDATION** | Differentiates made companions from selected units |
| Small world exploration and quest change | **KEEP IN FOUNDATION** | Turns home and construction into a gameplay loop |
| Resident reactions to furnishings | **KEEP IN FOUNDATION** | Makes decoration inhabited, not static |
| Small reusable material-action vocabulary | **TEST EARLY** | Could unify craft, puzzles and competition |
| Select companions/tools for an outing | **TEST EARLY** | Connects making to strategy |
| Expedition risk, resource scarcity and retreat | **TEST EARLY** | May add needed tension; tune independently of household care |
| Three starter creature families | **COMPARE** | Accessible choice, but may inherit overly familiar genre silhouette |
| Three starter crafting disciplines | **COMPARE** | Encourages authorship, but could be abstract |
| Direct creature-versus-creature battle | **COMPARE** | Strategic familiarity versus product originality |
| Environmental Threadwork encounter | **COMPARE** | May be distinctive but risk becoming forced puzzles |
| Fiber garden and seasonal materials | **TRANSFORM** | Support creativity; avoid repetitive harvesting obligation |
| Skills and progression | **TRANSFORM** | Primarily new techniques/patterns, not raw percentage upgrades |
| Resident relationships | **TEST SMALL** | Affection may reward attention; avoid compulsory social simulation |
| Craft fairs and festivals | **PARK** | Strong flavor, but not required for a playable loop |
| Pattern lineage and modifiable patterns | **TEST LATER** | Interesting creative mastery; schema/art risks |
| Full procedural anatomy | **PARK** | Technical and validation cost enormous |
| Fixed-species mass collecting | **QUESTION** | Can displace attachment to individuals |
| Competitive multiplayer | **PARK** | Secure netcode and balance premature |
| High-pressure daily upkeep | **QUESTION** | Time pressure can be desirable; test context and consent |
| Real-money shop | **DEFER** | Core experience first; avoid paid battle advantages |

## 4. One game rather than five silos

**Combined player fantasy:**

> I built a place I care about. I made the creatures who live there. I understand how they're constructed. I chose whom to bring, used what I made to overcome something beyond home, and returned to see lasting change.

The five source games each illuminate a different part of that sequence:
- **Stardew:** place and relationships develop over time.
- **Minecraft:** the player's constructions remain useful and persistent.
- **Don't Starve:** preparation and encounters can carry meaningful risk.
- **Pokémon:** companions and team choices matter to the player.
- **Animal Crossing:** the world feels lived in, personalized and inviting to revisit.

These are general design inspirations. Build **original characters, interfaces, world rules, aesthetics, encounter objectives, and progression**.

## 5. The strongest new hypothesis: inhabitation

An Animal Crossing-style motivation is not just “more furniture”. It's the chance to make a space feel like *a living place*.

**Proposed minimal resident grammar:**
- Stable critter ID and an authored expressive pose set.
- One or two categorical preferences (e.g., quiet/window, warm/cushion) defined independently from combat abilities.
- Furniture with documented **affordances** (can sit, rest, inspect, play).
- Deterministic or explicitly seeded selection of eligible small interactions.
- State that survives changing rooms, saving and reloading without storing a complex autonomous schedule.

**Toy example:** Pip tends toward the sunny cushion while another critter gravitates toward a yarn basket. The player swaps furnishings; each reacts in character. Decorations without interactions still remain valid for pure aesthetic expression.

**Non-goals:** Self-optimizing behavior agents, simulated emotional neglect, real-time schedules, spontaneous item destruction or a requirement to keep a dozen residents happy.

## 6. The other new hypothesis: a worthwhile frontier

Don't Starve should prevent us from assuming the game must never challenge or frustrate a player.

A safe cottage and potentially dangerous frontier can reinforce each other. The outing should have a **clear stake and a reasonable failure path**:
- Bring limited material/tools or a small team.
- Choose between different tactics and resource costs.
- A mistake may cost supplies, fray a companion temporarily or require retreat.
- Recovery is transparent; chosen companions and authored patterns remain owned.
- Optional higher stakes can be considered after preferences are established.

Avoid making permanent loss, hostile time gates or resource starvation an unquestioned default. Equally, avoid declaring all risk incompatible with a pastel art style.

## 7. Client interview: ask what she actually does

Use neutral questions rather than asking the client to endorse the team's favorite interpretation:

| Game | Focused question |
| --- | --- |
| Stardew Valley | Which activities draw you back most: farming/decorating, relationships, mining, completing collections, or something else? |
| Minecraft | Are you mostly interested in building, exploring, survival, engineering/automation, or a mixture? |
| Don't Starve | Is it preparation, surviving danger, base building, discovering systems, combat, or another part you prefer? |
| Pokémon | Do you mainly enjoy finding creatures, raising favorites, collecting, strategic team battles, or exploring? |
| Animal Crossing | Is it arranging your home/island, villagers, collection goals, visiting, or simply returning to a familiar world? |

Ask also **which parts she skips or dislikes**, and which of these games she'd choose with only 10 minutes available versus an entire evening.

**Evidence rule:** A reported favorite or observed play session does not certify the proposed mechanic; client comments, observed interaction and representative prototypes are required to promote ideas into accepted requirements.

## 8. Small discriminating prototypes

| Experiment | Compare | What it tests |
| --- | --- | --- |
| **H1 — Inhabited room** | Static decorative scene vs. 2 residents with 3 furniture affordances | Does reactive inhabitation make returning home satisfying? |
| **H2 — Construction choice** | Purely visual customization vs. one construction-derived ability | Does capability add enjoyment or conflict with aesthetics? |
| **H3 — Frontier risk** | No-cost retry vs. recoverable supply/fray consequence | Does meaningful tension improve the experience? |
| **H4 — Encounter form** | Conventional 1v1 battle vs. Threadwork obstacle | Which encourages replay, understanding and original identity? |
| **H5 — Opening choice** | Three starter patterns vs. three technique disciplines | Which inspires more authorship and less confusion? |
| **H6 — Home consequence** | Material-only quest reward vs. visitor/bridge/room change | Which makes the world feel more alive? |

Use **comparable visual polish**, the **same critter art** and **neutral observation prompts** where possible. Do not pretend one participant supplies statistical certainty.

## 9. Originality and scope safety

The goal is to borrow lessons about player motivations and widely used mechanics, not the recognizable ensemble of any game's IP. In particular:
- Player creates critters; no wild-critter ball capture system.
- No copied creature roster, iconic gadgets, trademark naming, lookalike villagers or UI architecture.
- Distinct narrative premise: material-constructed inhabitants with construction-driven world interactions.
- Similarity risk is assessed holistically, and qualified legal review precedes commercial release. This document is not legal advice.

All opportunities remain subordinate to product-owner validation, technical feasibility and a small reviewable prototype. **This is a sieve, not a mandate to implement five games' worth of mechanics.**
