## Assignment 2.1

### Question 1 — Scrum or Kanban

For CampusFlow, I would run it as Kanban rather than Scrum. Scrum requires fixed-length sprints, sprint planning meetings, and daily standups — all of which assume a team coordinating together on a committed schedule. Since I'm working on CampusFlow solo, in short and unpredictable sessions, and my scope will keep evolving as I learn new things, committing to a fixed sprint backlog would be artificial and hard to stick to. Kanban's continuous flow — pulling the next card when I have time, adding new cards whenever new ideas or requirements appear — fits a one-person, flexible workflow much better.

For TrackFlow, I would lean toward Scrum instead, or at least a lighter version of it. TrackFlow is a shared, instructor-led project with multiple people contributing, so having a fixed rhythm (sprints, standups, a shared sprint backlog) helps keep everyone coordinated and prevents work from silently drifting out of sync. My answer differs between the two projects because the deciding factor isn't the type of project — it's team size and coordination need. Solo work benefits from Kanban's flexibility; team work benefits from Scrum's shared structure and checkpoints.

### Question 2 — A real trade-off

I'm picking "working software over comprehensive documentation." For CampusFlow, this shows up when I'm planning out the epics and figuring out what fields each card needs (subject, due date, type, etc). I could sit and write a full detailed spec for every single field and status before touching any code, or I could just get a basic working version going and figure out the details as I actually use it. I'm going with working software over documentation, mainly because I'm the only one building and using this thing, so I'll learn way more from actually using an early version than from trying to guess everything upfront on paper.

### Question 3 — Critique and redesign

# Problems with the TaskBoard Pro brief:

1. No changes allowed once design starts (Phase 2) — this goes against "responding to change over following a plan." You always learn more once you're actually building, so locking everything down that early just means the end result misses stuff you would've figured out along the way.
2. Two whole weeks spent just writing a spec document with nothing working yet — goes against "working software over comprehensive documentation." There's no way to even check if the plan makes sense before sinking all that time into it.
3. No demos until the entire build phase (Phase 3) is done — goes against "customer collaboration over contract negotiation." By the time anyone sees it, it's basically already finished, so there's no room left to actually change anything based on feedback.

# Agile redesign for CampusFlow:

Iteration 1: just get the basic board working — To Do, In Progress, Done columns, and the ability to add a card with a title and due date. Nothing fancy, no login, no categories, just to see the core thing work.
Iteration 2: add tagging so cards can be marked as Assignment/Test/Activity, plus sort by due date. Use it a bit in between iterations to see what's actually missing before piling on more features.

### NOTES.md Updates

1. Naming it made it real
Yes, picking CampusFlow as a concrete domain changed how I thought about the project a lot. When it was just an abstract "generic board," it felt like a theory exercise. Once I decided it was specifically for tracking assignments, tests, and activities, I started thinking about real details — like what fields a card actually needs (subject, due date, type) and what a student would realistically want to see first. It made the planning feel like I was building something for myself, not just filling in a template.

2. Where the sample brief's problems actually bite
Out of the three problems I identified in Question 3, I think the "no demos until the build phase is complete" issue would hurt the most in practice. If nobody sees the product until Week 9, there's no chance to catch a wrong assumption early — you could spend months building the wrong thing and only find out once it's basically too late to change course cheaply. The other two problems (locked requirements, documentation-heavy start) are bad, but this one means feedback comes far too late to actually be useful.

## Assignment 2.2

### Question 1 — Roles, solo and shared
For TrackFlow, roles would plausibly land as: Product Owner = whoever set up the repo and is driving the shared vision (e.g. Nadio75, since he initiated the repo structure), Scrum Master = whoever keeps standups/process on track in class, Dev Team = the rest of us contributing code.

For CampusFlow, I'm all three roles. The one I expect to neglect first is Scrum Master — process and habits feel like overhead when I just want to code, so standups and backlog grooming are the first things I'd skip under pressure. Concrete habit to stop that: write my daily standup note (3 lines: did/next/blocked) before opening my code editor each day, not after.

