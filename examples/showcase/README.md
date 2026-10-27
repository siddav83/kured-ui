# Kured UI — local component showcase

This is a small, **private-to-development** Astro example that renders the real components from `@siddav83/kured-ui`, not screenshots or rewritten lookalikes. It is not published as part of the library package.

## Run it locally

Prerequisites: Node.js 22 and npm (Astro 5 requires a supported Node version).

```sh
git clone https://github.com/siddav83/kured-ui.git
cd kured-ui
git switch feature/local-showcase
cd examples/showcase
npm install
npm run dev
```

Open **http://localhost:4321/** in your browser.

## Why the package connection works

The showcase's `package.json` contains:

```json
"@siddav83/kured-ui": "file:../.."
```

This tells npm to install the library directly from the repository's root directory on disk. The component imports deliberately use the same public paths as a future npm release:

```astro
---
import '@siddav83/kured-ui/styles.css';
import Button from '@siddav83/kured-ui/components/Button.astro';
---
<Button href="#projects">View projects</Button>
```

When the package is eventually published, the dependency can change to a version such as `"@siddav83/kured-ui": "0.1.0"` without rewriting component imports.

## Useful commands

- `npm run dev`: serve the gallery locally
- `npm run build`: test production compilation of the gallery
- `npm ls @siddav83/kured-ui`: show the installed local package
- `npm pack --dry-run` **from the repository root**: inspect the library's eventual publication contents

No deployment, npm publication, or GitHub release is required to use the showcase.
