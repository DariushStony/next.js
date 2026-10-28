# Build Output and Manifests

<!-- Owners and paths: the [build-output-and-manifests] section of review/OWNERS. Owners: replace the TODOs. -->

## Context

- `next build` orchestration and what it writes: all `*-manifest.json` files, `prerender-manifest`, routes manifest, standalone output + NFT traces, `output: 'export'`, the adapter API, build-id and deployment-id handling.
- TODO: key files and the invariants that must hold

## What failure looks like

- A manifest field renamed or reordered breaks the Vercel builder or self-hosters' adapters; standalone output missing a traced file (500 at runtime); export writing HTML for a dynamic route; non-deterministic builds; build-id changes causing skew.
- TODO: past regressions and reverts, with links

## Escalate when

- Any change to a manifest's shape or file name, to NFT trace inclusion, or to standalone/export directory layout (strong: these are public build output); changes to `prerender-manifest` classification (medium, shared with app-prerender).
- TODO

## Rules

- TODO

## Preferences

- TODO