### Question 2 — Definition of Ready / Definition of Done (Epic: Core Board & Task Management)
**Definition of Ready:**
- Item describes a single, specific user action (not a vague feature)
- Item has a clear column/category it belongs to (To Do/In Progress/Done)
- Item can realistically be built in under a day
- No unresolved question about what "finished" looks like for it

**Definition of Done:**
- Feature works end-to-end without crashing
- Data persists after a page refresh
- Code is committed and pushed to the repo with a clear commit message
- I manually tested the happy path at least once

### Question 3 — The artifact most at risk
The Sprint Backlog is most at risk in a solo, daily-cadence project — it's tempting to just "know what I'm doing today" in my head instead of writing it down. The actual cost: without a written Sprint Backlog, there's no clear line between "backlog" and "committed work," so it's easy to overcommit, lose track of what actually met the Definition of Ready, and standups become guesswork instead of a real status check.

### NOTES.md Updates

1. **Role I'll neglect — anything changed?**
Still Scrum Master. If anything, building the actual Product Backlog and Sprint 1 Backlog today confirmed it — I spent almost all my energy on the "what to build" (Product Owner) and "building it" (Dev Team) side, and had to consciously force myself to write the standup log and DoR checks rather than skip straight to coding.

2. **What DoR actually filtered out**
Yes — I originally expected to pull "Set a due date on a card" into Sprint 1, but it didn't meet my Definition of Ready because I hadn't decided on a date format/UI yet. Same with sorting, priority tags, and search — they depend on the due-date feature landing first, so they got pushed out of Sprint 1 even though I initially assumed they'd make the cut.
   

   ## Assignment 2.3

### Question 1 — Choosing a view
List is CampusFlow's primary daily view — most days I just need a flat, sortable list of
what's due, and List makes it fastest to scan and update status. Board would help during
active sprint work, when I want to see To Do / In Progress / Done at a glance instead of
scrolling a list. Timeline would help at the start of a term, when I need to see assignment
and test due dates laid out across the weeks to spot clashes early.

### Question 2 — Custom fields, deliberately
- **Priority** (High/Medium/Low) — supports filtering "what do I do first" when several
  items are due close together.
- **Type** (Assignment/Test/Activity/Class Task) — supports filtering by category so I can
  see, e.g., only tests coming up.
- **Due Status / Story Points** — supports estimating how much work is left in a sprint and
  spotting overloaded weeks before they happen.

### Question 3 — Tag or field?
- Tag example: `needs-review` — a free-form, cross-cutting label I might reuse on any task
  regardless of project.
- Custom field example: `Type` (Assignment/Test/Activity/Class Task) — scoped, structured,
  and every task must have exactly one value.
- If swapped: making `Type` a tag would let a task have zero or several types (or none at
  all), so filters and reports by type would become unreliable. Making `needs-review` a
  custom field would force it into a fixed dropdown scoped to this one project, when it's
  really a loose label I want to reuse across projects.

  ### Part 2 — QuickNotes practice evidence
Task 5 saved filter (needs-design + unassigned) built via Advanced Search, since the
project's Filter panel doesn't expose Tags as a filter option on this Asana plan.


### NOTES.md Updates

1. What the QuickNotes exercise revealed:
   Building QuickNotes first showed me that Asana's free plan doesn't expose Tags as a
   Filter condition — I only found this out because I tried it on the throwaway project
   first. That meant when I got to my real CampusFlow project, I already knew to lean on
   Priority/Completion status for saved filters instead of tags, which saved time.

2. Where Sprint 1 Backlog and reality disagreed:
   Moving sprint-1-backlog.md into Asana surfaced a naming mismatch between my own planning
   docs — product-backlog.md only grouped items under 2 broad headers, while epics.md had
   5 proper epics. I had to manually re-sort the 15 backlog items into the correct 5 epics
   in Asana, which wasn't obvious until I actually tried to organize sections "by epic" and
   the two files didn't line up.

3. The field vs. tag call I almost got wrong:
   I nearly tried to use a tag to mark Sprint 1 items instead of just moving them into a
   proper Sprint 1 section — a tag would have let an item sit in multiple "sprints" at once
   with no clear single home, whereas a section keeps it unambiguous which sprint an item
   actually belongs to.


