# Tripolgy — updated prototype (November 2026)

A no-build travel planner in HTML, CSS, and JavaScript.

## Important limitations before public launch
- Account data, passwords, trip records, approvals, and uploaded covers live in **localStorage in the current browser**. This is a functional single-browser prototype, **not secure production authentication**. Do not enter a real password. Multiple devices cannot share the same accounts/trips; copying an invite URL alone will not grant access to a trip.
- To launch for real users, add a hosted authentication/database/storage backend (for example, Supabase Auth, Postgres, and Storage) and enforce row-level security.
- The AI travel planner calls public endpoints directly from the browser. They may fail, change behavior, or throttle. When AI generation fails, the interface falls back to a clearly marked sample plan. The sample itinerary is not verified and should not be relied upon for bookings.
- Ratings/costs, when supplied by AI, are estimates, not confirmed data. Weather and map links use third-party services; live photo lookups require internet access.
- Do not expose production AI API keys in browser settings; use a server-side proxy before deployment.

## Provider credits
AI planning via Pollinations or optionally Gemini, forecast from Open-Meteo, place lookup via OpenStreetMap Nominatim, other-place imagery via Wikipedia, and the six provided destination images bundled locally.

DISCLAIMER: USED CHATGPT HELP TO CREATE TRIPOLGY
