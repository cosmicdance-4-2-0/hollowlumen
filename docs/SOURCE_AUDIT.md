# Hollowlumen — Baseline Source Audit and Specification Triage

**Audit date:** 2026-11-05  
**Inspected revision:** [ac0317e250bef11c1f12abebe7be023aa41ecb47](https://github.com/cosmicdance-4-2-0/hollowlumen/commit/ac0317e250bef11c1f12abebe7be023aa41ecb47) on main  
**Evidence:** GitHub recursive tree at that revision consists of **README.md only**. There is no source tree, package.json, lockfile, tests, art assets or runnable prototype in the repository.  
**Outcome:** Documentation reconstruction, not feature verification. Read the [product specification draft](PRODUCT_SPEC.md) for proposed replacement requirements.

## 1. Extracted source signals (worth retaining)

| Signal | Evidence in source | Interpretation |
| --- | --- | --- |
| Cozy fantasy life sim | Opening premise, home and companions | Product identity, subject to owner approval |
| Living yarn companions | “Lumenettes”; yarn colors, faces, accessories | Distinctive visual and emotional hook |
| Short, interruptible sessions | 1–5 minute play, 1–3 minute wander | Strong experience principle |
| Personal home space | Cottage, garden, burrow and decoration | Primary expressive system candidate |
| Offline production | Yarn gathering, garden, bounded catch-up | Companion system to active play |
| Optional adventure | Three described outing concepts | Variety without mandatory progression |
| Social warmth | Friend visits, gifts, sharing | Future aspiration, not verified feature |
| Companion out of game | Battery display / native widget fantasy | Platform investigation candidate |
| Fairness promise | No paywalls on core progression | Valuable constraint, contradicted by one pack |
| Example brand elements | Lumenette Hollow, Lumenettes, Pip | Naming candidates, not an approved brand guide |

**Evidence vocabulary:** “Described” does not mean implemented. No external design brief, art references, gameplay prototype, or product-owner interview was provided in the inspected repository.

## 2. Material problems to correct

| ID | Observation | Why it matters | Recommended disposition |
| --- | --- | --- | --- |
| F-01 | README says **Playable prototype**, lists completed roadmap items and provides npm build/run commands; repo has README only. | Unsupported status and unusable onboarding. | Update README after spec approval to say **concept/specification**; only claim builds with evidence. |
| F-02 | “Web prototype” and “battery widget” blur an in-app UI with a real mobile home-screen widget. | Wrong platform commitments; native work is separate. | Define in-app companion panel versus native iOS/Android widget. |
| F-03 | Claimed >~70% battery gameplay bonus rests on API support not guaranteed in browsers. | Cross-platform parity and fairness risk. | Capability-gated optional presentation; owner decides any reward effect. |
| F-04 | **No paid power** clashes with “Hollow Patron” **faster idle**. | Core product promise contradicted. | Defer monetization and explicitly decide cosmetic-only versus paid convenience. |
| F-05 | First MVP includes home, garden, burrow, three minigames, idle, widget, store, and multiplayer simulation. | Unbounded scope for a repository with no application code. | Propose one vertical slice with clear exit criteria. |
| F-06 | Resource economy, crafting process, upgrade costs, caps, rare drops and token purpose are undefined. | No way to build or test consistent progression. | Specify transaction invariants, then tune via config and experiments. |
| F-07 | “Couple of hours” live cooldowns and “couple of minutes” prototype cooldowns are mixed. | Tuning examples can be mistaken for production constants. | Separate illustrative values from approved balance tables. |
| F-08 | “Baby-friendly sessions” is ambiguous. | May imply child audience, caregiver-friendly play, or both. | Ask product owner; do not infer age rating or compliance. |
| F-09 | The stack is named but no package manifest or source verifies it. | Premature technical lock-in. | Defer framework choice until platform and slice constraints are approved. |
| F-10 | “Friends can visit” but “real multiplayer visits simulated.” | Social expectations and data boundaries are unclear. | Mark mock behavior as mock; networked interaction deferred. |
| F-11 | No state schema, sync strategy, offline clock policy, failure recovery, or save migration plan. | Progress loss/duplication risk in a persistence-led game. | Make deterministic state and versioned saves part of slice foundation. |
| F-12 | No acceptance criteria, test fixtures, target device matrix, art direction package, or license. | Neither correctness nor readiness can be established. | Add measurable gates and explicit owners before calling anything shipped. |

## 3. Source-to-spec trace

- **Premise / tone / loop** → Product spec §§1–2.
- **Home / decoration / Lumenettes** → §§2.3–2.4.
- **Short trips / optional activities** → §§2.3, 2.5.
- **Idle / capped catch-up / yarn economy** → §§2.3, 2.6.
- **Friends / gifts / photo mode** → §§2.3, 2.7.
- **Battery / widget** → §§2.3, 2.8.
- **Shop / patron pack** → §§2.3, 2.9.
- **Technology / platforms / saves** → §§1.3, 3–4.
- **Roadmap, completion, missing evidence** → §§5, 7, 9.

## 4. What this draft intentionally did not do

- Did not infer the product owner's consent, priorities, demographics, monetization policy, or favorite art style.
- Did not implement gameplay, create a build manifest, or fabricate demo screenshots.
- Did not lock a framework, rendering engine, cloud backend, or monetary model.
- Did not copy unverified README completion checkmarks into an engineering roadmap.
- Did not modify the original README; historical source claims remain available for review, and its status must be corrected before describing this repository as a runnable prototype.

## 5. Suggested next review checkpoint

Obtain product-owner answers to **D-01, D-02, D-04, D-05, D-06 and D-08** in the product spec. Produce 2–3 low-cost visual mockups and one interaction loop, select a candidate, then promote the accepted document to **v0.2 approved design baseline**. Only then choose technology and commission the M1 executable slice.

External technical verification references:

- [MDN Battery Status API — limited availability](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API)
- [Apple WidgetKit](https://developer.apple.com/documentation/widgetkit/)
- [Android Glance app widgets](https://developer.android.com/develop/ui/compose/glance/create-app-widget)
