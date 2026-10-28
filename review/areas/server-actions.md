# Server Actions

<!-- Owners and paths: the [server-actions] section of review/OWNERS. Owners: replace the TODOs. -->

## Context

- Server Functions end to end: SWC transform that extracts actions, the action manifest, the action request handler (ID lookup, bound args, origin checks, encryption), and the client call path.
- TODO: key files and the invariants that must hold

## What failure looks like

- Actions resolve to the wrong function after a deploy, bound-argument encryption keys rotate and break in-flight forms, origin checks regress (security), closures leak server values, action IDs collide between layers.
- TODO: past regressions and reverts, with links

## Escalate when

- Any change to action ID generation, `encryption.ts`, origin/CSRF checks, or the `server_actions.rs` output shape (strong); new `next-action` header handling (strong, security).
- TODO

## Rules

- TODO

## Preferences

- TODO