## Assignment 2.4

### Question 1 — Rewrite Sprint 1 as real user stories

1. As a student using CampusFlow, I want to see a board with three columns, so that I can visually organize my tasks by status.
2. As a student using CampusFlow, I want to add a new card with a title and description, so that I can capture a new assignment without losing detail about it.
3. As a student using CampusFlow, I want to edit an existing card's title and description, so that I can update it as the task changes.
4. As a student using CampusFlow, I want to delete a card, so that I can remove tasks that are no longer relevant.
5. As a student using CampusFlow, I want to move a card between columns, so that I can reflect my actual progress on a task.
6. As a student using CampusFlow, I want to mark a card as complete, so that I can see finished tasks without deleting them.
7. As a student using CampusFlow, I want to categorize a card by type, so that I can tell at a glance what kind of item it is.
8. As a student using CampusFlow, I want core card actions to be saved immediately, so that my changes survive a refresh.

Rewriting these actually changed how I thought about a couple of them. "Categorize by type" as a backlog phrase sounded like just a label, but writing out the "so that" forced me to think about *why* a student would care — being able to tell what kind of task something is at a glance, without opening it. The persistence story changed the most: as "persist board data" it sounded like one small task, but writing it as a full story made me realize it depends on every other feature already existing first.

### Question 2 — Acceptance criteria

1. Board with three columns
   - Board shows exactly three columns, labeled To Do, In Progress, Done
   - Columns are visible immediately on load, no extra clicks

2. Add a new card
   - Title is required; description is optional
   - New card appears in the column it was created in, right after saving
   - Each card gets a unique ID

3. Edit an existing card
   - Edit view is pre-filled with the current title/description
   - Saving updates the card in place, no duplicate created
   - Cancelling leaves the original data untouched

4. Delete a card
   - Delete is reachable directly from the card
   - A confirmation step prevents accidental deletion
   - Deleted card disappears from the board and from storage

5. Move a card between columns
   - Card can move from any column to any other column
   - New column is saved immediately after the move
   - Moving a card doesn't lose its title, description, or category

6. Mark card as complete
   - Completion is a distinct state from column position
   - Completed cards are visually distinct (e.g. checkmark or strikethrough)
   - Marking complete/incomplete is reversible

7. Categorize card by type
   - Type is chosen from a fixed list at creation or edit
   - Type is visibly shown on the card
   - Every card always has exactly one type

8. Persist core card actions
   - Card data (title, description, column, type, complete status) survives a page refresh
   - Data survives closing and reopening the app
   - No data loss on add, edit, move, or delete

### Question 3 — INVEST check

I picked story 8 (persist core card actions) because it's the one I was least confident about.

- **Independent** — Fails. It depends on every other story existing first, since it has to save whatever data those features produce.
- **Negotiable** — Passes. How I persist the data (localStorage, a file, a backend) is still completely open.
- **Valuable** — Passes. Losing your task list every time you refresh the page would make the app pretty useless.
- **Estimable** — Borderline. It's hard to size properly until the other stories' data shapes are actually settled.
- **Small** — Fails. Covering "all card data" across every feature is a cross-cutting concern, not one small slice of work.
- **Testable** — Passes. I can refresh the page and check the data is still there.

Since it fails Independent and Small, I'd change it. Instead of "persist all board data," I'd narrow it to something like: "As a student, I want core card actions (add/edit/delete/move) saved immediately, so my changes survive a refresh." That shrinks the scope down to just the CRUD actions, which makes it much closer to independent — the type and complete-status fields naturally get saved along with those same actions anyway, so there's no need for a separate story just for them. That does change its scope: it becomes smaller and more testable on its own, but it's a more honest size for one sprint item.

### Question 4 — Estimating alone, again

| Story | Points |
|---|---|
| Board with three columns | 2 |
| Add a new card | 3 |
| Edit an existing card | 2 |
| Delete a card | 1 |
| Move a card between columns | 3 |
| Mark card as complete | 2 |
| Categorize card by type | 2 |
| Persist core card actions | 5 |

