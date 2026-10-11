# AGENTS.md — Agent Entry Point

You are working on **AI Dubai Registration**. This repository is governed by a **Project Kit** — a set of docs that define what to build, how to build it, and how to behave while building it. **Do not write code or plan work before reading it.**

## Read this first, every session

1. **`./START-HERE.md`** — the map: what the kit is and how it's organized.
2. **`./MANIFEST.md`** — the rule for **how to treat every doc** (which to populate, edit in place, only append to, never hand-edit, or delete).
3. **`./decisions.md`** — the **source of truth**. Every other doc derives from it.
4. The **always-loaded** governance set listed in `./governance/README.md`.
5. If you're picking up build work: **`./delivery/02-task-ledger.md`** — the next unblocked task.

> `.` is wherever the kit lives in this repo (e.g. `.`, `planning/`, or `docs/`). Set it once above.

## Non-negotiable behaviors

- **Respect each doc's lifecycle** (from `MANIFEST.md`): never edit an `append-only` log's past entries; never hand-edit a `derived` doc to disagree with `decisions.md` — change the decision first, then regenerate.
- **Honor the project's hard lines** in `./governance/13-domain-hard-lines.md`. These are the guarantees the product rests on. Crossing one is never an acceptable trade-off.
- **Confirm a task's dependencies are done** before starting it, and update its status in the ledger as you go.
- **Ask, don't guess** when a requirement is ambiguous and guessing wrong is costly (see `governance/01-agent-rules.md`). Log gaps in `./logs/gap-log.md`.
- **Run `bin/build.sh` after any plugin change** and bump the version in the plugin header, the version constant and `readme.txt` together; commit the rebuilt `dist/` zip.
- **Commit as halmaaini (haithamalmaaini@hotmail.com)** with no co-author or AI attribution lines (D-10).
- **Cite the decision** (`(D-…)`) behind any non-obvious rule you enforce in code (the traceability spine).

## What this repo is

A WordPress plugin for aidubaiconference.com/2026 (Future 10X): visitor registration, confirmation and update emails, personal QR codes, and an "I'm attending" poster maker. See `product/prd.md` and `decisions.md`.

---

*If the kit and reality disagree, fix the code or update the doc — never silently ignore both.*

---
<!-- Attribution (required by CC-BY-4.0 / MIT — please keep). -->
Built with **TheKit** by Haitham Al Maaini · https://github.com/halmaaini/TheKit
Licensed CC-BY-4.0 (docs) / MIT (code): https://github.com/halmaaini/TheKit/blob/main/LICENSE
