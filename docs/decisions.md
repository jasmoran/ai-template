# Decisions

Newest at the bottom. Each entry: date, decision, who decided, reason. Mark entries that supersede an earlier one, and Claude's own choices as "awaiting review". The current design lives in the topic docs, not here.

## YYYY-MM-DD: Docs are the cross-session memory

Agents must record discussions, decisions, and context in `docs/` without being asked, keep those docs current, and keep them split by topic so a new session reads only what's relevant.
**Why:** The user doesn't want to re-explain previous conversations or give context more than once.

## YYYY-MM-DD: Commit early and frequently

Commit after each coherent unit of work, and before running long tests or builds.
**Why:** User preference, stated as rule #2 for the project.

## YYYY-MM-DD: No unrequested edits to shared external docs

Notion, Slack, Google Docs and similar are changed only when the user explicitly asks.
**Why:** User preference. A stale doc the user linked was once rewritten without being asked, and they had to restore it.

## 2026-11-17: Robot mower requirements: wire is fine, no running costs

User decided: a boundary wire is acceptable and they will install it themselves; no subscriptions or running costs beyond blades; theft protection isn't worth paying extra for; slope, noise, safety and runtime don't matter beyond finishing 250 m² in 8 hours. Edge trimming (raised lawn edges, fences, under a hedge) is the main priority.
**Why:** Fits their lawn (flat, 250 m², light tree cover) and they want the lowest ongoing cost. Wire-free models gained nothing here and often bring subscriptions. Full requirements are in `docs/robot-mowers-nz.md`.
