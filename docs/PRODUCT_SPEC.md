# Lumenette Hollow — Product and Systems Specification

**Version:** 0.1.0-draft  
**Status:** PROPOSED — not product-owner approved  
**Prepared:** 2026-11-05  
**Source baseline:** [README.md at ac0317e](https://github.com/cosmicdance-4-2-0/hollowlumen/blob/ac0317e250bef11c1f12abebe7be023aa41ecb47/README.md)  
**Companion document:** [Source audit and decisions](SOURCE_AUDIT.md)

> This document reconstructs a testable concept from a single unverified pitch. It is **not** an assertion that described features exist, that a technical stack has been chosen, or that unresolved product decisions have been made.

## 0. Reading this specification

- **SOURCE**: an idea or claim present in the baseline README; not automatically validated or approved.
- **PROPOSAL**: an engineering or design recommendation added in this reconstruction.
- **OPEN**: a decision requiring the product owner's direction.
- **REQUIREMENT (candidate)**: a testable condition proposed for an eventual approved build.
- **IMPLEMENTED**: reserved for a feature verified in actual source and with relevant checks; **no features currently qualify** in the inspected repository.

Identifiers are stable for review. A proposal becomes binding only when accepted in a subsequent versioned specification. Treat example tuning parameters as configuration candidates, not hidden constants.

## 1. Product identity

### 1.1 One-sentence concept [SOURCE]

**Lumenette Hollow** is a relaxed, craft-centered rural-fantasy life sim in which players care for expressive living-yarn companions (Lumenettes), personalize a cottage and garden, and optionally take short excursions to gather materials.

The GitHub repository is named **hollowlumen**; this does not itself establish the shipping game's title. The README uses *Lumenette Hollow*, the companion species *Lumenettes*, and *Pip* as an example/starter name.

### 1.2 Intended experience [SOURCE + PROPOSAL]

The player should feel that they can return for a minute, accomplish something pleasant, and leave without penalty or anxiety. Expression and companionship are central; optimization is optional. The rural fantasy should feel tactile, gentle, whimsical, and legible even on a small display.

**Candidate product pillars:**

1. **Respect time:** meaningful actions in short sessions; no mandatory appointment mechanics or streak punishments.
2. **Make something personal:** decorating, crochet/yarn themes, and a recognizable companion.
3. **Companions feel present:** customization, expression, and reactions matter more than grinding stats.
4. **Curiosity over jeopardy:** short optional outings add variety without blocking the cozy loop.
5. **Return at your own pace:** offline accumulation is bounded, transparent, and never a pressure tactic.

**Anti-goals [PROPOSAL]:** mandatory real-time social participation, hostile combat as the main mechanic, energy walls that force purchases, punitive pet-neglect systems, unskippable daily chores, artificially scarce paid power, or gameplay that requires constant connectivity.

### 1.3 Audience and platforms

- **SOURCE:** mobile-friendly and PC/web play; primary interactions should suit 1–5-minute sessions.
- **PROPOSAL:** responsive **web-first** delivery for the first playable vertical slice, with touch, mouse, and keyboard support. This is a delivery strategy, **not** approval of React/TanStack/Tailwind/Zustand.
- **OPEN:** whether a native Android/iOS release is a foundational goal or a later adaptation.
- **OPEN:** whether “baby-friendly sessions” means *caregiver-friendly session lengths*, child suitability, or both. No age rating or child-data policy can be inferred from the phrase.

## 2. Player-facing experience

### 2.1 Core loop [SOURCE, formalized as PROPOSAL]

**Return → see companion/home → optionally collect accumulated materials → choose one short activity → craft, decorate, or customize → save and leave.**

The player may also choose to do nothing except visit. Neither an adventure nor an idle claim is required to enjoy the home. Returning after an extended absence must not produce a punishment or accusatory message.

### 2.2 First-session experience [PROPOSAL]

The first launch should offer a simple, immediate path: meet a starter Lumenette (provisionally Pip), choose an initial visual trait, place a decorative object, discover one resource source, and see a clear optional next action. Progress must be saved locally. A player should be able to stop after any completed interaction.

**No account, payment, network, or device-battery permission is required to begin.**

### 2.3 Core feature requirements (candidate acceptance contract)

| ID | Feature | Requirement / acceptance evidence | Trace | Priority |
| --- | --- | --- | --- | --- |
| CORE-01 | Companion | Player can view one expressive Lumenette and change at least its name and one visual attribute; a restart preserves choices. | SOURCE + PROPOSAL | Slice |
| HOME-01 | Home decoration | Player can select, place, move, and remove a decoration without losing it; placement and inventory survive reload. Invalid placements fail gracefully. | SOURCE + PROPOSAL | Slice |
| IDLE-01 | Offline gathering | Elapsed time advances a bounded resource generator without an active tab or network. Identical saved state, elapsed time, and config produce identical results. | SOURCE + PROPOSAL | Slice |
| IDLE-02 | Return/claim | Player sees what accumulated, why it is capped, and can claim it exactly once; repeated clicks/reloads do not duplicate rewards. | SOURCE + PROPOSAL | Slice |
| CRAFT-01 | Make something | One explicit recipe transforms collected resources into a usable decoration or companion accessory, with costs and result visible beforehand. | PROPOSAL | Slice |
| WANDER-01 | Optional outing | At least one self-contained 1–3-minute activity offers a clear objective, completion state, and modest resource/cosmetic reward. It can be declined without blocking the home loop. | SOURCE + PROPOSAL | Slice |
| SAVE-01 | Persistence | Local progress survives ordinary reloads, stores a schema version, handles missing/invalid fields, and provides a documented recovery behavior. | SOURCE + PROPOSAL | Slice |
| UX-01 | Short-session continuity | No required activity forces the player to stay beyond a short session; state is saved at safe points and leaving does not destroy earned durable progress. | SOURCE + PROPOSAL | Slice |
| UX-02 | Accessible interaction | Essential interactions are available without precision dragging alone; readable labels, focus navigation, motion controls, and appropriate feedback are considered in acceptance tests. | PROPOSAL | Slice |
| CONTENT-01 | Data-driven content | Furniture, companion appearance options, recipes, rewards, and outing definitions are describable in content data, separate from core simulation rules. | PROPOSAL | Foundation |
| SOCIAL-01 | Visits | Any future visit system distinguishes real shared data from a labeled simulation; social identity, privacy, moderation, and synchronization must be specified before production. | SOURCE + PROPOSAL | Deferred |
| WIDGET-01 | Home-screen companion | A native mobile widget may display the chosen Lumenette and glanceable information via platform-specific integration; this is **not** claimed to exist in the web slice. | SOURCE + PROPOSAL | Deferred |
| COMMERCE-01 | Paid cosmetics | A future store must disclose purchases, preserve non-paying core progression, and obtain separate requirements for purchase/restore/refund; no checkout is in the first slice. | SOURCE + PROPOSAL | Deferred |

**Slice** means the smallest credible playable vertical slice; **Foundation** is design work required to avoid throwaway coupling; **Deferred** is explicitly not an MVP commitment.

### 2.4 Home and personalization [SOURCE + PROPOSAL]

Supported concept: cottage, garden, and burrow decoration, furniture, rugs, lamps, plants, animal beds, yarn craft motifs, companion colors/patterns/faces/accessories, and photo-sharing opportunities.

For the first slice, implement **one bounded home area**. Do not build all three spaces until the placement model has been tested. Separate *owned objects* from *placed instances*; removing a placement must not destroy ownership. Specify how decorations overlap, rotate, and snap only after a layout experiment.

Lumenettes should communicate through a small set of readable expressions or animations. **No neglected-companion penalty** is proposed. Friendship, mood, and “care” may eventually be expressive systems, but must not covertly become maintenance chores.

### 2.5 Wander excursions [SOURCE + PROPOSAL]

The baseline suggests three interactions: catching drifting skeins, avoiding brambles, and mending a scarf pattern. These are *ideas*, not verified minigames. Prototype each cheaply and choose the strongest first-slice mechanic by observed usability and replay value.

Candidate encounter contract: identifier, presentation content, player controls, explicit objective, outcome, accessibility alternative, base duration target, and reward table. Completion must be resilient to interruption. No permanent failure penalty is specified.

### 2.6 Idle economy and crafting [SOURCE + PROPOSAL]

Idle activity may include gathering yarn/materials, tending garden crops, and making simple items. The source suggests upgrade dimensions of rate, yield, and rare-material chance, plus occasional cooldowns and a maximum offline catch-up period.

For the first slice:

- **One deterministic generator** and **one spending sink** are sufficient to test the loop.
- Store **last simulation timestamp**, generator configuration, claimed/unclaimed resources, and inventory distinctly.
- Calculate offline gains from elapsed time up to a **configurable cap**; clamp negative time deltas and protect against clock manipulation/large jumps.
- Specify whether unclaimed accrual continues after the cap. Make claims idempotent and protect against overflow.
- Rate, yield, drop chance, cooldown, and cap all live in versioned gameplay configuration; do not invent permanent balance values in implementation.
- The README's “couple of hours” for live upgrades and “couple of minutes” in its supposed prototype are **unapproved tuning examples**, not requirements.

**OPEN:** exact resources, number of crafting tiers, what “tokens” purchase, rare-material distribution, inventory limits, and whether players can lose resources. No paid currency is required in the first slice.

### 2.7 Social, visits, and sharing [SOURCE + PROPOSAL]

The intended fantasy includes visiting another player's home, reactions, small gifts, asynchronous sharing, and possibly co-op. These entail accounts, networking, sync conflicts, user-generated content, abuse controls, and data retention. They do **not** belong in the first playable slice.

Photo mode can initially produce a locally saved screenshot without any social backend. If online visits are later approved, define visibility settings, abuse/report/block behavior, rate limits, gift economics, moderation, and deletion before launch. Do not imply that simulated neighbors are real players.

### 2.8 Battery companion and widget [SOURCE, critically assessed]

The pitch mentions an on-device battery widget and a roughly 70%-charge threshold yielding a resource/reward benefit. These are distinct concerns:

1. **Display the companion or charge**: optional presentation, potentially valuable.
2. **Tie progression rewards to battery charge**: a balance, fairness, privacy, and device-behavior decision, **not accepted by default**.
3. **Native home-screen widget**: requires platform-specific work; not equivalent to an in-web-app status card.

**Candidate constraints:**

- Core gameplay works identically when battery information is unavailable or access is denied.
- Do not prompt players to keep a device charging merely to earn game resources.
- No battery polling in the core simulation; a capability adapter reports optional, coarse presentation state.
- An in-app *companion panel* may be prototyped on the web; it must not be labeled a native home-screen widget.
- No device information leaves the device without a separate reviewed requirement.
- **OPEN:** whether the original reward mechanic is actually essential, cosmetic-only, or should be removed.

Compatibility basis: [MDN Battery Status API](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) reports limited web-browser availability; [Apple WidgetKit](https://developer.apple.com/documentation/widgetkit/) and [Android Glance](https://developer.android.com/develop/ui/compose/glance/create-app-widget) are native widget paths.

### 2.9 Monetization [SOURCE, unresolved contradiction]

The source simultaneously says **no purchasable power** and proposes a “Hollow Patron” offering **faster idle**. Faster idle is a gameplay advantage, regardless of whether described as “mild quality-of-life.”

**PROPOSAL:** no payments in the first slice. Later, start with purely cosmetic packs, accessible preview, clear ownership and restoration, and no advantage affecting output, progression, or time pressure. A patron subscription or accelerated idle requires an explicit product decision and a re-evaluation of the no-paid-power promise. Do not silently grandfather it into the spec.

## 3. Technical architecture [PROPOSAL, not a chosen stack]

Prioritize **clear contracts and deterministic behavior**, not framework selection. The README's React, TanStack Start/Router, Tailwind, Zustand, and CSS/SVG list is an unverified suggestion because no package or source exists.

Suggested separations:

| Boundary | Owns | Must not own |
| --- | --- | --- |
| Game rules / simulation | Resource generation, inventory transactions, crafting, bounded time advancement, progression | DOM, native widget APIs, purchases, networking |
| Content definitions | Lumenette palettes/expressions, furniture, recipes, outings, rewards, localized strings | Storage adapters and time sources |
| Application state and use cases | Orchestrate player commands and produce stable view state | Renderer-specific layout or opaque business rules |
| Persistence adapter | Versioned save load/write, migration, defensive recovery, local/export strategy | Economy tuning |
| Presentation | Responsive home, companion, inventory, outings, accessibility and animations | Direct changes to saved totals without game commands |
| Capability adapters | Optional battery data, native widget, share/export, future social and commerce | Core-progression prerequisites |
| Observability / verification | Local diagnostics, deterministic test fixtures, opt-in diagnostics if authorized | Hidden telemetry |

**Minimum command model:** explicit typed operations such as *PlaceDecoration*, *RenameCompanion*, *AdvanceOffline*, *ClaimProduction*, *CraftItem*, and *CompleteOuting*. Define preconditions, effects, and replay/idempotency behavior before implementation.

**State boundary:** versioned save data might include schema version, player identity (local), companion definitions, placed decorations, owned inventory, generator state, progression, and timestamps. This is a schema proposal, not a frozen field list.

**Design rules:**

- Keep clock and randomness injectable for reproducible tests.
- Do not invent a server, authentication, or analytics in the slice.
- Expose tunables and feature flags in centralized configuration, not scattered magic numbers.
- Preserve backward-readable save behavior or explicitly version migrations when state format changes.
- Distinguish local storage from authoritative multiplayer state if/when networking becomes real.
- Prefer a simple renderer and data-driven content over a complicated plugin architecture unless experiments justify it.

## 4. Experience, safety, and quality constraints [PROPOSAL]

- **Accessibility:** usable touch targets, text equivalents for icons, keyboard/focus navigation for essential actions, visible feedback, reduced-motion path, and non-color-only information.
- **Caregiver/time-respecting UX:** safe interruption, instant return to context, gentle non-urgent notifications (prefer none initially), no streak pressure, and no forced daily visit.
- **Performance:** prioritize responsive input and battery-conscious animation on representative low/mid mobile hardware. Set numerical budgets only after choosing target devices and measuring a real build.
- **Security/privacy:** local-first and no accounts in slice; if social or telemetry is added, define data collection, consent, storage, deletion, and child-safety obligations before activation.
- **Visual language:** yarn texture, soft edges, legible stitch faces, distinctive silhouettes, and restrained rural fantasy. Create an art direction sheet and small asset/style experiments; no aesthetic quality can be verified from source today.
- **IP/license:** the README says the creature concept is original and license is TBD. This is an **author statement, not independent clearance**. Obtain a real repository license and asset provenance review before distribution.

## 5. Milestones and completion gates

### M0 — Concept validation and specification approval (this draft)

**Exit evidence:** product owner confirms core fantasy, primary device, audience intent, must-have experiences, widget priority, monetization boundary, and visual references. Ambiguous items are either decided or deliberately deferred. Draft updated to approved version.

### M1 — Playable vertical slice (first code milestone)

**Scope:** one starter Lumenette, one home area, place/move/remove a small set of decorations, one simple generator, one recipe, one short optional outing, local persistence, and responsive navigation.

**Exit evidence:** fresh start → interact → earn → craft → place → save/reload → return offline → claim works under automated checks and a manual phone/desktop test. No real shop, widget, or social claims.

### M2 — Cohesive cozy loop

**Scope:** better visual/audio identity, expressions, expanded decor and recipes, polished onboarding, more than one outing if justified, progression tuning, save migration support, accessibility passes, and usability research.

**Exit evidence:** repeatable short sessions with clear voluntary goals and no dead-end economy; measured completion/interruption observations; stability checks and documented user feedback.

### M3 — External capabilities (separately approved tracks)

**Candidate tracks:** native companion widget, social visits, shared homes/co-op, seasonal content, purchases. Each requires its own product contract, platform/integration validation, moderation/privacy implications, and independent acceptance criteria. None is automatically included in M1/M2.

## 6. Falsifiable design experiments (Kite's proposal)

1. **The two-minute return test:** a low-fidelity loop tests whether returning, gathering, making, and decorating feels rewarding without an outing. **Failure signal:** progress feels mechanical or requires too many screens.
2. **Companion attachment test:** compare a static decorative yarn ball to an expressive, reacting Lumenette. **Failure signal:** expressions add complexity without meaningfully improving comprehension or perceived companionship.
3. **Wander choice test:** prototype the three README activity concepts with matched presentation; observe completion, confusion, and willingness to replay. **Failure signal:** the selected mechanic is simply more novel, not more enjoyable or accessible.
4. **Widget proposition test:** show the same companion concept as an in-app panel and as a native-widget mockup before choosing platform investment. **Failure signal:** little value outside the app, or battery rewards become the only reason to use it.

These are proposed tests, not trials already conducted. Do not collect identifiable telemetry without a reviewed plan and user permission.

## 7. Acceptance tests for the first code milestone

- **T-01 First run:** no existing save, no account, no network → usable home and starter companion.
- **T-02 Persistence:** rename, customize, decorate, reload → exactly the same durable state.
- **T-03 Offline:** same input save + elapsed interval + config → same resource gain; elapsed below zero → no negative award; huge elapsed → configured cap.
- **T-04 Claim:** claiming twice, including reload/retry, cannot award twice.
- **T-05 Transactions:** insufficient crafting resources changes nothing; sufficient resources are consumed once and crafted item appears once.
- **T-06 Placement:** invalid position rejected with explanation; removing a decoration returns the owned object to availability.
- **T-07 Wander:** user may skip; successful completion awards documented result; interruption does not silently duplicate or forfeit earned durable progress.
- **T-08 Device capabilities:** battery API missing/denied, no native widget, network offline → core loop remains fully playable.
- **T-09 Interaction:** complete first-session actions on touch and by keyboard, with non-color-only cues and reduced motion.
- **T-10 Evidence:** CI checks and tested device/browser matrix reported honestly; no “playable” or “complete” label without matching artifact and execution evidence.

Use synthetic test saves and deterministic clocks; these cases are *not yet implemented or executed*.

## 8. Decision register [OPEN — product-owner authority]

| Decision | Options to present | Recommendation | Affects |
| --- | --- | --- | --- |
| D-01 Primary delight | Decorating / Lumenette companionship / Crochet craft / Exploring | Validate which is the main reason to open the game | Core loop |
| D-02 Release target | Web first / Android first / iOS first / shared native+web | Web slice first unless widget is mandatory day one | Architecture |
| D-03 Audience | Time-limited adults/caregivers / families/children / general | Clarify before age, privacy, language and commerce decisions | UX, compliance |
| D-04 Craft mechanics | Recipe inventory / pattern-making interaction / both | Recipe loop first; prototype interaction separately | Economy, content |
| D-05 Battery mechanic | Visual companion only / optional flavor / gameplay bonus | No gameplay bonus until fairness and support proven | Platform, balance |
| D-06 Commerce | None / cosmetic-only / cosmetic + convenience | None in slice; cosmetic-only later | Economy, trust |
| D-07 Social | Local photo export / async visits / live co-op | Local export first; networked features later | Infrastructure, safety |
| D-08 Visual identity | Illustrated 2D / stitched-paper 2D / lightweight 3D | Compare mockups before selecting renderer | Art, performance |
| D-09 Offline limits | Cap, claim cadence and upgrade pacing | Define through config and short-session user testing | Balance |
| D-10 Brand/title | Lumenette Hollow / Hollowlumen / other | Ask owner to choose canonical player-facing name | Branding |

**No decision in this register is presumed answered.**

## 9. Definition of Done and change control

An MVP requirement becomes **DONE** only when (1) its behavior is present in source, (2) acceptance criteria are exercised, (3) adverse/boundary conditions are checked in scope, (4) a repeatable build exists, and (5) limitations are documented. A checkbox in a pitch is not evidence.

Each accepted change to this document should record its decision owner, rationale, source revision, and affected requirement IDs. Separate **product specification** (what experience is wanted), **technical ADRs** (how it will be built), **roadmap** (when), and **test evidence** (what actually works). No implementation has been authorized by this specification alone.
