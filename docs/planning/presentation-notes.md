# Presentation Notes — CampusFlow: Developer Onboarding Overview

## Slide 1 — Title (10s)
"CampusFlow — a student academic tracker I built. Quick onboarding walkthrough."

## Slide 2 — Agenda (10s)
"What it does, board structure, tech stack, repo, docs, pitfalls, demo."

## Slide 3 — Problem / Context (30s)
"Students track assignments, tests, activities across scattered tools. CampusFlow
puts it all on one Kanban board. Single-user for now — multi-role is a future epic,
not built yet."

## Slide 4 — Architecture (30s)
"Board → Column (To Do/In Progress/Done) → Card. Working index.html with a live
3-column board and add-card form. Backlog planned in Asana with custom fields and
tags."

## Slide 5 — Key Components (25s)
"Git-tracked repo, plain HTML/CSS/JS front end, docs live alongside the code, Asana
runs the sprint workflow."

## Slide 6 — Repo Structure (25s)
"Repo: daily-app on GitHub. First commit already had README, notes, and a
docs/planning folder — built so a second dev could onboard without me explaining
verbally."

## Slide 7 — Documentation (25s)
"README for what/how-to-run. epics.md for deferred scope. agile-redesign.md for how
the backlog became sprints. Each Sprint 1 item has acceptance criteria."

## Slide 8 — Pitfalls (25s)
"Risk of scope creep into multi-user too early. Column rules need to stay clear.
Asana and code can drift if not updated together."

## Slide 9 — Demo (25s)
"Show the live board, add a card to To Do, then show the matching Sprint 1 story
in Asana."

## Slide 10 — Summary (15s)
"Small, focused tracker with room to grow. Start with README, epics.md,
agile-redesign.md, Asana board. Questions?"

## Anticipated Q&A (keep in back pocket, don't read out)
- Why not multi-user now? → Deferred deliberately, keeps core simple first.
- How would a new dev start? → Clone repo, read README then epics.md.
- Asana/code sync? → Acceptance criteria checked against board before marking Done.