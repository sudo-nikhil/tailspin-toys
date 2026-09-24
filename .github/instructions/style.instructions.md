---
description: 'Tailwind CSS v4 styling patterns and dark theme guidelines'
applyTo: '**/*.{astro,css}'
---

# Tailwind CSS Instructions

## Tailwind CSS v4 Configuration

This project uses Tailwind CSS v4.1.14 via the `@tailwindcss/vite` plugin.

### Global CSS Setup

- Import Tailwind in `global.css`: `@import "tailwindcss";`
- No separate `tailwind.config.js` file is used
- Configuration is handled through the Vite plugin

## Dark Theme Styling

ALL UI components MUST use dark theme colors:

### Color Palette

- Background colors: `bg-slate-800`, `bg-slate-900`, `bg-slate-950`
- Text colors: `text-slate-100`, `text-slate-200`, `text-slate-300`
- Border colors: `border-slate-700`, `border-slate-600`
- Accent colors for hover/focus states

### Common Patterns

- Cards and containers: `bg-slate-800 rounded-xl p-6 shadow-lg`
- Hover effects: `hover:bg-slate-700 transition-colors duration-200`
- Borders: `border border-slate-700`
- Gradients for visual interest: `bg-gradient-to-br from-slate-800 to-slate-900`
- Backdrop effects: `backdrop-blur-sm bg-slate-900/50`

### Responsive Design

- Use responsive prefixes: `sm:`, `md:`, `lg:`, `xl:`
- Mobile-first approach
- Ensure readability on all screen sizes

## Utility Classes

- Prefer utility classes over custom CSS when possible
- Use semantic grouping: layout, spacing, colors, typography
- Keep utility combinations readable and maintainable

## TypeScript and Commenting Conventions

- Prefer explicit TypeScript types for function parameters and returns, especially in `db/` and `src/lib/`.
- Model component props with named interfaces and keep them near the implementation they describe.
- Favor small, expressive helper functions over large untyped blocks of logic.
- Comments should explain intent, constraints, or domain reasoning; avoid comments that simply describe code mechanics or repeat nearby names.
- Treat outdated comments as bugs to fix in the same patch that changes the code.
- ESLint enforces the repo's baseline TypeScript quality rules (`@typescript-eslint` recommended rules and no-unused-vars with `_` exemptions), so keep code free of obvious lint issues as part of the same change.

## Modern UI Patterns

- Rounded corners: `rounded-lg`, `rounded-xl`, `rounded-2xl`
- Smooth transitions: `transition-all duration-200 ease-in-out`
- Shadows for depth: `shadow-md`, `shadow-lg`, `shadow-xl`
- Focus states for accessibility: `focus:ring-2 focus:ring-blue-500`
