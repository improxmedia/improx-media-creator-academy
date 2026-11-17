# IMPROX MEDIA Creator Academy

Internal learning portal for the IMPROX MEDIA team: English communication, storytelling, on-camera presence and video craft.

Single static page (`index.html`), no build step.

## Settings (top of the `<script>` in `index.html`)

| Setting | What it does |
|---|---|
| `REQUIRE_LOGIN` | `false` = opens straight to the dashboard. `true` = shows the pass code and key gate (demo only: checked in the browser, not secure). |
| `REPORT_URL` | Empty = member profiles and progress stay on the member's own device. Set to your own endpoint to receive profile and progress updates. |

## Member profile and location

On first visit a member enters their name and country (city optional) and ticks a consent box. An optional "Detect my approximate location" button looks up an approximate location from their IP via ipwho.is, only when pressed. Nothing is collected silently.

## Videos

Lessons embed official public YouTube videos with credit to the owners. To use your own or licensed footage instead, put the file in `videos/` and set `video:"videos/your-file.mp4"` on the lesson. A hosted file always takes priority over YouTube.

## Security note

This is a static site. Do not rely on the built-in pass code for privacy. For a real private portal, put it behind server-side login (for example Cloudflare Access) and issue and revoke IDs from a database.
