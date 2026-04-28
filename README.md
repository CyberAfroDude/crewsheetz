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
