# Hollowlumen Design Language — Lavender & Loop

**Version:** 0.1.0-draft  
**Status:** PROPOSED visual design direction, not approved branding  
**Date:** 2026-11-05  
**Basis:** Product direction in [PRODUCT_SPEC.md](PRODUCT_SPEC.md); user-established preference for **purple and pastels**  
**Scope:** Game, collection, critters, patterns, and favorite phone widget

> **Tiny wonders, stitched with care.**

## 1. The identity

**Working name of visual system:** **Lavender & Loop**. This is an internal design-system name, not a proposal to rename the game.

Hollowlumen should look like an **illustrated crochet keepsake box that came to life**: lavender skies, soft paper, loops of yarn, hand-stitched detail, tiny expressive critters, and enough visual restraint that individual creatures feel special.

Three reference words: **tactile · tender · curious**.

- **Tactile:** materials resemble actual crocheted yarn, sewn seams, and soft fabric; handmade imperfections are deliberate.
- **Tender:** forms are round, animation is gentle, expressions are affectionate without guilt or coercion.
- **Curious:** unlocked patterns and individual critters should feel like small discoveries, not resource production machines.

**Avoid:** generic candy-colored mobile-game gloss, casino rewards, shiny plastic bodies, thick neon outlines, baby-product typography, omnipresent glitter, overly detailed backgrounds, and UI screens that compete with the critters. Soft does not mean washed-out or indistinct.

**Signature visual:** a little crocheted creature on a warm ivory field, surrounded by a subtle loose loop of lavender thread. The thread loop appears in selected states, decorative section headings, and a possible logo mark; it is not required around every component.

## 2. Color — purple is the home; pastels are the inhabitants

### Primary palette (initial exact tokens)

