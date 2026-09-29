# DRAMORA V4 — Launch-ready web/PWA foundation

Connected to the DRAMORA Supabase project. Includes:
- Real published-series/episode loading
- Email/password sign-in and account creation
- Supabase-synced My List
- Supabase watch progress + resume
- Real licensed video URL playback
- Published-episode filtering
- Search and dynamic genres
- Mobile-first vertical player
- Guest mode and launch/empty state

## Important
Only publish titles/episodes for which DRAMORA has the required distribution rights. The app intentionally reads only `series.status = published` and `episodes.is_published = true`.

## Run
Serve this folder from a web server. Do not open `index.html` with `file://` because browser modules/auth/network policies can block requests.
