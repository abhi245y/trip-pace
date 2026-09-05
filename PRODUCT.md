# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

One person on a trip, with the phone in two different reading situations that
the product must serve at once:

- **Mounted, while moving.** In a windscreen or vent mount, read in glances of a
  fraction of a second. This is the standby display's scene.
- **In hand, at stops.** Held and read properly while parked or riding along.
  This is the main page's scene.

Trips are mixed in kind — intercity drives, commutes, touring — so no single
readout has been established as the one that always leads.

## Product Purpose

Track a trip in progress and answer, continuously, how the pace is actually
going: current speed, distance covered, how far is left, when you will arrive,
and what stopping has cost you. Success is that a glance answers the question
the traveller has right now without them working for it.

## Positioning

Two mechanisms a general navigation app does not offer:

- **Stops are accounted for, not averaged away.** Stops are detected and
  classified (brief vs. stopped), and the app states the delay a stop added to
  arrival, the distance you would have covered at your pre-stop speed, and how
  much the remaining time grew.
- **Suspended time is reconstructed rather than lost.** When the OS suspends the
  page, the gap between the last fix and the next is split into "driving at the
  previous moving average" and "stopped", so distance, times and averages stay
  honest across backgrounding.

Also distinct: distance-per-minute / per-30-minutes / per-hour at both current
speed and moving average, in km, m or cm.

## Operating Context

- Installed to the home screen as a PWA and used standalone; HTTPS required for
  geolocation.
- Screen wake lock held for the length of a trip; the phone is on power.
- Mobile data, often intermittent. Geocoding (Nominatim) and routing (OSRM) are
  keyless and may fail; the app must stay useful with no network.
- A trip survives reload and suspension via localStorage and is resumable.
- Landscape orientation, or the Standby button, enters a mounted glance display;
  portrait-forced entry rotates the display 90°.

## Capabilities and Constraints

- Single file, `public/index.html`, no build step. Served as static assets by
  Cloudflare Workers (`wrangler.jsonc`, `assets.directory = ./public`).
- Leaflet 1.9.4 from cdnjs for the route map; no other runtime dependency.
- Live speed with EMA smoothing, trip/moving/stopped timers, max speed,
  route-snapped progress with off-route detection, manual distance target as the
  fallback when no route is set, and an end-of-trip summary.
- Units switch between km, m and cm for the coverage readouts.
- **Frozen:** tracking mathematics, the tunables block, the localStorage key
  shape, and every existing readout. A redesign may change layout, colour,
  typography, hierarchy and the standby display; it may not remove a feature or
  alter what a number means.

## Brand Commitments

- Product name: **Trip pace**.
- The user has made Apple's StandBy mode a binding reference for the standby
  display's look and level of finish. Recorded as given, not expanded.

## Evidence on Hand

- Working implementation at `public/index.html`; `README.md` describes deploy
  and use.
- No brand assets, logo, typeface licences, photography, or copy beyond what is
  in the file. None are to be fabricated.
- Live GPS behaviour (tracking, stop detection, gap reconstruction) has never
  been verified in a moving vehicle in any session so far.

## Product Principles

1. **Two reading distances, one product.** Every surface belongs to either the
   mounted glance or the in-hand read, and is designed for that distance.
2. **The numbers are the product.** Readouts are the primary material; chrome
   exists only to organise them.
3. **Stay honest across gaps.** Suspension, lost signal and stops are stated
   plainly rather than smoothed into a wrong number.
4. **Useful with no network.** Search and routing are enhancements; tracking is
   not allowed to depend on them.
5. **One file, no build.** Additions must survive as static assets on Workers.

## Accessibility & Inclusion

- Pinch zoom must stay enabled; text needs accessible names and live regions for
  GPS and permission errors.
- The mounted glance scene sets a high bar for contrast and type size.