The story that surprised me most was persistence. As a raw backlog phrase it felt small — just "save the data somewhere" — but once I wrote it as a full story and ran it through the INVEST check, it became obvious it touches every other feature's data shape. That's why it jumped from feeling like a 2 or 3 to an honest 5.

## Assignment 3.1

### Q1 — Suggesting mode vs. comments vs. direct edits
- **Direct edit**: for my own sections, or fixing an obvious typo/broken link in CampusFlow's README — no ambiguity, no need to ask.
- **Suggesting mode**: editing someone else's writing where they should approve the change — e.g. tightening the wording in my epics.md Goal section before a teammate signs off on it.
- **Comment**: flagging something without touching the text — e.g. "should this task belong in Sprint 1 or Sprint 2?" on the Daily App planning doc, where I'm asking, not editing.

### Q2 — Permissions, deliberately
- **Editor**: me only (solo project) — I'm the one making structural changes to CampusFlow's docs/sheets/decks.
- **Commenter**: bitcube trainer/lecturer — needs to give feedback without being able to restructure my work.
- **Viewer**: classmates/other cohorts — can see progress for reference or peer learning, no reason for them to edit or comment on a solo project.

### Q3 — Sync or async?
- **Live (Meet)**: blocking questions and anything needing back-and-forth — e.g. "is CampusFlow's scope realistic for 4 weeks?" needs real discussion, not a comment thread.
- **Async (Docs/Sheets/Calendar)**: goal-setting, task assignment, status updates — these are one-directional or slow-moving, so writing them down once and letting people read on their own time is faster than scheduling a call.
- Justification: sync time is expensive (everyone stops what they're doing); async is for anything that doesn't need a live decision.

## NOTES.md Updates

### 1. What the "TidyUp" practice revealed
Doing the fake TidyUp version first actually helped — I got confused at first about why I was typing content about a chore app when it had nothing to do with CampusFlow, but once I understood it was just for practicing the mechanics (comments, suggesting mode, permissions), it made the real CampusFlow kickoff much faster since I already knew where everything was (data validation, conditional formatting, speaker notes) instead of hunting for it for the first time on my real project.

### 2. The permission you almost got wrong
I nearly added more people than necessary just to "practice" the different access levels, before realizing one deliberate share (Commenter for my trainer, with a clear reason — feedback without letting them restructure my docs) was enough. It made me realize permissions should be based on who actually needs access and why, not on adding people just to fill out the levels.

### 3. Sync vs. async, in practice
My Q3 split mostly held up — goal-setting, task status, and the tracker were fine async, since I was working solo and didn't need real-time input to fill those in. The one place a live conversation still mattered was clarifying scope decisions (e.g. confirming what's in/out of scope for CampusFlow) — that's the kind of thing that benefits from a quick back-and-forth rather than a comment thread, even if the "meeting" ends up being a short solo stand-up talking through it out loud.

## Real Artifacts — Assignment 3.1

Drive:https://drive.google.com/drive/folders/1sGQhieBo0rySGme_pDNNlmEGuo5GbXXb?usp=drive_link
Doc: https://docs.google.com/document/d/1JEH7z0fo9G4O4edURqdtquggSP13ro-otitSxYrFqzM/edit?tab=t.0

Sheet:https://docs.google.com/spreadsheets/d/1c7NcIkgd8c_Vtmpa6Gm9kWQbc9oBSqR5aXUAOnH59_4/edit?gid=0#gid=0

Slides:https://docs.google.com/presentation/d/1SJscWijOBf3_06D2EoMqHjBj4fYoxMzCTCR61d5jFVs/edit?slide=id.p#slide=id.p

Calendar:https://calendar.google.com/calendar/u/0/r/eventedit/NnJ2ZTJiOHVmYzc1OGpkdHFscmhtMWw2YTEgbWF0aGFib21vaGFwaTk5QG0


## Assignment 3.2

### Question 1 — Beyond the core four

My Team Directory repo would benefit from a Known Limitations section. It's a single-file PowerShell script (team.ps1 + team.txt) with no validation beyond basics and no concurrent-access handling — someone cloning it without that context might assume it's production-ready or try to scale it to multiple users writing to team.txt at once, causing data loss. Leaving it out means the first person to hit that limitation discovers it by breaking something, instead of reading about it.

