# Architecture Context

## Stack

| Layer | Technology | Role |
| --- | --- | --- |
| Framework | Next.js 16.4 App Router, React 19.3, TypeScript | Routes, layouts, and server/client rendering |
| Styling | Tailwind CSS v4 via the existing Turbopack loader | Utility classes and CSS variable tokens |
| UI | shadcn/ui, Radix Nova preset, Radix primitives | Reusable accessible UI components |
| Icons | lucide-react | SVG icons inside React components |
| Class merging | Official shadcn `cn` package | Conditional classes and Tailwind conflict resolution |

## System Boundaries

- `app/` owns routes, the root layout, and global theme styles.
- `components/ui/` contains the seven CLI-generated shadcn components. Preserve generated source after installation; compose components and pass props or `className` in application code.
- `lib/utils.ts` exposes the reusable `cn()` helper for application code.
- `components.json` owns shadcn generation settings and import aliases.
- `context/feature-specs/` defines implementation scope; `context/progress-tracker.md` tracks delivery and verification.

## Storage Model

- This feature does not introduce persistence. Storage requirements remain unspecified.

## Auth and Access Model

- This feature does not introduce authentication or authorization. Requirements remain unspecified.

## Invariants

1. Follow `context/feature-specs/01-design-system.md`; do not add unspecified product behavior.
2. Do not manually modify generated `components/ui/` source after installation.
3. Keep Tailwind CSS v4 and the existing Turbopack integration.
4. Retain the centered Ghost AI home page and favicon from the boilerplate cleanup.
5. Verify `npm run build` before moving to another feature unit.
