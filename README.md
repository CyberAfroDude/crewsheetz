# CrewSheetz

Static CrewSheetz prototype ready for deployment on Vercel and version control on GitHub.

## Local Preview

Run a local server from the project root:

```bash
python3 -m http.server 4173
```

Then open:

- `http://127.0.0.1:4173/`

## Deploy to Vercel

### Option 1: From GitHub (recommended)

1. Push this repository to GitHub.
2. In Vercel, click **Add New Project** and import the GitHub repository.
3. Framework preset: **Other** (static site).
4. Build command: leave empty.
5. Output directory: leave empty (root).
6. Deploy.

## Supabase Setup

1. Create a new Supabase project.
2. In Supabase SQL Editor, run `supabase/schema.sql`.
3. Open `supabase-config.js` and set:
   - `url` to your project URL
   - `anonKey` to your public anon key
4. Redeploy on Vercel.

The app keeps working without Supabase configured (local state fallback).
When configured, app state syncs to `public.app_state` row `id = 1`.

### Option 2: Vercel CLI

```bash
npm i -g vercel
vercel
vercel --prod
```

## Project Files

- `index.html` - root entrypoint
- `crewsheetz-v4.html` - full UI implementation
- `vercel.json` - Vercel runtime configuration
- `supabase-config.js` - frontend Supabase credentials config
- `supabase/schema.sql` - table + policy setup
