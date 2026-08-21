# WALT HEALTH — public portal

Live: https://dylanwalt.github.io/walt-health/

Front-facing brand portal for the personal health OS.
Also hosts the WHOOP OAuth callback when `?code=` is present (same URL — do not change redirect URI).

## Brand

- Ice blue mark: `#95C8E2`
- Charcoal ground: `#0B0B0C`
- Wordmark: white
- Assets in `assets/`

## App views (password gate)

| View | Contents |
|------|----------|
| Overview | Plan status snapshot |
| History | Reserved (no wearable feed) |
| You | Goals, efficiency budget, gym, nutrition, timeline |
| This week / Today | Plan status + guided session |

Dashboard payload lives in `data/dashboard.json` (InBody kept; wearable series removed).

## Google Calendar

Subscribe to the plan feed (free, no Google API):

1. Open [Google Calendar](https://calendar.google.com) → Other calendars → **From URL**
2. Paste: `https://dylanwalt.github.io/walt-health/data/workouts.ics`
3. Default event time: **17:00–18:25 SAST** at Virgin Active Morningside (change in `plan.calendar` and regenerate the `.ics`)

Or download `data/workouts.ics` and import once (URL subscribe stays in sync when the feed is republished).
