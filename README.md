# ScopeCraft Studio

ScopeCraft Studio is a polished React + TypeScript portfolio project for freelancers who want to show product thinking, not just UI implementation. It turns a raw client brief into a scope analysis with workstreams, delivery risk, timeline, recommended stack, acceptance criteria, discovery questions, and a copy-ready Markdown proposal.

![ScopeCraft Studio dashboard](screenshots/scopecraft-home.png)

## Why this project works in a portfolio

- Shows a real freelancer workflow: brief intake, scope shaping, risk management, saved projects, and proposal export.
- Demonstrates typed domain logic in `src/lib/analyzer.ts` instead of hard-coded UI placeholders.
- Includes responsive dashboard design, keyboard-friendly controls, and export actions.
- Makes a strong demo because every textarea change updates the analysis instantly.

## Features

- Live scope scoring for clarity, technical depth, delivery risk, and proposal readiness.
- Keyword-driven workstream detection for strategy, UI, auth, backend, payments, AI, analytics, and integrations.
- Risk register with mitigation advice.
- Delivery plan generated from the detected complexity.
- Markdown export for proposal handoff.
- Browser PDF export via the print dialog.
- Demo login state and local project saving.
- Three sample briefs plus a custom input mode.

## Tech stack

- React 19
- TypeScript
- Vite
- Lucide React
- CSS Grid and responsive CSS
- Local Storage for saved demo projects

## AI integration path

The current app uses a transparent local heuristic engine in `src/lib/analyzer.ts`. To turn it into a real AI-assisted tool, add a server route that calls the OpenAI API and returns the same `ScopeAnalysis` shape. Keep the API key on the server or in a serverless function, never in the browser bundle.

## Getting started

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Quality checks

```bash
npm run check
```

This runs ESLint and a production build.

## Deploy

Any static host works:

```bash
npm run build
```

Upload the generated `dist` folder to Netlify, Vercel, Cloudflare Pages, or GitHub Pages. For Vercel, import the GitHub repository, keep the default Vite settings, and set the build command to `npm run build`.

## Suggested GitHub description

> A client-brief analysis studio for freelancers: paste a rough brief and generate scope, risks, timeline, acceptance criteria, tech stack, and a Markdown proposal.

## Next portfolio upgrades

- Add a small test suite for the analysis engine.
- Replace the local heuristic analyzer with an OpenAI-powered serverless endpoint.
- Add Supabase or Neon for multi-device project persistence.
- Add before-and-after screenshots to this README after deploying.
