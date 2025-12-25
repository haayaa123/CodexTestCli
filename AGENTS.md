# Repository Guidelines

## Project Structure & Module Organization
- `src/main.js` bootstraps the Vue app and mounts `App.vue`.
- `src/App.vue` is the root component; reusable components live in `src/components/`.
- `src/style.css` holds global styles; component-scoped styles live inside `.vue` files.
- `src/assets/` contains bundled assets; `public/` contains static files served as-is.
- `index.html` is the Vite entry template used during build and dev.

## Build, Test, and Development Commands
- `npm install` installs dependencies.
- `npm run dev` starts the Vite dev server with HMR.
- `npm run build` produces the production bundle in `dist/`.
- `npm run preview` serves the production build locally for verification.

## Coding Style & Naming Conventions
- Use Vue 3 Single File Components with `<script setup>`.
- Indentation is 2 spaces in `.vue`, `.js`, and `.css` files (match existing files).
- Use single quotes in JavaScript imports and strings where possible.
- Component files use PascalCase (e.g., `HelloWorld.vue`); CSS classes use kebab-case.

## Testing Guidelines
- No automated test framework is configured yet.
- If you add tests, document the chosen runner and add a script in `package.json` (for example, `test`).
- Name tests clearly (for example, `*.spec.js`) and keep them near the components they cover or under a `tests/` folder.

## Commit & Pull Request Guidelines
- Current history uses Conventional Commits (example: `chore: init vue vite app`). Follow that style.
- PRs should include a concise summary, testing steps, and screenshots for UI changes.
- Link related issues and call out any config or dependency changes.

## Configuration Notes
- Vite reads environment variables prefixed with `VITE_` (for example, `VITE_API_URL`).
- Keep secrets out of the repo; document required env vars in the PR or README.
