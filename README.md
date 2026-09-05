# Trip pace

Single-file GPS trip tracker (`public/index.html`): live speed, distance-per-minute/hour, route-based remaining distance + ETA, stop detection, suspended-gap reconstruction, iOS-StandBy-style landscape display.

## Deploy on Cloudflare (Workers static assets)

Cloudflare recommends Workers with static assets over Pages for new projects. This repo is already configured.

**Automatic deploys (recommended):** Cloudflare dashboard → Workers & Pages → Create → Import a repository → pick this repo.
Build command: leave empty. Deploy command: `npx wrangler deploy`. Every push to `main` redeploys.

**Manual:** `npm install && npx wrangler login && npm run deploy`

**Local:** `npm run dev` (serves on localhost, which counts as a secure context so GPS works).

## Use on phone
Open the `*.workers.dev` URL in Safari/Chrome → Share → Add to Home Screen. Allow location. HTTPS is required for GPS.
