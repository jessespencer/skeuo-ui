# Uber Dark UI Kit

## Project Overview
Neumorphic component library showcasing iOS-inspired dark/light UI design. Single-page demo app — all components rendered in `src/App.tsx`.

## Tech Stack
- React 19 + TypeScript (strict) + Vite 7 + Tailwind CSS 4
- No state management library — React Context for theming only
- Deployed to GitHub Pages at `/uber-ui/` base path

## Project Structure
- `src/components/` — All UI components (Button, Switch, Dropdown, Slider, etc.)
- `src/components/icons.tsx` — Custom SVG icon set
- `src/components/theme-utils.ts` — Shared gradient stroke helper
- `src/context/ThemeContext.tsx` — Dark/light theme context with localStorage persistence
- `src/index.css` — CSS custom properties (design tokens), Tailwind config, theme overrides
- `src/App.tsx` — Demo page rendering all components
- `figma-variables-*.json` — Figma token exports for dark/light themes

## Key Patterns
- Components manage their own interactive states (hovered, pressed, focused) via hooks
- Theme switching applies `data-theme` attribute on `<html>` and uses a `no-transitions` class during swap
- Neumorphic styling via CSS custom properties for surface gradients, shadows, and accent colors
- Keyboard accessibility: components handle Enter/Space key events, use proper ARIA roles

## Development
```bash
npm run dev      # Dev server at localhost:5173/uber-ui/
npm run build    # TypeScript check + Vite build → dist/
npm run lint     # ESLint
```

## Deployment
GitHub Actions workflow (`.github/workflows/deploy.yml`) auto-deploys to GitHub Pages on push to `main`.
