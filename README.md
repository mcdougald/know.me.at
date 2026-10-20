<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="know.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">know.me.at</h1>

<p align="center"><strong>A team wiki you can take with you.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/self--host-supported-525252?style=flat-square" alt="Self-host: supported">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

Many wikis keep your writing in a format only they can read, so leaving means a lossy export and a lost history. I built know.me.at as a team wiki for small teams where pages are saved as plain markdown: leaving is a copy of your files, with every page's history as git commits. Permissions are checked inside the database query, so a page you cannot read is never loaded at all. It is spaces, collections and pages done completely, without the weight of a blocks platform: no realtime co-editing, no whiteboards.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="know.me.at at a glance: markdown is the document, links that build a map, no lost edits, leave with everything" width="880">
  </picture>
</p>

## Why know.me.at

| The usual team wiki | know.me.at |
| --- | --- |
| Content stored in a private block format | Plain markdown is what gets saved |
| Export is a conversion | Markdown files or a git bundle, with page history as commits |
| The last save wins | A conflicting save opens a three-way merge with your text still in it |
| Pages filtered after they are loaded | Permissions applied inside the query, and search follows the same rules |

## Features

- **Markdown is what gets saved**: pages are stored and rendered from markdown, and nothing is converted when you export.
- **Wiki-links and backlinks**: `[[links]]` between pages resolve by name and build backlinks, so a space gets its shape from what people write.
- **Revisions you can diff**: each page keeps its history under a retention policy, with a diff between versions.
- **Conflicting saves open a merge view**: each save carries the revision it started from, and if someone saved first, you get a three-way merge with your text still in it.
- **Permissions per collection**: read and write access applied inside the query, and search follows the same rules.
- **Take it with you**: export as an archive of markdown files or as a git bundle with page history as commits, attachments included.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How know.me.at works: write, save, link, find, export" width="880">
  </picture>
</p>

You write a page in markdown, and each save is checked against the revision you started from, so a conflict becomes a merge instead of a lost edit. The `[[links]]` you write build the backlinks between pages, and Postgres full-text search finds pages under the same permissions as reading them. Because the stored markdown is the document, an export hands back exactly what was saved.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
  <img src="https://img.shields.io/badge/Markdown-remark-737373?style=flat-square&logo=markdown&logoColor=white" alt="Markdown with remark">
  <img src="https://img.shields.io/badge/Mermaid-diagrams-737373?style=flat-square&logo=mermaid&logoColor=white" alt="Mermaid diagrams">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- Drizzle ORM + Postgres (with Postgres full-text search)
- Better Auth (the shared me.at account)
- unified / remark markdown pipeline, Mermaid diagrams, DOMPurify

## Part of the me.at family

know.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
