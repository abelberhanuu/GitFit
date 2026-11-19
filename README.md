# GitFit

A Next.js/TypeScript AI fitness-planning application using the Google provider from the Vercel AI SDK.

## What the repository contains

- A guided interface collecting user details and fitness goals.
- An API route that sends a prompt to a Gemini model and returns generated text.
- Workout and diet-plan rendering.
- Browser-side PDF export using jsPDF.
- Reusable interface components and Tailwind styling.

**Outcome:** a prototype workflow connecting a form, an AI generation endpoint, and downloadable plan documents.

## Run locally

```bash
git clone https://github.com/abelberhanuu/GitFit.git
cd GitFit
npm ci
```

Configure credentials for the installed `@ai-sdk/google` provider in a local environment file. Do not commit credentials. Review [app/api/gemini/route.ts](app/api/gemini/route.ts): the checked-in route requests `models/gemini-2.0-flash-exp`. Confirm model access and configure an available model before relying on a live demo.

```bash
npm run dev
```

Open the URL printed by Next.js.

## Source map

| Path | Responsibility |
| --- | --- |
| [app/Components/Homepage/Homepage.tsx](app/Components/Homepage/Homepage.tsx) | Guided interface, generated text, and PDF export |
| [app/api/gemini/route.ts](app/api/gemini/route.ts) | AI generation endpoint |
| [app/Components/ui/](app/Components/ui/) | Interface components |
| [package.json](package.json) | Runtime dependencies and scripts |

## Current limits

The generation endpoint catches errors without returning a structured error response. Live AI generation and production builds have not been validated during this documentation update. Generated fitness text is prototype output and is not evaluated as clinical guidance.

## Attribution

The existing [MIT license](LICENSE) credits **Rahil (2025)**, and the interface contains a matching creator credit. Those credits are retained. This README describes the code present in this repository and does not establish original authorship or a specific personal contribution.
