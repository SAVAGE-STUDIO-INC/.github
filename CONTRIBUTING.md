# Contributing — the house law

This is a small house with sharp standards. Every repo in the org follows
the same law; a repo's own `CLAUDE.md`/README refines it, never relaxes it.

## The gates

Nothing ships red. Before any push:

```
pnpm typecheck && pnpm lint && pnpm build
```

All three green, every time. If a gate fails, fixing it comes before
anything else — broken steps never stack.

## The way

- **pnpm only.** No npm, no yarn.
- **TypeScript strict.** No `any` escape hatches, no `@ts-ignore` drive-bys.
- **Branch → PR → merge.** No direct pushes to `main`.
- **Design consumes brand tokens.** No ad-hoc colors or type. Gold is foil,
  never paint. The marks are never redrawn.
- **Faces stay thin.** Public sites read; writes go through the MACHINE's
  public contract. Auth lives in the MACHINE only.
- **One database, additive-only.** Schema is owned in one place; migrations
  never drop or rename what exists.
- **No secrets on disk or in code.** Credentials live in the vault; env
  resolves at run time.

## Commits

Conventional commits (`feat:`, `fix:`, `docs:`, `chore:`), scoped and
specific. Say what shipped, not what you did.
