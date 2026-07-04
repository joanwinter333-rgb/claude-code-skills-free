# Claude Code Skills — Free Tier

Two free, production-grade skills for [Claude Code](https://www.anthropic.com/claude-code). Copy them into
your project and Claude runs the workflow the way a senior engineer would — every time.

| Skill | What it does |
|---|---|
| [`readme-refresh`](readme-refresh/SKILL.md) | Bring a README back in sync with what the code actually does — verify every claim, fix drift, fill gaps |
| [`pr-description`](pr-description/SKILL.md) | Write a PR description from the *actual diff* — what changed, why, the risk, and how it was verified |

## Install (30 seconds)

```bash
# per-project (ships with your repo)
mkdir -p your-project/.claude/skills
cp -r readme-refresh pr-description your-project/.claude/skills/
```

Then open Claude Code and type `/` — the skills appear in the list. Or just describe the task
("refresh this README", "write the PR description") and Claude picks the right one automatically.

## Why skills beat prompts

A good skill encodes a *complete workflow* — the phases a senior engineer runs, in order, with explicit
verification gates and stop conditions — instead of a one-line request. The result is consistency: Claude
does the whole job the same careful way on the tenth run as the first.

## Want the full set?

These two are the free tier of **[The Production Pack](https://winterjoy1.gumroad.com/l/qnrbr)** — 10
battle-tested skills for shipping real software with Claude Code:

`/legacy-audit` · `/n-plus-one-hunter` · `/migration-safety` · `/release-captain` ·
`/test-gap-analysis` · `/security-sweep` · `/api-contract-guard` · `/perf-baseline` ·
`/incident-postmortem` · `/dead-code-reaper`

**→ Get all 10: [winterjoy1.gumroad.com/l/qnrbr](https://winterjoy1.gumroad.com/l/qnrbr)**

---

*Honest note: these skill documents were authored with AI assistance and shaped by real production
experience. Every workflow was tested in Claude Code before release. MIT-licensed — use them anywhere.*
