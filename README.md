# Next.js Boilerplate

[![CI](https://github.com/ak1008yaa/nextjs-boilerplate/actions/workflows/ci.yml/badge.svg)](https://github.com/ak1008yaa/nextjs-boilerplate/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

A small, opinionated Next.js starter that is ready to ship: App Router,
strict TypeScript, Tailwind CSS 4, ESLint, a CI pipeline and automated
dependency updates.

## Stack

| Layer      | Choice                        |
| ---------- | ----------------------------- |
| Framework  | Next.js 16 (App Router)       |
| Runtime    | React 19                      |
| Language   | TypeScript 5                  |
| Styling    | Tailwind CSS 4                |
| Linting    | ESLint 9 + eslint-config-next |
| CI         | GitHub Actions                |
| Hosting    | Vercel                        |

## Requirements

- Node.js 22 LTS or newer
- npm 10 or newer

## Getting started

```bash
git clone https://github.com/ak1008yaa/nextjs-boilerplate.git
cd nextjs-boilerplate
npm install
cp .env.example .env.local
npm run dev
```

Open <http://localhost:3000>.

## Scripts

| Command             | Description                    |
| ------------------- | ------------------------------ |
| `npm run dev`       | Start the development server   |
| `npm run build`     | Create a production build      |
| `npm start`         | Serve the production build     |
| `npm run lint`      | Run ESLint                     |
| `npm run typecheck` | Type-check without emitting    |

## Project structure

```
app/                  App Router routes, layout and global styles
  layout.tsx          Root layout and metadata
  page.tsx            Home route
  globals.css         Tailwind entry point and theme tokens
public/               Static assets served from the site root
.github/workflows/    CI pipeline
```

## Environment variables

Copy `.env.example` to `.env.local` and adjust the values. Files ending in
`.env.local` are ignored by git and must never be committed.

Only variables prefixed with `NEXT_PUBLIC_` are exposed to the browser. Never
put a secret in one of them. Server-only secrets belong in the hosting
provider's environment settings.

## Continuous integration

Every push and pull request to `main` runs a single `quality` job that installs
dependencies, lints, type-checks and builds the project on Node.js 22. A red
check blocks the merge.

Dependabot opens grouped weekly pull requests for npm packages and GitHub
Actions, so upgrades arrive as small, reviewable changes.

## Deployment

The project deploys to Vercel with zero configuration. Push to `main`, or
connect the repository in the Vercel dashboard and keep the default build
settings (`npm run build`, output `.next`).

## License

MIT © ATLAS-DEV. See [LICENSE](./LICENSE).

---

powered by [ATLAS-DEV](https://www.atlas-dev.pro)