### Question 2 — Comment audit

team.ps1 currently has zero comments anywhere in the file, so there isn't an existing bad comment to flag. The line most in need of one that's missing is line 17, the role search filter, which silently assumes every line in team.txt is formatted like "Name, Role: X" — if that format ever changes, the search just returns nothing with no explanation why. A comment explaining that assumed format would save someone real debugging time. A second candidate is line 8, which re-reads team.txt from disk a second time to get the count instead of reusing the members variable already loaded on line 7 — non-obvious and worth a comment explaining whether that's intentional or just an oversight.

### Question 3 — What makes a decision ADR-worthy

I chose to store team data in a plain text file instead of a structured format like JSON or CSV. This is ADR-worthy because it trades off simplicity (no parsing library needed, human-readable) against extensibility (harder to add fields later, no schema validation) — a future contributor needs to understand why plain text was chosen deliberately, not just inherited. A routine detail, like a variable name, needs no such explanation because there's no real alternative worth weighing.

## Assignment 3.3

### Part 1 — Written Decisions

**Q1 — Channel choice, for real**
This week I messaged Andiswa on Slack asking about the CampusFlow board layout while also flagging a merge conflict in the same message. The merge conflict part should've been its own message (or even a quick call) since it was blocking, and the layout question was a "no rush" async question that got lost because it was bundled with something urgent. What I'd change: split it into two messages — one flagged "blocking, need this today" for the conflict, one tagged "no rush" for the layout opinion — so she could triage instead of reading past the urgent part.

**Q2 — The self-check you did or skipped**
Blocker: the add-card form in `index.html` wasn't saving new cards to the To Do column. Before asking anyone, I should have checked the browser console for JS errors and confirmed the event listener was actually attached to the form — and I did check the console, but I skipped checking whether the script tag was even loading (it wasn't — wrong file path). So: partial self-check, missed the more obvious thing first.

**Q3 — Specific vs. vague feedback, side by side**
Specific: "In `addCard()`, you're pushing the new card straight into the DOM before validating that the title field isn't empty — move the empty-check above the DOM insert so blank cards can't get created."
Vague: "This function needs work."
The difference: specific feedback names the exact line/behavior and gives a concrete fix direction; vague feedback tells you something's wrong but not what or where, so the person has to redo your diagnostic work themselves.

### Part 2 — Given Scenario Practice (BudgetBuddy)

**Task 1 — Channel rewrite**
Original: "hey so the budget sync feature is kind of broken and also can we talk about whether we're doing the export feature this sprint, no rush but let me know"

Slack (quick, needs a fast async answer):
> "Budget sync looks broken — categories aren't totaling correctly after a sync. Anyone free to pair on this in the next hour? If not I'll keep digging and post what I find."

Email (or a written sprint-planning doc/thread, not urgent, needs a considered answer):
> Subject: Export feature — in or out for this sprint?
> "Quick scope check: are we committing to the export feature this sprint, or pushing it to next? No urgency on this — just want to close it out before planning next sprint. Let me know your thinking whenever's convenient this week."

**Task 2 — Question rewrite**
Original: "the totals aren't adding up right, anyone know why?"

Rewritten:
> "Context: working on the category totals in `updateBudget()`. What I tried: added a $50 expense to Groceries, expected the category total to go from $200 to $250. What happened: it shows $200 still — the category total isn't updating, though the overall budget total did update correctly. Ask: can someone check if `updateBudget()` is supposed to update both the category and overall totals, or is category recalculation happening somewhere else that I'm missing?"

**Task 3 — PR feedback on `updateBudget()`**
> "This function is doing three separate jobs in one 40-line block — validating input, recalculating every category total, and writing to the DB — which makes it hard to tell which part broke if something goes wrong (like the category-total bug we just hit). Suggestion: split into `validateInput()`, `recalculateTotals()`, and `saveBudget()`, and call them in sequence from here. Also a couple of inline comments on the recalculation logic would help — I had to trace through it line by line to understand the loop."

