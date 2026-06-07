# VISCERA STUDIO Portfolio

This project is a high-impact, editorial-style digital portfolio built with Next.js 16 and Tailwind CSS 4. It focuses on a brutalist aesthetic with high-contrast typography and fluid, scroll-based animations.

## Project Overview

- **Framework:** Next.js 16 (App Router)
- **Styling:** Tailwind CSS 4 (PostCSS)
- **Typography:** Syne (Headers), Inter (Body)
- **Animations:** Custom Vanilla JS (Intersection Observer & Scroll Listeners)
- **UI Components:** Radix UI / Shadcn UI (Installed but currently unused on the landing page)

## Architecture

- **`app/`**: Contains the main page and layout.
  - `page.tsx`: The primary entry point. It is a client-side component handling all animations and layout sections.
  - `globals.css`: Contains design tokens (OKLCH), Tailwind 4 configurations, and custom global styles (e.g., `.huge-type`).
- **`components/ui/`**: A comprehensive suite of reusable UI components based on Shadcn UI.
- **`hooks/`**: Custom React hooks like `use-mobile` for responsive behavior and `use-toast` for notifications.
- **`lib/utils.ts`**: Contains the `cn` helper for dynamic Tailwind class merging.

## Development Conventions

### Styling
- Use **Tailwind CSS 4** for most styling needs.
- Global design tokens are defined as CSS variables in `app/globals.css`.
- High-impact typography should use the `.huge-type` utility class.
- Prefer **Vanilla CSS** for complex grid compositions and specialized effects (like the cursor blob).

### Animations
- Animations are currently managed in the `useEffect` hook within `app/page.tsx`.
- Key techniques used: `IntersectionObserver` for reveals, `window.scroll` listeners for parallax, and mouse event listeners for the background "blob."
- When adding new animations, maintain the high-performance "will-change" optimization for transformed elements.

### Components
- While the landing page currently uses raw HTML for an "editorial" feel, new features should leverage the components in `components/ui/` to maintain consistency.

## Building and Running

- **Development:** `npm run dev`
- **Build:** `npm run build`
- **Linting:** `npm run lint`
- **Start:** `npm run start`

## Assets
- Images are currently sourced from Unsplash via direct URLs.
- Icons are powered by `lucide-react`.
- Static icons and manifest files are located in `public/`.
