# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project in one line

Not yet defined. Replace this with one sentence on what the project is, and point to `docs/project.md`.

## Rule 1: Keep project memory in the docs, every session

The user should never have to re-explain earlier conversations or give the same context twice. The files in `docs/` are the project's memory across sessions.

- **At session start:** read the doc index below, then read only the docs relevant to the task.
- **During work:** whenever a decision is made, a preference is stated, a requirement changes, or something non-obvious is learned, write it into the right doc. Don't ask whether to document it. Just do it.
- **Background is fine:** doc updates can go to a background subagent while you do the main task. Check that the update landed before ending the turn.
- **Keep docs current, not just added to:** edit or delete stale content rather than appending contradictions. Each fact lives in exactly one place.
- **Keep docs small and topical:** one file per topic. When a topic grows beyond what `docs/project.md` should hold, split it into a new file and add it to the index.
- **Update the index** below whenever a doc is added, renamed, or removed.

### Doc conventions

- **The decisions log holds the reasons; the topic docs hold the current state.** `docs/decisions.md` records what was decided and why, by date. The current design lives in `docs/project.md` or a topic doc. When a decision changes the design, update the design doc and log the reason.
- **Mark reversals.** An entry that replaces or partly reverses an earlier decision says so, for example "Supersedes YYYY-MM-DD's …", and the design doc is updated to match.
- **Say who decided.** Each entry notes whether the user decided, or Claude chose on its own. Claude's own choices are logged as "awaiting review", tagged **Implemented** in the design doc, and added to next steps for the user to review.
- **Record what was tried and dropped,** and why, so a later session doesn't propose it again.
- **Status entries are dated, newest first, and say how far the work was verified:** built, deployed, tested end to end, or not yet tested.
- **Open questions sit next to the design they affect,** in the topic doc, not in one central list.

### Doc index

| File | Contains | Read when |
|------|----------|-----------|
| `docs/project.md` | What the project is, current status, open questions, next steps | Every session |
| `docs/decisions.md` | Dated log of decisions and user preferences, with reasons (the current design lives in the topic docs) | Before making a design or tooling choice |

## Rule 2: Commit early and often

- Commit after every coherent unit of work (a working change, a doc update, a refactor step). Don't batch unrelated changes.
- Commit before running long tests or builds, not after they pass. Fix failures in follow-up commits.
- Committing needs no permission. Pushing, force-pushing, and rewriting history still need confirmation.
- Doc updates can be committed together with the change they describe or on their own.

## Rule 3: Don't edit shared external docs unless asked

Don't change Notion pages, Slack, Google Docs, or other shared external documents unless the user explicitly asks for that edit. A link to a stale doc is reference material, not a request to rewrite it. Describe the change in chat and ask first.

## Commands

None yet. The repo has no code. Once it does, add build, test (including single-test), and lint commands here. Also name a fast check to run after every change, and note gotchas a new session would otherwise have to relearn.

## Architecture

None yet. Add the big-picture structure here (or in a dedicated `docs/architecture.md` linked from the index) once code exists.
