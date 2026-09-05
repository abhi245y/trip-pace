---
name: Trip pace
description: A watch-keeper's log of a passage — ruled ledger bands on night-watch ground, read at two distances.
colors:
  ground: "#0b1a24"
  band: "#0e212f"
  ink: "#f4ede0"
  ink-2: "#7d9aa8"
  rule: "#1d3a4a"
  rule-lit: "#2f5b70"
  brass: "#c8500f"
  brass-lit: "#e0821f"
  oxide: "#e0654a"
  verdigris: "#6f9e8f"
  standby-ground: "#000000"
  standby-rule: "#1c1c1c"
  standby-ink-2: "#8d9aa2"
typography:
  hero-numeral:
    fontFamily: "Bodoni Moda, Didot, Times New Roman, serif"
    fontSize: "clamp(104px, 30vw, 138px)"
    fontWeight: 650
    lineHeight: 0.9
    letterSpacing: "-0.005em"
    fontVariation: "'opsz' 22"
    fontFeature: "tabular-nums"
  numeral:
    fontFamily: "Bodoni Moda, Didot, serif"
    fontSize: "21px"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: "0.01em"
    fontVariation: "'opsz' 16"
    fontFeature: "tabular-nums"
  numeral-lg:
    fontFamily: "Bodoni Moda, Didot, serif"
    fontSize: "52px"
    fontWeight: 500
    lineHeight: 1
    fontFeature: "tabular-nums"
  label:
    fontFamily: "Archivo, -apple-system, system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 600
    letterSpacing: "0.14em"
  body:
    fontFamily: "Archivo, -apple-system, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
  standby-display:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(72px, min(56cqb, 42cqi), 220px)"
    fontWeight: 600
    lineHeight: 0.98
    letterSpacing: "-0.015em"
    fontFeature: "tabular-nums"
  standby-mid:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(34px, min(22cqb, 19cqi), 96px)"
    fontWeight: 600
    lineHeight: 1.06
    letterSpacing: "-0.01em"
    fontFeature: "tabular-nums"
  standby-label:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(13px, 4cqi, 22px)"
    fontWeight: 600
    letterSpacing: "0.22em"
rounded:
  none: "0"
  mark: "50%"
spacing:
  hair: "4px"
  tight: "9px"
  row: "12px"
  band: "14px"
  gutter: "18px"
  loose: "26px"
components:
  button:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "13px 16px"
  button-hover:
    textColor: "{colors.brass-lit}"
  button-primary:
    backgroundColor: "{colors.brass}"
    textColor: "#ffffff"
    rounded: "{rounded.none}"
    padding: "13px 16px"
  button-primary-hover:
    backgroundColor: "{colors.brass-lit}"
    textColor: "#2a1200"
  button-sm:
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "9px 12px"
  input:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "9px 2px"
    size: "16px"
  band:
    backgroundColor: "{colors.ground}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "14px 0 16px"
  row:
    textColor: "{colors.ink-2}"
    rounded: "{rounded.none}"
    padding: "9px 0"
  state-mark:
    backgroundColor: "{colors.ink-2}"
    rounded: "{rounded.mark}"
    size: "7px"
---

# Design System: Trip pace

## Overview

**Creative North Star: "The Deck Log"**

This is a watch-keeper's record of a passage, not a dashboard. The discipline of a log is stating what was run honestly, including the stretches nobody observed — so the system's entire structural vocabulary is ruled entries on dark paper, and its most important invention is a set of rules that say *how* a number was come by, not just what it is. It refuses the near-black-plus-neon-gauge instrument cluster the category ships: there is no gauge, no glow-for-its-own-sake, no card, no rounded panel, no glass.

Structure is carried entirely by hairline rules. Every band, every entry, every column division is a 1px line; nothing is a container. Colour is scarce and confined to rules, fills and marks, and the ink is warm log-paper cream (`#f4ede0`) on deep night-watch ground (`#0b1a24`) — the paper is the ink, not the background. Numerals are the material and everything else is the margin: labels are small, condensed and set in small-caps rhythm so they read as a clerk's marginalia beside engraved figures.

The system serves two reading distances and treats that split as a first-class rule rather than an inconsistency. The in-hand page is a printed page: Bodoni Moda with pinned optical sizes carries every numeral. The mounted standby display is an engraved plate read in a fraction of a second from a windscreen mount, often rotated 90°, where Bodoni's horizontal hairlines drop out — so Archivo, wide and heavy, carries every standby numeral. Behind both sits one live WebGL material: the log's own ruled paper streaming under a pen, its rule density, travel and tint driven by real speed and trip state.

