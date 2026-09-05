---
version: 1
slug: "public-index-html"
primary_target: "public/index.html"
related_targets: []
---

Scope: `public/index.html` — the whole app: in-hand page and mounted standby display.
Visitor mode: Operate.

Audience and job: one traveller, two reading distances. Mounted in a vehicle it is a
fraction-of-a-second glance; in hand at a stop it is read properly. Mixed trip kinds,
so no readout permanently leads. Constraints: single file, no build, static on Workers;
tracking maths, tunables, localStorage shape and every existing readout are frozen.
Apple StandBy is a user-pinned reference for the standby display's finish.

Unresolved: none blocking.

## Direction contract

THESIS: A watch-keeper's record of a passage. The log's discipline is stating distance
run honestly across stretches nobody observed — which is what gap reconstruction already
does. Refuses the near-black-plus-neon-gauge dashboard the category ships.

OWN-WORLD: Night-watch ground (deep ink #0b1a24), log paper as the ink (#f4ede0), oxide
brass accent (#c8500f), sea grey (#7d9aa8). Ruled ledger bands, not cards: hairline rules
own the structure, a doubled rule marks a stop, a hairline-dashed rule marks reckoned
rather than observed. Bodoni Moda for engraved numerals, Archivo (variable width) small
caps for ledger headings. No rounded panels, no glass, no rope or parchment.

STORY: The traveller reads the current watch at a glance, and at a stop reads what the
stop cost — stated as a log entry, not an alert.

FIRST VIEWPORT: Masthead rule with watch state and fix accuracy. Below it the current
watch: engraved speed numeral at 118px+ centred, moving/trip/max averages as tracked
marginal entries. Then ruled log bands — distance run, under way, stopped, reconstructed.
Primary action sits in the engraved control band at the foot.

SIGNATURE INTERACTION: The WebGL field is re-skinned from streaks to the log's own ruled
paper streaming under a pen — rule density and ink weight driven by real speed, brass at
a brief stop, oxide when stopped.

FORM: The Deck Log; candidate 7 of 7 on my ordered list; seed key d21aefc9.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
