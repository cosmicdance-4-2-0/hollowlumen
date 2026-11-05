# Hollowlumen — Client Review and Acceptance Plan

**Version:** 0.1.0-draft  
**Status:** Proposed review procedure; no client approvals established  
**Date:** 2026-11-05

The client is the product owner of the experience. The development team can propose directions; only observed play and attributable client feedback can justify promoting one to an accepted requirement. Merging a documentation branch does **not** mean the client approved it.

Related drafts: [Product specification](PRODUCT_SPEC.md), [Gameplay expansion](GAMEPLAY_EXPANSION.md), [Lavender & Loop](DESIGN_LANGUAGE.md).

## Open decisions

| ID | Question | Options to present, without assuming acceptance | Status |
| --- | --- | --- | --- |
| CL-01 | What is the main game? | Cozy companion / crafting RPG / primarily competitive | OPEN |
| CL-02 | Which first patterns feel appealing? | Pufflet, Loopling, Bobbinbug as provisional starting examples | OPEN |
| CL-03 | What art form feels like real crochet? | Storybook illustration / rigged 2D / tactile 3D | OPEN |
| CL-04 | What is fun about making a creature? | Select components / surprise details / short tactile assembly | OPEN |
| CL-05 | Should critters battle? | Never / optional playful contests / integral RPG encounters | OPEN |
| CL-06 | What world activities appeal? | Repair quests / exploration / puzzles / competition | OPEN |
| CL-07 | What should pet care demand? | Expression-only / light needs / consequences | OPEN |
| CL-08 | Which phone is the widget for? | Android / iOS / both eventually | OPEN |
| CL-09 | Are the current names and palette right? | Hollowlumen, Lavender & Loop and candidate critter names | OPEN |
| CL-10 | Is monetization welcome, and how? | Full unlock / cosmetics / later expansions / none | OPEN |
| CL-11 | Would real crochet patterns or kits appeal? | Human-tested craft instructions or no physical tie-in | OPEN |

## Small client-facing trial

Use demonstrable materials, even if initially only paper sketches or explicitly labeled mockups.

1. **Show three starter constructions** at character-portrait and widget scale. Ask which feels appealing and which looks convincingly crocheted.
2. **Compare crafting styles.** Show deliberate choices, a limited surprise reveal, and a brief skippable assembly interaction. Observe which one they want to repeat.
3. **Show companionship.** Name a creature, pet it, select favorite, see another individual from the same pattern.
4. **Show one quest and battle concept.** Ask whether battling strengthens the world or distracts from it. Offer a non-combat resolution to compare.
5. **Present an honestly labeled widget preview** on the intended phone; never call the preview a working native widget.
6. **Conclude without steering:** “Which part would you willingly do again?” and “What should we leave out?”

Don't ask leading questions like “Don't you love this?” Avoid treating praise for one illustration as validation of the entire gameplay loop.

## Recording evidence

For every client review, record only information authorized for this public repository:
- Date, demonstrated artifact and actual device/medium.
- Direct statements attributed accurately, separately from team interpretations.
- Observed actions, points of hesitation, accessibility or input barriers.
- Choice made, alternatives shown, explicit approval/rejection and unresolved issues.
- Next minimal validation artifact.

**Approval rule:** A choice is APPROVED only after the product owner meaningfully reviews it and agrees. Record the evidence and date. Otherwise retain OPEN or PROPOSED. Never fabricate signoff.

## Acceptance ladder

- **Concept:** Client can distinguish the three starter bodies, describes the visual style in their own terms, and has an informed genre preference.
- **Creation:** Two individuals built from the same pattern can remain visibly distinct and independently saved.
- **Companionship:** A first-time player can name, pet and favorite without coaching; control and focus behavior remain accessible.
- **Adventure:** One quest or battle is actually enjoyable; players understand what its outcome changes. Core companionship does not require combat.
- **Persistence:** Names, traits, favorites, quest rewards and recovery survive a reload or interruption.
- **Native widget:** Only a real-device experiment proves it. Test offline, restart, missing-favorite and common widget sizes.
- **Commercial:** Discuss value and willingness to pay only after there is an enjoyable demonstrable core. No store is assumed.

## Current decision

**Not decided:** Whether the broader RPG supersedes the present cozy prototype. Until client review, treat the expansion as a parallel product hypothesis, not a signed-off scope increase.

**Current evidence:** Repository documents and prototype brand assets; no running gameplay, playtests or native widget. This plan has not itself been tested with the client.

## New challenger study: conventional combat versus Threadwork (OPEN)

The [zero-sacred-cows concept review](CONCEPT_DEMOLITION_REVIEW.md) questions whether the RPG's recognizable creature-battler structure is the right product shape. It is **not a replacement spec**.