**Key Characteristics:**
- Hairline rules carry all structure; there are no cards, panels, or filled containers.
- Rule weight and mark carry state: solid = observed, dashed = reckoned, doubled = a stop entry.
- Two type systems for two reading distances: engraved Bodoni in hand, extended Archivo at a glance.
- The width axis works in both directions: labels condensed to 75%, glance numerals extended to 110%.
- Colour is confined to rules, fills and marks; brass is never text.
- A single live WebGL field is the only image in the system, and it is driven by real data.

## Colors

A night-watch palette: deep ink ground, warm log-paper cream as the ink, oxide brass for marks, and two state hues held in reserve.

### Primary
- **Oxide Brass** (`#c8500f`): the log's mark. Used exclusively as a non-text colour — the doubled rule above a stop entry, the primary action fill, selected-item borders, the engraved corner brackets on the control band, and the selection ground. It fails 4.5:1 as text on ground, which is why the system carries a lit sibling.
- **Lit Brass** (`#e0821f`): brass wherever it must be read as text or as a focus ring — hovered control lettering, the stop entry's heading, the brief-stop line, the focus outline, and the caret.

### Secondary
- **Oxide Red** (`#e0654a`): stopped. The stopped-duration numeral, error messages, and the stopped state mark.
- **Verdigris** (`#6f9e8f`): under way. The moving state mark, confirmation messages, and the doubled rule above the passage summary.

### Neutral
- **Night Watch** (`#0b1a24`): the ground for every surface on the in-hand page, and the halo colour behind large readouts.
- **Band Ground** (`#0e212f`): the ruled band's ground, one step up from the page.
- **Log Paper** (`#f4ede0`): the ink. All primary numerals and control lettering.
- **Sea Grey** (`#7d9aa8`): labels, secondary entry text, reckoned values, and the resting state mark.
- **Rule** (`#1d3a4a`): the hairline that carries structure — band tops, entry tops, column divisions.
- **Lit Rule** (`#2f5b70`): the emphasised hairline — the masthead's 2px underscore, control borders, input underlines, and the dashed reckoned rule.
- **Standby Ground** (`#000000`), **Standby Rule** (`#1c1c1c`), **Standby Sea Grey** (`#8d9aa2`): the mounted display's own three-value neutral set. The standby drops to true black because it is read at a glance on a mounted screen and its rules must be nearly invisible.

### Named Rules
**The Brass-Is-Not-Ink Rule.** `--brass` never sets a text colour. It draws rules, fills, bracket marks and the selection ground; where brass must be read as lettering, `--brass-lit` is the only permitted value. Audit test: search the stylesheet for `color:var(--brass)` — there must be zero hits.

**The Colour-Is-Reserved Rule.** Hue appears only on rules, fills and marks. No paragraph, label, heading or ordinary numeral is coloured; the entire in-hand page is cream and sea grey until a state occurs.

**The State-Hue Trio Rule.** Only three hues encode state — verdigris under way, lit brass at a brief stop, oxide when stopped — and each one appears simultaneously on the status mark, the message line and the WebGL field's tint. State is never signalled by one lone element.

## Typography

**Display Font:** Bodoni Moda (with Didot, Times New Roman, serif) — variable optical size axis, 6–96
**Body / Label Font:** Archivo (with -apple-system, system-ui, sans-serif) — variable width axis, 62–125

**Character:** An engraver and a clerk. Bodoni's high-contrast, hairline-serif figures give every in-hand numeral the weight of something struck into a plate; Archivo's condensed small-caps labels are the clerk's hand in the margin beside it. Nothing in the system is set in a display face at body size, and nothing is set in a sans at hero size on the in-hand page.

