# Newslings — Claude handoff

This repository is for the **kids' daily world-news podcast** (ages 5–10), not the unrelated Stuff Fascists Like site that also used the `newslings` agent/workspace name.

- `index.html` is the existing website prototype. Do not assume it is deployed or connected to a podcast pipeline.
- `docs/BRIEF.md` is the original product brief, edited to remove local secret locations and to require authentication for any future approval UI. It contains historical plans, not proof that a pipeline, accounts, schedules, domain, or publishing integration exist. Verify service capabilities and pricing before implementation.
- `docs/TTS-SCRIPT-GUIDE.md` contains script-writing and pronunciation guidance.
- The OpenClaw workspace held three MP3 production assets, but they are **not** in this public repository until ownership/licensing is confirmed.
- Credentials and agent auth/session files must never be committed. Use environment variables or a secrets manager; no live keys are included here.

Suggested starting point: inspect `index.html` and the brief, agree on the current product scope, then implement in small testable steps. Keep human approval before any external publication.
