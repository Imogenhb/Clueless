# Clueless – Outfit Selector

A Next.js 16 (App Router) personal outfit recommendation / digital closet app. All data is client-side (localStorage). No database.

## Cursor Cloud specific instructions

### Services

| Service | Command | Port |
|---------|---------|------|
| Next.js dev server | `npm run dev` | 3000 |

No additional services (databases, Docker, etc.) are required.

### Key commands

| Task | Command |
|------|---------|
| Install deps | `npm install` |
| Dev server | `npm run dev` |
| Lint | `npm run lint` (ESLint 9) |
| Build | `npm run build` |

### Caveats

- **Auth gate**: The app has an `AuthGate` component wrapping all page content. Without Supabase credentials (`NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY` in `.env.local`), the UI shows a login prompt on every route. API routes still respond normally.
- **No test framework**: The codebase has no automated tests (no Jest, Vitest, Playwright, or Cypress). Lint (`npm run lint`) and build (`npm run build`) are the available verification steps.
- **Pre-existing lint errors**: ESLint reports ~6 errors (mostly `react-hooks/set-state-in-effect`) and ~14 warnings. These are pre-existing and unrelated to any agent changes.
- **API fallbacks**: All external API keys are optional. Without them, API routes return graceful fallback responses (mock weather data, informative error messages).
- **Node version**: The project works with Node.js v22+. No `.nvmrc` or engine field is present.
