---
description: Interview me and set up my household chief of staff (family, pets, routines, tasks) in a private folder.
argument-hint: "[optional: location, default ~/household-cos]"
---

Set up the user's household chief-of-staff system. Load the `household-chief-of-staff` skill first and follow its tone: warm, brief, no interrogation.

## Location

Default: `~/household-cos/`, unless $ARGUMENTS names another location. Confirm it with the user. This folder holds health, child, and relationship details. **If the location is inside a git repo or a synced/shared folder, warn the user and suggest a private location.** iCloud Drive is fine if they want it on their phone, as long as it isn't a shared folder.

If the user already has a filled-in `HOUSEHOLD.md` (for example, one Claude prepared for them earlier), ask for it and use it as the starting point instead of re-asking everything.

## Interview (a few questions at a time; skip anything already known)

Ask in small batches. People with ADHD lose steam with long forms, so aim to have a working system in about 10 minutes, and tell them everything else can be filled in later.

1. **You:** name, time zone, work/school rhythm, best and worst energy times. What helps your brain and what backfires? (Offer examples; don't require a diagnosis or any medical detail.)
2. **Partner:** name, schedule, who usually owns what, and how they like to get logistics.
3. **Kids:** names, ages/birthdays, school/grade, activities, and anything coming up soon.
4. **Pets:** names, species/breed, ages, food, meds/preventives, vet and emergency vet.
5. **Right now:** the 3-5 things weighing on you at home. These seed `tasks.md`.
6. **Anchors:** when to do the morning launch, evening reset, and weekly planning, and how often date night happens.
7. **Connected tools:** which calendar, email, and task app the family actually uses. Check which connectors are available in this session and say which ones you can see.
8. **Hard rules:** confirm the defaults (no sending, booking, or buying without approval; no guilt language; a check on wellbeing if things look dark) and add their own.

## Create (from the skill's `templates/`)

- `HOUSEHOLD.md`, filled in (not left blank).
- `tasks.md`, seeded with what they named, each with a tiny next step. At most 3 items in "Now."
- `routines.md`, filled with their anchor times, plus a "minimum" version of each routine.
- `pets.md`, one section per animal.
- `MEMORY.md`, plus 1-2 real memory files (e.g. `user-plan-style.md`).

## Wire it in

Offer to add this line to `~/.claude/CLAUDE.md`:
`> My household chief-of-staff context lives at ~/household-cos/HOUSEHOLD.md. Read it before household tasks.`

Offer to put the recurring anchors on the calendar (as drafts they approve) if a calendar connector is available. Examples: the weekly planning slot, monthly pet preventives, and each pet's annual vet exam.

## Confirm

Show the file tree and verify that the files exist. Read back the top of `HOUSEHOLD.md` so they can correct it. Celebrate briefly ("That's the hard part done"). Then suggest one thing: try `/household-chief-of-staff:today` tomorrow morning.
