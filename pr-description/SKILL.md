---
name: pr-description
description: Write a pull-request description from the actual diff — what changed, why, risk, and how it was verified. Use when opening or updating a PR.
---

# PR Description

A PR description is for two readers: the reviewer today and the engineer git-blaming this change during
an incident in two years. Serve both from the actual diff, never from memory of what you intended.

## Phase 1 — Read the real diff

1. `git diff <base>...HEAD --stat` then the full diff. The description covers what the diff contains —
   including the drive-by changes you forgot you made. If you find unrelated changes, flag them for
   splitting rather than burying them in prose.
2. Identify: behavior changes (user-visible), interface changes (API/schema/config — call these out
   loudly), and pure internals.

## Phase 2 — Write it

Structure (adapt to the repo's PR template if one exists — check `.github/`):

- **What & why** (2–4 sentences): the problem, and why this approach. Link the issue/ticket.
- **Changes**: grouped bullets by area, not per-file. Interface/breaking changes get their own labeled
  bullet at the top with migration notes.
- **Risk & rollout**: what could break, blast radius, feature-flag/rollback story, migration ordering
  (deploy before/after migrate?).
- **How verified**: the actual commands/tests run and their results — "tests pass" only if you ran them
  in this state. Screenshots for UI, query counts for perf claims, repro-then-fix for bug fixes.

## Rules

- Nothing in the description that the diff contradicts — reviewers lose trust instantly and permanently.
- If you can't fill "How verified" honestly, that's not a writing problem; go verify, then write.
- Keep it under ~300 words unless the change genuinely warrants more. Long is not thorough.

---

*From the free tier of **The Production Pack** — 10 senior-engineer skills for Claude Code: https://winterjoy1.gumroad.com/l/qnrbr*
