# Architecture

## Goal

This repository is evolving from a simple Codex experiment into a scalable multi-project workspace.

## Planned Structure

```text
/apps
  /snake-game
  /movies-test

/packages
  /shared

/docs
```

## Design Principles

- Separate each experimental application into isolated workspaces.
- Keep reusable logic inside `/packages/shared`.
- Store engineering and workflow documentation inside `/docs`.
- Reduce branch chaos by using consistent naming conventions.

## Branch Strategy

- `main` → stable trunk
- `topic/*` → experiments and prototypes
- `feature/*` → production-oriented features
- `fix/*` → bug fixes

## Future Direction

Potential future apps:

- AI dashboard
- Chat application
- Image generation tools
- Automation agents
- GitHub workflow tools
