# CLAUDE.md — Portfolio Engine

Permanent rules for Claude Code. Read fully before making any changes.

## PROJECT
Reusable portfolio website framework for architects in Bangladesh.
One engine, many clients. Client differences live in Firebase config, not code.

## TECH STACK (LOCKED)
- Next.js (App Router) — pin current stable
- TypeScript
- Tailwind CSS
- shadcn/ui
- Firebase (Auth, Firestore, Storage, App Hosting)
- Framer Motion (subtle only)
- Zod
- Vitest + Playwright

Do not add new major dependencies without asking.

## ARCHITECTURE PRINCIPLES

1. Config-First Rule
   Client-specific needs → configuration, not code.
   Never fork the engine per client.

2. Public Site = Server-Rendered
   Public pages must be server-rendered or statically rendered.
   Content in HTML for SEO and speed. NOT client-side Firebase for initial content.
   Admin panel may use client-side Firebase SDK.

3. No Feature Creep
   Product = 6 public sections + admin panel.
   No blog, newsletter, multi-language, e-commerce, booking, chatbot, AI, builder, analytics.

4. One Repo, One Engine
   All clients use same codebase. New clients get current version.
   Old clients stay on delivered version unless they pay for updates.

5. Ownership
   Client owns: Firebase project, domain, data, images, content.
   You own: Portfolio Engine source, skins, shared software.
   Client receives: perpetual licence to delivered version.

6. Deployment
   Firebase CLI local-source deployment. No GitHub connection to client Firebase.

7. Image Discipline
   All uploads compressed to 200-400 KB max.
   Multiple sizes generated: thumbnail, card, full.
   Critical for staying in Firebase free tier.

8. Soft-Delete
   Project deletion = soft (trash, recoverable 30 days).
   Never hard-delete user content directly.

## FOLDER STRUCTURE
portfolio-engine/
├── src/
│ ├── app/
│ │ ├── (site)/ # Public pages
│ │ ├── admin/ # Admin panel
│ │ └── api/ # API routes
│ ├── components/
│ ├── engine/
│ ├── skins/
│ │ ├── minimal/
│ │ └── editorial/
│ ├── config/
│ ├── lib/
│ └── types/
├── public/
├── CLAUDE.md
├── PROJECT-STATE.md
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── next.config.js
├── firebase.json
├── .firebaserc
└── README.md

## CONVENTIONS
- TypeScript strict mode
- Functional components + hooks
- Named exports preferred
- kebab-case files, PascalCase components
- Tailwind for all styling, no inline styles
- No `any` types
- Zod for external data validation

## DO NOT
- Add pages not in spec
- Add features client didn't request
- Introduce client-specific code
- Hardcode Firebase project IDs
- Commit secrets or API keys
- Use deprecated Next.js APIs
- Skip TypeScript types
- Deploy without testing locally

## WHEN IN DOUBT
Ask before acting. Small question > large wrong implementation.
Preserve existing architecture. Do not redesign.