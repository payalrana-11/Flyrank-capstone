# AI Content Visibility Dashboard

> A front-end capstone dashboard for tracking AI visibility, citations, and GEO/AEO analytics — modeled after real-world AI search monitoring products.

## About

This project is a **software engineering capstone** focused on AI content visibility: how brands and keywords appear across AI engines (ChatGPT, Perplexity, Claude, Google AI Overviews). Rather than a generic tutorial app, it mirrors the domain of products like **FlyRank** — citation tracking, visibility scoring, and trend analysis — so the work reads as genuinely relevant on a resume.

All data and AI responses are **simulated with mock data** (local JSON and MSW). There is no live backend or real third-party API integration in the core scope. That limitation is intentional and documented honestly below.

## Pages

| Page | Description |
|------|-------------|
| **Login** | Simple authentication (fake auth or optional Supabase) |
| **Dashboard** | Overall visibility score, citations this week, active tracked keywords/brands, weekly trend |
| **Tracked Items** | Searchable, filterable, sortable table with pagination — keyword/brand, AI engine, visibility score, trend, last checked, status/trend badges |
| **Item Detail** | Split layout: citation history & mention timeline (left), status, tags, and internal notes (right) |
| **Analytics** | Charts for citations per day, engine comparison, and ranking trend over time |
| **Settings** | App preferences and configuration |

## AI Features

These features are **UI demonstrations powered by mock data**, not live LLM or analytics API calls:

- **Citation trend summary** — AI-generated-style summary of how a tracked item is performing over time
- **Suggested next action** — Recommended follow-up based on score movement (e.g. refresh content, add citations)

Mock responses are designed to feel realistic for demos and portfolio review. They are not presented as production AI integrations.

## Tech Stack

| Layer | Technologies |
|-------|--------------|
| Framework | [Next.js](https://nextjs.org/) (App Router), [React](https://react.dev/) |
| Styling | [Tailwind CSS](https://tailwindcss.com/) |
| UI | [shadcn/ui](https://ui.shadcn.com/) — tables, badges, cards, and other accessible primitives |
| Charts | [Recharts](https://recharts.org/) |
| Data | Local JSON + [MSW](https://mswjs.io/) (Mock Service Worker) to simulate API responses |
| State | [Zustand](https://zustand-demo.pmnd.rs/) or React Context (filters, selected item) |
| Auth (optional) | [Supabase](https://supabase.com/) free tier — stretch goal, not core scope |
| IDE | [Cursor](https://cursor.com/) — primary AI-assisted development environment |
| Deployment | [Vercel](https://vercel.com/) |

## Prerequisites

- Node.js 18+
- npm, pnpm, or yarn

## Getting Started

```bash
git clone https://github.com/yourusername/AI-capstone.git
cd AI-capstone
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

If using optional Supabase auth, copy environment variables into `.env.local`:

```bash
cp .env.example .env.local
```

## Project Structure

```
├── app/              # Next.js App Router pages and layouts
├── components/       # Reusable UI (shadcn/ui + custom)
├── lib/              # Utilities, mock data helpers
├── mocks/            # MSW handlers and JSON fixtures
├── store/            # Zustand stores (or context providers)
└── public/           # Static assets
```

Structure will evolve as features are implemented.

## Mock Data & API Simulation

The app does not require a backend for the capstone scope. MSW intercepts fetch requests in development and serves realistic responses from local JSON fixtures — tracked items, citation history, analytics series, and simulated AI summaries.

This keeps the project deployable as a static/front-end app on Vercel while still demonstrating async data loading, loading states, and error handling patterns used in production apps.

## AI-Assisted Development

Built with **Cursor** as the primary AI pair-programming IDE (scaffolding, component generation, refactors, and documentation). AI tooling is used to accelerate development within free-tier constraints; architectural and product decisions remain human-directed.