**Task 4 — Receiving it well**
> "Thanks for this — you're right that it's doing too much at once, and I can see how that would've made the category bug harder to catch. Quick clarifying question: when you say split out `recalculateTotals()`, should that still take the whole budget object, or just the one category that changed? Want to make sure I split it the way that actually helps debugging, not just for the sake of shorter functions. I'll get a revised version up today."

### Part 3 — Applying This to Your Real Work

**Task 5 — Real help request**
> "Context: working on the To Do column's add-card form in CampusFlow (`index.html`). What I tried: added a new card via the form, checked the browser console for JS errors, confirmed the event listener code looked right. What happened: no console errors, but no new card appeared and no error either. Ask: could you take a quick look at whether my script tag path is actually loading the JS file? I suspect it's a load-order or path issue rather than a logic bug." *(This is the actual blocker from the add-card form issue — real message you'd send to a mentor/teammate.)*

**Task 6 — Real PR feedback**
Left on index.html, addCard(): addCard() was building the card with innerHTML using 
the raw title/desc values, which means any HTML or script typed into the title or 
description field would actually get executed instead of shown as text. Switched to 
creating the elements directly and setting textContent, so user input always renders 
as plain text regardless of what's typed.
Link: https://github.com/mathabomohapi99-crypto/daily-app/pull/7/changes#r4033132741

**Task 7 — Reflect on real feedback you've received**
Feedback hadn't come in yet by the time I needed to finish this, so I sent an async 
request rather than wait: "Hey, when you're up — could you leave one specific comment 
on my addCard() function in daily-app, or my Assignment 3.2 docs? Whenever's 
convenient, no rush." I'll add the actual feedback and my response here once it comes 
in — sending it async and not blocking on a reply is the same principle from today's 
session (Question 2: don't ask/wait when you could keep moving).

**Task 8 — Before/after a real message**
Before (Slack, sent this week): "hey the merge conflict thing is done btw also do you think we should redo the column layout? no rush"
After (split, applying channel/async norms):
> Slack #1 (resolved status, no action needed): "Merge conflict on daily-app is resolved — pushed the fix, CI's green."
> Slack #2, separate thread (async, no urgency, tagged as such): "No rush — thinking about redoing the column layout on CampusFlow at some point. Curious if you have thoughts whenever you get a sec."
What changed and why: the original buried a status update (needs no reply) inside a question (needs a reply), so both risked getting the wrong response time. Splitting them means the resolved-item doesn't sit there expecting a reply, and the actual question doesn't get buried under it.

### NOTES.md Updates

1. **What BudgetBuddy revealed:** Rewriting BudgetBuddy's bad question made me notice my own habit of asking "why is X broken" without stating what I'd already tried — I do this because I assume it's obvious I checked the console first, but the person reading doesn't know that. Doing it on a throwaway example first made it easier to spot in my real Task 5 request.

2. **The self-check almost skipped:** In Task 5, I almost wrote "the add-card form is just broken, can someone look" before actually re-checking the console — writing Q2 honestly first (where I admitted I'd skipped checking the script path) is what made me go back and check it properly before sending the real request.

3. **Feedback on something real vs. sample:** Writing feedback on my own real `addCard()` function felt harder than BudgetBuddy — with a sample I have no attachment to being "right," but naming a real bug in my own code meant I had to sit with it being a genuine mistake before I could describe it usefully instead of downplaying it.

### Stretch A — Async Slack thread (optional)

> Day 1: "Blocked — add-card form isn't saving new cards to the To Do column. Checked console, no errors shown. Digging into the script load order next."
> Day 2: "Partial update — found it, the script tag path was wrong so the JS never loaded. Fixed the path, form now saves cards. Testing edge cases (empty title, long titles) before calling it done."
> Day 3: "Resolved — add-card form works end to end, pushed to main, CI green."

A fourth teammate joining on day 3 would need: (1) what the original bug was and its symptom (silent failure, no console error), (2) the actual root cause (wrong script path, not a logic bug), and (3) confirmation of current state (fixed, tested, merged) — without those three, "resolved" on its own tells them nothing about what almost went wrong or what to watch for next time.