### Hierarchy
- **Hero Numeral** (Bodoni Moda, 650, `clamp(104px, 30vw, 138px)`, line-height .9, `opsz` pinned to 22): the present-speed readout, the one figure the page is built around. Centred, over the live field.
- **Large Numeral** (Bodoni Moda, 500, 52px, line-height 1): the stopped-duration figure in a stop entry, set in oxide.
- **Column Numeral** (Bodoni Moda, 600, 26px, `opsz` 16): the coverage grid's three-across values.
- **Entry Numeral** (Bodoni Moda, 600, 21px, `opsz` 16): the value at the right edge of every ruled entry, and the manual-target input.
- **Marginal Numeral** (Bodoni Moda, 600, 20px, `opsz` 16): moving avg / trip avg / maximum under the hero, set as tracked marginal entries.
- **Label** (Archivo, 600, 11px, width 75%, uppercase, letter-spacing .14–.24em): every heading, unit, status line, control and column caption on the in-hand page. One recipe, one size; only the tracking varies with how much air the label has.
- **Body** (Archivo, 400–500, 13–14px, line-height 1.5): entry descriptions, stop-entry prose, and notes.
- **Standby Display** (Archivo, 600, width 110%, `clamp(72px, min(56cqb, 42cqi), 220px)`): the primary glance numeral on the mounted display.
- **Standby Mid** (Archivo, 600, width 110%, `clamp(34px, min(22cqb, 19cqi), 96px)`): the secondary glance readouts.
- **Standby Label** (Archivo, 600, width 75%, `clamp(13px, 4cqi, 22px)`, letter-spacing .22em, uppercase): captions under glance readouts.

### Named Rules
**The Two-Distances Rule.** Bodoni Moda carries every numeral on the in-hand page; Archivo carries every numeral on the mounted standby display. This is not a drift, it is the system: rotated 90° and read from a windscreen mount at a fraction of a second, Bodoni's horizontal hairlines drop out and its 1 and 4 read as slabs. The mounted display is an engraved plate, not a printed page. Any new surface must declare which distance it belongs to and take that surface's face whole.

**The Pinned Optical Size Rule.** Every Bodoni numeral pins `font-variation-settings:'opsz'` — 22 on the hero, 16 on every smaller numeral. Left to auto, the browser resolves near 96 at hero size, the thinnest cut in the loaded range, and the numeral 4 loses its crossbar. Optical size is load-bearing here, not stylistic: never ship a Bodoni numeral without a pinned `opsz`.

**The Both-Ways Width Rule.** The variable width axis runs in both directions and the direction encodes distance. Labels are condensed (75%) at every size, on both surfaces. Glance numerals are extended (110%, 105% in the standby key-value block). Nothing in the system sits at the default width.

**The Tabular Rule.** Every numeral carries `font-variant-numeric:tabular-nums`, so a changing readout never shifts its neighbours. The one deliberate exception is the odometer drum, where Bodoni ships no tabular figures: the drum strip carries all ten digits and sizes itself to the widest, because a fixed 1ch slot lets an 8 overlap.

## Layout

A single centred column, 560px maximum, with an 18px gutter and safe-area-aware top and bottom padding — the same column at every viewport width. There are no width breakpoints in the system; the only mode switch is orientation, and `prefers-reduced-motion` is the only other media condition. Desktop and mobile render the identical column at identical height.

Vertically the page is a stack of ruled bands: a masthead (a status line and GPS accuracy, closed by a 2px lit rule), the current watch (hero numeral, unit line, three tracked marginal entries divided by vertical hairlines), then ruled log bands, then the engraved control band at the foot. Bands separate by a `border-top` hairline and 14px/16px internal padding; entries within a band separate by their own hairline and 9px padding, with the first entry's rule suppressed so a band never doubles its own top rule.

Columnar readouts use an equal three-across grid whose cells divide by vertical hairlines and align outward — first cell left, last cell right, middle centred — so the block reads as a ruled table, not three centred tiles.

The mounted standby display is a two-pane grid filling the viewport, each pane a vertically scroll-snapped stack of full-height widgets with a page-dot indicator, divided by a vertical hairline that fades out at both ends. When entered from portrait it rotates 90° and swaps its own width and height.

### Named Rules
**The Rules-Carry-Rhythm Rule.** There is no spacing scale to conform to. Vertical rhythm is set by hairline rules and the padding that hangs off them (9px inside an entry, 14/16px inside a band, 26px around the hero). Do not retrofit a modular scale; add a rule and hang its padding.

**The Own-Pane Scaling Rule.** The standby display sizes off its own pane, never the viewport: each pane is `container-type:size` and every standby size is expressed in `cqb`/`cqi`. Viewport units collapse to their clamp floors in the rotated landscape branch. Any new standby widget uses container query units.

## Elevation & Depth

The system has no depth model. Nothing is lifted, nothing floats, and no shadow describes a surface above another surface — there is no ambient shadow, no elevation ramp and no layering. Shadows exist in three specific non-depth jobs only, and each is doing legibility or notation work.

