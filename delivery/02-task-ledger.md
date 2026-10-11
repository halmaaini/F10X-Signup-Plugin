# Task Ledger

Single source of truth for task status. Statuses: `Not Started`, `In Progress`, `Blocked`, `Done`.

| Task ID | Task | Status | Depends On |
|---|---|---|---|
| P1-01 | Set up repo from TheKit; read sponsor portal and design reference; screenshot live site | `Done` | — |
| P1-02 | Owner Q&A; lock decisions, PRD, roadmap | `In Progress` | P1-01 |
| P1-03 | Clickable demo artifact (registration, emails, admin, QR, poster maker) | `Not Started` | P1-02, owner's poster sample |
| P1-04 | Owner approves demo | `Not Started` | P1-03 |
| P2-01 | Plugin build | `Not Started` | P1-04 |
| P2-02 | GitHub updater + `bin/build.sh` + `dist/` | `Not Started` | P2-01 |
| P3-01 | Local WordPress end-to-end test | `Not Started` | P2-02 |
| P3-02 | Independent code review; fix every finding | `Not Started` | P3-01 |
| P3-03 | Plain-English README (install, go-live, limits, security, troubleshooting, updates) | `Not Started` | P3-02 |
| P3-04 | Staging, then live | `Not Started` | P3-03 |
