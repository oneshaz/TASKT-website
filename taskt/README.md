# TASKT.

A single-page, dark retro-modern daily task board inspired by the visual language of Hacktoberfest 2026.

## Run locally

Install Node.js 18+ and then run:

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (normally http://localhost:5173).

## Production build

```bash
npm run build
npm run preview
```

## Deploy to Vercel

1. Upload this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Framework preset: **Vite**. Build command: `npm run build`. Output directory: `dist`.
4. Click **Deploy**. No environment variables, database, or server are needed.

## Daily progress rules

- All unfinished tasks carry forward automatically.
- Previously completed tasks remain in the Completed column but do not count toward today's progress.
- Tasks finished today count toward today's completion percentage.
- Reopened tasks become active again, and can be finished today.
- Progress = completed-today tasks / (unfinished tasks + completed-today tasks).
- Tasks persist only in the same browser via `localStorage`, not across devices.

## Project structure

- `index.html`: document shell and fonts
- `src/main.jsx`: React app and task logic
- `src/style.css`: visual design and responsive layout
- `vite.config.js`: Vite configuration
- `package.json`: scripts and dependencies
