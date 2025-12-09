# Ocean Notes – Simple Notes App (Astro)

This is a simple notes UI built with Astro following the Ocean Professional theme.

Features:
- View a list of notes with title, preview, and last-updated timestamp
- Create, edit, and delete notes using a modern modal
- Local persistence via `localStorage`
- Optional REST API support if `PUBLIC_API_BASE` or `PUBLIC_BACKEND_URL` is set (uses `/notes` CRUD)

Environment (no new env vars introduced):
- PUBLIC_API_BASE (optional)
- PUBLIC_BACKEND_URL (optional)
- PUBLIC_LOG_LEVEL (optional)
- Other PUBLIC_* variables are ignored by this app.

Behavior:
- If an API base URL is provided and reachable, requests go to:
  - GET    {API_BASE}/notes
  - POST   {API_BASE}/notes
  - PUT    {API_BASE}/notes/:id
  - DELETE {API_BASE}/notes/:id
- If the API fails or is not configured, the app gracefully falls back to localStorage.

Run:
- npm install
- npm run dev (served on port 3000 per astro.config.mjs)
- npm run build && npm run preview

Notes:
- Title is required for create/update.
- The design uses blue (#2563EB) and amber (#F59E0B) accents, white surfaces, subtle shadows, and rounded corners.
