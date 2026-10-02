# AGENTS.md — ify-wled-controller

Worker router. Read BEFORE any code change.

## Invariants
- Work on a feature branch; never push `main`.
- TDD: failing test first (Vitest), then implementation.
- UI: consult the `ui-ux-pro-max` skill for design decisions; keep one design system.
- Device access ONLY via the vendored contract in `vendor/ify-device-contracts/` (see `CONTRACTS.md` after first sync). No raw fetches to device APIs outside the device gateway module (`src/devices/`).
- Loopback/LAN only: the app talks to devices on the local network; do not add cloud relays without an explicit decision.
- Verify: `npm run test` green + `npm run build` clean before requesting review. Report actual command output, never claimed.

## Sources of truth
- Scope/tasks: Hermes Kanban (assignee coder-web)
- Design system: `docs/design-system.md` (created during F1 design)
- Device contract: `vendor/ify-device-contracts/VERSION`