### Shadow Vocabulary
- **Legibility halo** (`text-shadow: 0 0 16px var(--ground)`, 18px in `#000` on standby, 10–12px on smaller labels): a zero-offset scrim, in the ground colour, sitting under any readout that overlays the live WebGL field. It is not decoration; it is what keeps a cream numeral readable against a moving canvas. Zero offset is mandatory — an offset halo would read as a drop shadow.
- **Live-speed bloom** (`0 0 calc(var(--lit,0)*34px) rgba(224,130,31, calc(var(--lit,0)*.4))`, 44px in warm amber on standby): a second halo whose radius and alpha are driven from a live `--lit` custom property set from real speed. Zero offset, same rule as above.
- **Doubled rule** (`box-shadow: inset 0 3px 0 -2px`, paired with a 1px `border-top` in the same colour): the log's doubled rule, not a shadow at all. Brass above a stop entry, verdigris above the passage summary.
- **State pulse** (`box-shadow: 0 0 0 0 → 0 0 0 9px rgba(244,237,224,0)` on a 2.6s / 1.3s / .9s beat): an expanding ring off the status mark, its tempo carrying state. Suppressed under `prefers-reduced-motion`.

### Named Rules
**The No-Depth Rule.** No shadow in this system describes elevation. A shadow may be a legibility scrim (zero offset, ground colour), a doubled rule, or a pulse. Anything offset, anything soft-grey, anything implying a light source above a raised card, is out of world.

## Shapes

Rectilinear and unfilled. No panel, band, entry, control or field carries a corner radius — `border-radius:0` is set explicitly on controls and inputs so no user-agent style can round them, and nothing in the system is a rounded container. The only curve in the whole system is the round state mark: the 7px status dot and the 5px standby page dots, both full circles (`border-radius:50%`), which are marks rather than surfaces.

Form is drawn, not filled. Bands and entries are open — a hairline top rule and air, never a background block. Controls are a 1px lit-rule outline over transparent ground; the one filled control in the system is the primary action, and it fills with brass rather than gaining a shape. Inputs are a single bottom rule with no box at all, and a disabled input switches that rule to dashed, borrowing the reckoned notation.

The one added ornament is the engraved corner bracket: 7px L-shaped brass marks at the top-left and bottom-right of each control-band button, drawn as two `::before`/`::after` half-borders. They exist because the control band was the one place the page fell back to a plain rectangle. On the primary action they turn translucent white; on hover they light to brass.

### Named Rules
**The No-Container Rule.** Structure is drawn with hairline rules, never with a box. If a grouping needs to be legible, give it a rule and a heading — not a card, not a fill, not a radius, not glass.

## Components

### Ruled Band
- **Character:** a page of the log, opened by a rule and a small-caps heading.
- **Shape:** 1px top rule in `--rule`, square, 14px top / 16px bottom padding, no background of its own.
- **Heading:** the label recipe (11px / 600 / width 75% / .2em / uppercase) in sea grey, 12px below.

### Ruled Entry
- **Character:** one line of the log — description on the left, value hard right.
- **Shape:** 1px top rule, 9px vertical padding, baseline-aligned; the first entry in a band drops its rule.
- **Type:** 14px sea grey description against a 21px Bodoni value in cream.
- **Reckoned variant:** the top rule becomes dashed in lit rule, and the value drops to sea grey. This is the system's notation for a value reckoned rather than observed.

### Stop Entry
- **Character:** a stop stated as a log entry, never as an alert.
- **Shape:** doubled rule in brass across the top (a 1px border plus an inset 3px box-shadow), square, band padding.
- **Colour:** heading in lit brass, the stopped-duration figure at 52px Bodoni in oxide, supporting prose in sea grey with cream Bodoni figures inline at 15px.
- **Sibling:** the passage summary uses the identical doubled rule in verdigris, with a two-across grid whose cells rule between rows.

### Controls
- **Shape:** square (`border-radius:0`), 1px lit-rule outline, transparent ground, 13px/16px padding; small variant at 9px/12px.
- **Type:** the label recipe at 12px with .18em tracking, uppercase, cream.
- **Hover:** border to brass, lettering to lit brass, over a .2s ease on border, colour and background.
- **Focus:** 2px lit-brass outline at 2px offset. **Disabled:** .5 opacity.
- **Primary:** brass fill, brass border, white lettering; on hover the fill lights to `#e0821f` with near-black `#2a1200` lettering.
- **Control band:** three flush buttons sharing one lit rule above, each carrying its engraved corner brackets.
- **Selected:** list and unit buttons mark selection with a brass border and lit-brass lettering — never with a fill.