| Token | Hex | Use |
| --- | --- | --- |
| \`--hl-canvas\` | \`#FBF8FF\` | App background, off-white with lavender undertone |
| \`--hl-paper\` | \`#FFF9F4\` | Warm paper/ivory panels, collection pages |
| \`--hl-surface\` | \`#FFFFFF\` | Interactive elevated cards |
| \`--hl-lavender-mist\` | \`#F3EEFF\` | Subtle panel background |
| \`--hl-lilac\` | \`#E8DAFA\` | Soft lavender areas, selected-card fills |
| \`--hl-orchid-thread\` | \`#D8C3F2\` | Decorative lines, highlights, yarn |
| \`--hl-wisteria\` | \`#BEA5E5\` | Stronger decorative accents; do not use for small text |
| \`--hl-plum-ink\` | \`#332940\` | Main type, icons, readable critter eye embroidery |
| \`--hl-muted-ink\` | \`#635574\` | Secondary text on pale surfaces only |
| \`--hl-action\` | \`#67438D\` | Primary buttons, actionable links, focus-related accents |
| \`--hl-action-hover\` | \`#563579\` | Hover/pressed action |
| \`--hl-outline-soft\` | \`#D7CBE2\` | Decorative dividers, **not** sole indication of controls |
| \`--hl-focus\` | \`#6A3FA0\` | Visible keyboard focus ring |

### Companion palette (variety, not interface status)

| Token | Hex | Role |
| --- | --- | --- |
| \`--hl-mint\` | \`#D8F1E6\` | Cool mint yarn / restful accents |
| \`--hl-blush\` | \`#F9DDEB\` | Dusty pink yarn / affectionate detail |
| \`--hl-peach\` | \`#FFE2D1\` | Apricot/peach yarn / warmth |
| \`--hl-buttercream\` | \`#F8E9BF\` | Soft golden yarn / playful accents |
| \`--hl-periwinkle\` | \`#DFE8FF\` | Blue-violet yarn / calm variation |

**Distribution guideline [PROPOSAL]:** the environment favors lavender and warm paper; *creatures can be any yarn color* offered by the game's content. Do not tint all creatures toward the brand purple or make rare traits identifiable by color alone. The brand identity should survive a collection screen full of green and orange critters.

**Use sparingly:** saturated orchid, gold foil, sparkles and other premium effects. No neon rarity classification and no purchase psychology coded into color.

### Verified sample contrasts (WCAG luminance calculation)

| Foreground / background | Contrast | Intent |
| --- | --- | --- |
| Plum ink \`#332940\` / canvas \`#FBF8FF\` | ~13.04:1 | Body text, pass |
| Muted ink \`#635574\` / canvas \`#FBF8FF\` | ~6.48:1 | Secondary text, pass |
| Muted ink \`#635574\` / lilac \`#E8DAFA\` | ~5.14:1 | Secondary text, pass |
| White \`#FFFFFF\` / action \`#67438D\` | ~7.60:1 | Button label, pass |
| Action \`#67438D\` / paper \`#FFF9F4\` | ~7.27:1 | Text links, pass |
| Soft outline \`#D7CBE2\` / canvas \`#FBF8FF\` | ~1.48:1 | **Decorative only**; not a sufficient control boundary |

For ordinary text, target **≥4.5:1**; large text and essential graphic controls **≥3:1** according to WCAG AA. **Muted ink on \`#D8C3F2\` is only ~4.22:1** and therefore must **not** be used for normal-sized text there. The numeric tests above cover specific pairings, not every possible combination or a full accessibility audit.

References: [W3C WCAG 2.2 contrast minimum](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [MDN color contrast](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable/Color_contrast).

## 3. Surfaces and geometry

- Use **soft paper over lavender mist**. The background is nearly plain; keep texture in illustration, not the text-reading layer.
- **Cards:** 16–20px radius. Soft shadow and optional stronger boundary when actionable.
- **Buttons:** 14–18px radius, filled deep plum-violet for the primary action, outlined/surface treatment for secondary actions.
- **Stickers/chips:** pill shape for labels such as *Favorite* or pattern complexity; color must not be the only meaning cue.
- **Spacing:** an 8px rhythm with half steps where needed (4 / 8 / 16 / 24 / 32).
- **Borders:** one or two visible line weights; avoid stacked borders, multiple shadows, and faux depth everywhere.
- **Texture:** subtle yarn grain, stitch edges, sewn labels, and irregular thread loops **only** where they clarify material or provide identity.
- **Hierarchy:** a soft large critter portrait followed by plain-language actions; avoid busy dashboards and stacked resource meters.

**The creature is the hero.** A page should be legible with the decorative thread motifs disabled.

## 4. Typography

Proposed typographic character: rounded, human, and quietly playful.

- **UI text:** native system sans/rounded UI where available; do not add network-dependent fonts before testing device support and licensing.
- **Display headings:** a restrained rounded display face may be evaluated later. No cursive script for gameplay controls, quantities, pattern names, or small labels.
- **Body:** approximately 16px default, line height 1.45–1.6.
- **Small labels:** approximately 14px; do not shrink important mobile controls to fit.
- **Headings:** scale around 22–30px depending on viewport; warmth through weight and whitespace, not ornate letterforms.
- **Numbers:** readable in inventory and pattern requirements; use tabular numerals for changing values when appropriate.
- Use sentence case: **“Your critters”**, **“Make a critter”**, **“Favorite”**. Avoid all-caps headings as the dominant voice.

Example fallback stack: \`ui-rounded, system-ui, -apple-system, "Segoe UI", sans-serif\`.

## 5. Critter art grammar

Amigurumi craft cues should be **credible**, not generic fuzzy blob art.

### Construction

1. Show **crocheted stitch structure** (small V-shaped stitch rows/spirals, especially around rounded volumes) at close view. Avoid knitting cables and woven checkered fabric as the default creature texture.
2. Build recognizable **silhouettes**. Starter patterns can be one ball; later patterns may have ears, tails, feet, antennae, or multipart bodies. Silhouette should still read at widget size.
3. Display occasional seam, stitch tension and yarn variation. Avoid perfectly smooth plastic or hyper-detailed realism that becomes visual noise on mobile.
4. Make faces from **embroidered stitch shapes** (eyes, mouths, blush details). Expressions should be readable at thumbnail size.
5. Use accessories sparingly: bows, tiny scarves, flower loops, yarn tufts. The accessory should not hide the creature's defining features.

### Pattern vs individual

- **Pattern** determines available body plan, number/type of parts, and which visible traits can vary.
- **Individual critter** determines actual yarn colors, expressed trait variations, stitched face, name and favorite status.
- **Mood/behavior** changes pose, blink, bounce, look direction and facial expression; it need not rewrite anatomy.
- **Future genetics** might change ear length, markings, colors or ornament styles within the pattern's allowed trait slots. Do not draw all combinations before the inheritance experiment exists.

**Draft art test:** place three critters from one pattern side-by-side. They should be recognizably of the same pattern, but clearly different *individuals*. Then place a critter from a more advanced pattern beside them; the silhouette should signal the pattern distinction without needing a complexity number.

## 6. Motion and sound

### Motion [proposal]

- A tiny **breathing/squish loop** and occasional blinking make a critter feel present. Avoid constant restless bouncing.
- **Pet/tap response:** short squash-and-stretch, blink, slight head lean, or happy stitch-eye change.
- UI transitions: approximately **180–300ms** (tuning candidate, not architecture constant).
- Critter loops: slow, irregular and low-amplitude; do not infer that a native widget can animate continuously.
- Respect operating-system reduced motion. Reactions must remain understandable without animation.
- No high-frequency flashes, intense sparkles, or movement required to understand critical state.

### Sound [future art direction]

Optional tactile sounds: muffled yarn pluck, little wooden-button click, soft chime on a new pattern, small expressive squeaks. No automatically playing ambience in the first prototype; users control audio and it must not be needed for gameplay comprehension.

## 7. Interface vocabulary

| Screen or piece | Visual behavior |
| --- | --- |
| **My critters** | A roomy collection of portrait cards; portrait is largest element, name below, favorite symbol visible |
| **Critter detail** | One large companion on a paper-like stage; \`Pet\`, \`Play\`, and \`Set favorite\` as explicit, easy-to-tap controls |
| **Pattern book** | An illustrated scrapbook of stitch patterns; locked patterns show meaningful silhouette previews without burying players in stats |
| **Make a critter** | Simple patterned recipe/creation sequence, not a manufacturing dashboard; reveal the new individual as a charming event |
| **Favorite selected** | A subtle lavender thread loop, small heart, and accessible \`Favorite\` text; no permanent pulsing highlight |
| **Empty collection** | Friendly illustration plus one clear action, no shame/guilt |
| **Achievements or genetics later** | May use stitch-tag and specimen-card metaphors; do not add screens or complex visual controls ahead of actual features |

### Naming and microcopy

Write like a gentle craft story, **not** an engagement-optimized mobile game.

Use: “A new pattern!”, “Meet your little friend”, “Pip looks curious”, “Choose a favorite”, “Your collection”.

Avoid: “Hurry!”, “Your pet misses you!”, “Don't lose your streak!”, “Claim before time runs out!”, “Upgrade now!”

Use explicit verbs and state changes; the UI should not hide what an action will do.

## 8. Favorite phone-widget language

The home-screen widget is a **core product aspiration**. Its visual language must survive constrained sizes, dark mode, tint/desaturation and platform typography. [Apple's widget guidance](https://developer.apple.com/design/human-interface-guidelines/widgets) stresses glanceability, readable type, and color-independent meaning.

**Small widget composition [proposal]:**

- One large, unmistakable critter portrait and a calm off-white/lavender background.
- If room permits: the critter's short name and one simple expression/mood indicator.
- Optional tiny stitched corner label; do not crowd the creature with meters, currencies, decorative ribbons or the app logo.
- A system-supported tap action can take the player to that critter in the app.
- The companion’s **identity** should survive tinted or monochrome widget appearances via silhouette, face and stitched detail, not only hue.
- Include an offline/default state and a missing-favorite placeholder. Do not imply continuously running animations or battery-based rewards.

**Prototype test:** design portrait art at 64px, 96px, and 160px; verify that face, silhouette, and main accessory remain identifiable. Create dark, light, tinted, and high-contrast examples before choosing final widget assets.

## 9. Reusable design tokens (reference mapping)

These names are descriptive proposals, not a mandated CSS/runtime design system:

~~~css
:root {
  --hl-canvas: #FBF8FF;
  --hl-paper: #FFF9F4;
  --hl-surface: #FFFFFF;
  --hl-lavender-mist: #F3EEFF;
  --hl-lilac: #E8DAFA;
  --hl-orchid-thread: #D8C3F2;
  --hl-wisteria: #BEA5E5;
  --hl-plum-ink: #332940;
  --hl-muted-ink: #635574;
  --hl-action: #67438D;
  --hl-action-hover: #563579;
  --hl-outline-soft: #D7CBE2;
  --hl-focus: #6A3FA0;

  --hl-mint: #D8F1E6;
  --hl-blush: #F9DDEB;
  --hl-peach: #FFE2D1;
  --hl-buttercream: #F8E9BF;
  --hl-periwinkle: #DFE8FF;

  --hl-radius-card: 18px;
  --hl-radius-button: 16px;
  --hl-space-unit: 8px;
}
~~~

Tokens should remain semantic and be mapped into whatever platform implementation is selected. This code sample is **not a commitment to a web stack**.

## 10. Design validation checkpoints

**DV-01 — Color and readability:** confirm primary button labels, normal text, icons, and actionable boundaries pass applicable contrast checks on each actual surface; don't merely assume pastels are accessible.

**DV-02 — Distinct critters:** at least three yarn/trait variants remain distinguishable in one pattern; different patterns read as different silhouettes.

**DV-03 — Size ladder:** each test critter remains recognizable at small widget, collection card, and full portrait scale.

**DV-04 — Usability:** a fresh player can find their collection, inspect a pattern, pet a critter, and select a favorite without relying on decorative symbols alone.

**DV-05 — Gentle motion:** animated and reduced-motion versions convey the same meaningful information.

**DV-06 — Widget adaptation:** do not approve visuals without seeing light/dark/tinted samples on the actual target mobile platform.

**DV-07 — Originality/licensing:** inspiration images are reference only. Produce original critter models and artwork; document asset authorship/licensing before release.

## 11. Open design choices

- Is the illustrated world more **storybook-flat** or **tactile dimensional plush**? Test one critter in each style, then commit.
- What are the two or three **signature starter critter silhouettes**?
- Does the favorite critter live on a **plain soft background**, a miniature nest, or a pocket/scrapbook frame?
- Should the world use one perpetual lavender daylight atmosphere, or distinct pastel palettes by biome?
- Is light/dark theme a first-version deliverable or a widget-specific requirement before broader app theming?

**Recommendation:** begin with tactile, slightly dimensional crochet creatures on clean illustrated paper-like UI. Do not build a shader-heavy 3D world or entire bespoke icon library merely to prove a first critter is charming.
