---
name: readme-refresh
description: Bring a README (or docs page) back in sync with what the code actually does — verify every claim, fix drift, fill gaps. Use when docs are stale, before a release, or after a feature lands.
---

# README Refresh

Docs drift is a trust problem: one wrong install command and readers stop believing the rest. This
workflow treats every statement in the README as a claim to verify against the code.

## Phase 1 — Verify every existing claim

1. Read the README and extract its checkable claims: install commands, quickstart snippets, CLI flags,
   config options, supported versions, API examples, badges.
2. Verify each against reality:
   - Run the install/quickstart commands in a clean context if feasible; otherwise trace them against
     the current manifest/lockfile and entry points.
   - Diff documented flags/options against the actual CLI parser and config schema.
   - Execute code examples; paste back the REAL output, not remembered output.
3. Mark each claim: accurate / drifted (fix) / removed feature (delete section).

## Phase 2 — Fill the gaps that matter

Check for the sections readers actually need, add only what's true:
- What it does in 2 sentences (the "why should I care" test — no jargon before the first period).
- Working quickstart: install, minimal run, what success looks like.
- Requirements (runtime versions, OS caveats) — from the manifests, not memory.
- Where to get help / contribute, if such channels exist. Don't invent community that isn't there.

## Phase 3 — Keep it honest

- Never document aspiration as fact ("blazingly fast", "production-ready") — cut adjectives, keep facts.
- Keep the README's existing voice and structure; this is a refresh, not a rewrite.
- End with a summary: claims verified, drift fixed (list), sections added/removed.

---

*From the free tier of **The Production Pack** — 10 senior-engineer skills for Claude Code: https://winterjoy1.gumroad.com/l/qnrbr*