### Inputs
- **Style:** no box. Transparent ground, a single 1px lit-rule bottom border, square, 16px, tabular figures, lit-brass caret.
- **Placeholder:** sea grey at full opacity. **Disabled:** sea grey text and a dashed bottom rule.
- **Numeric variant:** 104px wide, right-aligned, 21px Bodoni.

### Status Mark
- **Character:** the watch's pulse in the masthead.
- **Shape:** a 7px circle, the one round object in the system.
- **States:** sea grey at rest, verdigris under way, lit brass at a brief stop, oxide when stopped; each beats a cream ring outward on its own tempo (2.6s / 1.3s / .9s), suppressed under reduced motion.

### Odometer Drum
- **Character:** a mechanical drum, not a counting number.
- **Behaviour:** each digit column is a strip of ten cells translated by its own place value, so the ones column rolls continuously and higher columns turn only on carry; every drum rests on a whole digit. Transition `.45s cubic-bezier(.2,.8,.2,1)`, disabled under reduced motion.
- **Shape:** each cell is `1em` tall with hidden overflow; the strip is unconstrained in width so it sizes to its widest glyph.

### The Velocity Field
- **Character:** the material of the world — the log's ruled paper streaming under a pen.
- **Behaviour:** one inline WebGL fragment shader, additively blended, drawing four depths of hairline rules whose ink weight, dash length and travel speed follow real speed; a rule never draws a full cell, because a continuous rule stops reading as travel. Frozen under reduced motion.
- **Tint by state:** log-paper ink under way, sea grey idle, brass at a brief stop, oxide when stopped.
- **One context, two mounts:** the same canvas is moved between the page hero (amplitude .5, vignette .8) and the standby display (amplitude .42, vignette .88). The vignette holds the centre back so numerals stay the brightest thing on screen.

### Standby Widget
- **Character:** the engraved plate, read in a glance.
- **Shape:** a full-pane flex column, centred, scroll-snapped, padded in container units (3cqb / 4cqi); no rule, no border, no box.
- **Type:** extended Archivo numerals over a condensed Archivo caption; key-value blocks rule between rows in `#1c1c1c` with condensed uppercase keys at .62em against right-aligned extended values.
- **Accents:** the three glance state colours — `#8fbfa8` ok, `#e0a86e` amber, `#e0654a` warn.
- **Indicator:** a vertical column of 5px dots at the pane's right edge, the current one in near-white.

## Do's and Don'ts

### Do:
- **Do** carry structure on hairline rules: `border-top:1px solid var(--rule)` for a band or entry, `--rule-lit` where the division must be felt.
- **Do** use the rule's own form to state provenance — solid for observed, dashed lit-rule for reckoned, doubled (border plus `inset 0 3px 0 -2px`) for a stop entry.
- **Do** pin `font-variation-settings:'opsz'` on every Bodoni numeral (22 at hero size, 16 elsewhere).
- **Do** condense every label to `font-stretch:75%` at 11px/600 uppercase, and extend every standby numeral to 110%.
- **Do** size the standby display in `cqb`/`cqi` against its own `container-type:size` pane.
- **Do** give any readout that overlays the live field a zero-offset halo in the ground colour.
- **Do** use `--brass-lit` for any brass that must be read as text or as a focus ring.
- **Do** keep every numeral `tabular-nums`, except the odometer drum where the strip sizes itself.

### Don't:
- **Don't** put a value in a card, panel, tile or filled box; a band and a rule is the container.
- **Don't** give a panel, control, field or band a corner radius — the circle is reserved for state marks.
- **Don't** use a shadow to imply elevation. Halos are legibility scrims at zero offset; nothing floats.
- **Don't** use `--brass` as a text colour; it does not clear 4.5:1 on the ground.
- **Don't** colour ordinary text. Hue belongs to rules, fills and marks.
- **Don't** set a standby numeral in Bodoni Moda, or an in-hand numeral in Archivo.
- **Don't** size the standby display in viewport units — they collapse to their clamp floors in the rotated branch.
- **Don't** add glass, blur, a gradient used as a surface fill, rope or parchment; the only image in the system is the data-driven velocity field. (A gradient may fade a hairline out at its ends, as the standby pane divider does.)
- **Don't** state a stop as an alert. A stop is a log entry with a doubled rule.