Additional review questions:
- **CL-12 — Interaction identity:** Conventional turn-based critter battle, textile/environmental Threadwork, a hybrid, or neither?
- **CL-13 — Opening authorship:** Three starter creature patterns versus three starter crafting disciplines (Shape / Flow / Join)?
- **CL-14 — Variation:** Individual random traits, versioned pattern lineage, or both in different roles?
- **CL-15 — Collection scale:** Large inventory versus a smaller, more meaningful workshop cast?
- **CL-16 — Creative originality:** Which aspects feel recognizably Hollowlumen rather than familiar genre conventions?

**Proposed paired encounter trial:** Same critter, comparable visual polish and onboarding, one short conventional battle and one material-interaction challenge. Evaluate comprehension, decision quality, willingness to replay, emotional fit and whether the creature's construction actually matters. Do not presume Threadwork wins. Also allow rejection of both.

**Test integrity:** Record which prototype was shown first; rotate the order between testers if there is more than one. Don't claim statistical results from one client's preference. If no playable prototype exists, treat feedback on sketches only as conceptual preference, not proof of gameplay enjoyment.

**IP/design gate:** No creature capture in balls. Original creature art, world expression and UI are required; similarity review should consider combined presentation and not only isolated mechanics. Qualified legal review remains a separate commercial-release requirement.

All five new questions are OPEN. No client answer or test outcome has been recorded.

## Integrated homestead + adventure direction (OPEN; 2026-11-05)

The [Integrated Game Vision](INTEGRATED_GAME_VISION.md) proposes **combining**, not choosing between, cottage life and the creature-construction adventure. The [Gameplay Opportunity Map](GAMEPLAY_OPPORTUNITY_MAP.md) catalogs possibilities without turning them into implementation requirements. No client review of this synthesis has been recorded.

Additional client decisions to validate:
- **CL-17 — Preferred balance:** More home/decorating, more exploration/encounters, or a flexible mixture?
- **CL-18 — Cottage meaning:** Mainly cozy decoration, interactive workshop, residents' behaviors, commissions, gardening, or a subset?
- **CL-19 — Reward emphasis:** Materials, new patterns, world restoration, creature relationships, or another motivator?
- **CL-20 — Adventure consequence:** Is a repaired world/home response more satisfying than accumulating coins or points?
- **CL-21 — Session flexibility:** Does the client enjoy short companionship sessions as well as longer adventures without pressure to check in?
- **CL-22 — Creature identity:** Would they rather maintain a small meaningful resident cast or a much larger collection?
- **CL-23 — Visual integration:** Does the other team's day/night cottage style suit the construction workshop, adventure and widget together?

**Product observation:** Show one consistent creature moving between a home scene, a pattern-creation screen and a short authored outing; after the outing, show a persistent consequence back at home. Ask what the client wants to revisit. Do not treat a conceptual slideshow as proof of playability.

**Engineering gate:** Preserve the existing web prototype's save and economy behavior while testing the new mechanics on an isolated branch. The two project forks have different scopes and are not automatically integrated; no code migration is authorized by this document.

All CL-17 through CL-23 remain **OPEN**. No client signoff, game test or native-widget test is inferred.

## Five-game inspiration and inhabited-home hypothesis (OPEN; 2026-11-05)

The user reports the client's favorite games as Stardew Valley, Minecraft, Don't Starve and Pokémon; the user has also observed her returning to Animal Crossing on Switch. This signals engagement, **not** a known preference for any one mechanic. The [Five-Game Mechanics Sieve](FIVE_GAME_MECHANICS_SIEVE.md) and [Playable Game Hypothesis](PLAYABLE_GAME_HYPOTHESIS.md) propose neutral tests and an integrated home–frontier experience.

New decisions, all **OPEN**:
- **CL-24 — Animal Crossing appeal:** Is the main draw decorating, resident relationships, collecting, repeated visits, or something else?
- **CL-25 — Home inhabitation:** Do small personalized critter habits and furnishing interactions increase attachment?
- **CL-26 — Frontier stakes:** Does recoverable risk, careful preparation, and occasional retreat sound enjoyable, or should adventures stay gentle?
- **CL-27 — Favorite game activities:** Which parts of each of the five games does the client repeatedly choose, skip or dislike?
- **CL-28 — Return-home satisfaction:** Is a changed resident/visitor/world more compelling than a material-only quest reward?
- **CL-29 — Creature construction tradeoffs:** Do meaningful structural capabilities strengthen creativity or make aesthetic choices feel constrained?
- **CL-30 — Play rhythm:** Which activities suit a quick check-in, and which would justify an extended adventure?

**Practical trial:** Demonstrate a home scene with an individual critter responding to a furnishings choice, then a small constructed-capability expedition with an authored obstacle and a visible home consequence. Pair a low-risk and a recoverable-risk version of the outing. Observe what she chooses to repeat; do not presume a gentle aesthetic implies an aversion to challenge.

**Evidence and privacy:** Record only feedback approved for this public repository. Do not infer client preferences from observed playtime alone. No client answers or experiment outcomes are recorded in this addendum.
