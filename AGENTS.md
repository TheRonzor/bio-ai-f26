# Agent Guide

This file is the root operating guide for AI agents working in this project. It should help agents preserve project memory, make focused use of documentation, and keep decisions visible as the work evolves.

## Start Here

- Read this file first.
- Read `PROJECT.md` early in each new task when it exists. Treat it as the canonical project memory: goals, current status, active work, important decisions, risks, and likely next steps.
- If `PROJECT.md` does not exist and the project has durable goals or ongoing work, create it when useful rather than scattering status across chat history.
- Project-specific docs and user instructions override these generic defaults.

## Read Only What You Need

Do not preload every documentation file before the task is clear. Start with `AGENTS.md` and `PROJECT.md`, then open only the focused docs relevant to the current work.

Create documentation by purpose, theme, or workflow instead of maintaining one large catch-all file. Useful examples include:

- `docs/research-notes.md` for sources, evidence, open questions, and literature-review context.
- `docs/design-system.md` for layout, components, typography, interaction patterns, or visual conventions.
- `docs/content-guidelines.md` for voice, terminology, audience, curriculum, or publication rules.
- `docs/art-direction.md` for visual style, references, palette, composition, and asset-generation guidance.
- `docs/testing.md` for verification commands, acceptance checks, fixtures, and known limitations.
- `docs/workflows.md` for repeated processes, handoff steps, release habits, or collaboration norms.

Add new focused docs only when they will reduce repeated explanation or preserve decisions that matter later.

## Keep Docs In Sync

Keep project documentation current as decisions are made. When a task changes goals, status, conventions, workflows, assumptions, architecture, research conclusions, creative direction, or future-development guidance, update the relevant doc in the same change.

Use `PROJECT.md` for high-level project memory:

- Current goal and scope.
- Recent progress and active work.
- Important decisions and why they were made.
- Known risks, blockers, and unresolved questions.
- Next steps that a future agent or collaborator should see immediately.

Use focused `docs/` files for durable details that are too specific for `PROJECT.md`.

If the user explicitly says the task is exploratory, temporary, or should not update documentation, respect that instruction and mention any documentation drift in the handoff.

## Working Conventions

- Git is exclusively user-managed. Agents must not run Git commands or use other tools to inspect or change Git state, including status, diffs, staging, commits, branches, tags, remotes, pulls, pushes, merges, rebases, stashes, worktrees, hooks, or repository configuration.
- Preserve existing project conventions before introducing new ones.
- Prefer the smallest change that fully satisfies the task.
- Avoid unrelated rewrites, reorganization, or style churn.
- When a new convention emerges, document it in `PROJECT.md` or the relevant focused doc.
- Keep generated or edited artifacts portable unless the project explicitly requires a specific platform, framework, or toolchain.
- For code and web work, use the project stack already in place before adding dependencies or build tooling.
- For research, analysis, course materials, documents, and creative work, keep sources, assumptions, audience, and acceptance criteria visible.
- For artwork or visual assets, document reusable style direction, references, constraints, and output requirements when they become part of the project.

## Verification

Verify work in a way that matches the medium and the project risk:

- Code: run relevant tests, builds, linters, type checks, or targeted smoke tests.
- Web or UI: check layout, interactions, responsiveness, console errors, and visual regressions where practical.
- Research or literature work: check citations, source quality, dates, quotations, and unresolved claims.
- Documents or course materials: review rendered output, structure, formatting, accessibility, and audience fit.
- Artwork or generated media: inspect the final asset against prompt, style, dimensions, legibility, and usage constraints.

If full verification is not practical, do the highest-value check available and clearly state what was not verified.

## Handoff

At the end of a task, summarize:

- What changed.
- What was verified.
- What remains uncertain or intentionally out of scope.
- Which docs were created or updated, or why documentation was not changed.

Keep handoffs concise, but include enough context that the next agent can continue without relying on hidden chat history.
