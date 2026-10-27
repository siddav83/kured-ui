# Kured UI

An independent Astro component library inspired by the visual language of Kured Food. This contains **generic reusable components**, not the Kured website, business content, analytics, or credentials.

## Components

- `Button`: an accessible native link or button with primary/secondary visual styles
- `Container`: centred max-width layout
- `Tag`: labelled colour accent
- `SectionHeading`: an h1/h2/h3 section title with optional eyebrow
- `ProjectCard`: project summary linking to details

## Usage (once installed in an Astro project)

```astro
---
import '@siddav83/kured-ui/styles.css';
import Button from '@siddav83/kured-ui/components/Button.astro';
---
<Button href="/projects" variant="primary">View projects</Button>
```

The package uses CSS variables defined in `styles.css`; fonts must be loaded by the consuming site. Its `exports` map permits imports from `/components/*.astro`.

## Release plan

1. Review the pull request and test the components in a consuming Astro app.
2. Run `npm pack --dry-run` to inspect packaged files.
3. Confirm ownership of the `@siddav83` npm scope.
4. Publish the first public version to the npm registry **only after explicit approval**.
5. Install a pinned version in the portfolio and build/test it.

`0.1.0` is a draft version, not a published release. No tokens or secrets belong in this repository.

## Licence

No licence has been granted yet (`UNLICENSED` in package.json). We will decide on a public licence before encouraging third-party reuse.
