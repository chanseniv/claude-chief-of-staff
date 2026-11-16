# Household Chief of Staff

A Claude Code plugin that acts as the chief of staff for a family home: kids, a partner, pets, routines, appointments, forms, and the hundred small things in between. It's designed for a parent with **ADHD, anxiety, and/or depression**. It holds the household's working memory so you don't have to, shows you only what matters now, and makes starting easy.

It is **not** a therapist or a clinician. It supports the routines your care team recommends, and it stops everything to point you to help if things get dark (US: call or text **988**).

## Install

```
/plugin marketplace add chanseniv/claude-chief-of-staff
/plugin install household-chief-of-staff@chief-of-staff
```

Restart Claude Code, then run `/household-chief-of-staff:setup`. Your household details are written to a **private** folder (default `~/household-cos/`), never to this repo.

## What's inside

| Piece | What it does |
|---|---|
| `agents/household-chief-of-staff.md` | A subagent you can hand any household task to |
| `skills/household-chief-of-staff/SKILL.md` | The operating principles, low-energy protocol, and safety rules |
| `/household-chief-of-staff:setup` | A ~10-minute interview that scaffolds `HOUSEHOLD.md`, `tasks.md`, `routines.md`, `pets.md`, and memory |
| `/household-chief-of-staff:today` | Morning launch: energy check → clock-time day → top three → one prep already started |
| `/household-chief-of-staff:dump` | Brain dump anything; get it back sorted into tasks, calendar, waiting-on, worries, and a parking lot |
| `/household-chief-of-staff:stuck` | Low-energy mode: shrinks the day to the real minimum and gives you one tiny next step |
| `/household-chief-of-staff:reset` | 5-minute evening shutdown: wins, tomorrow's first moves, worry offload |
| `/household-chief-of-staff:week` | Weekly family planning, plus a couple check-in agenda |

## Design choices and the evidence behind them

| Choice | Basis |
|---|---|
| External memory, visible time, reminders at the moment | Barkley's "point of performance" model of adult ADHD; organizing and planning components of CBT for adult ADHD (Safren et al., 2010, *JAMA*) |
| Tiny first step tied to a when/where trigger | Implementation intentions meta-analyses (Gollwitzer & Sheeran, 2006; a 2024 update finds smaller but real effects) |
| On low days, act first and let motivation follow | Behavioral activation for depression (Ekers et al., 2014, *PLoS ONE*, 26 RCTs) |
| Check facts, sort worries, optional worry window | Worry-postponement RCTs (small effects, so it's optional) |
| Scheduled connection with your partner | Gottman lab research on everyday "bids" (observational, so labeled as a heuristic) |
| Three priorities max, buffers, no guilt language | Practical judgment, labeled as such |

Full citations and caveats: [`skills/household-chief-of-staff/reference/evidence.md`](skills/household-chief-of-staff/reference/evidence.md). Pet notes (dachshund back health, lilies and cats) are cited in [`reference/pets.md`](skills/household-chief-of-staff/reference/pets.md).

## Works better with connectors

If you connect Google Calendar, Gmail, Todoist, Notion, or Google Drive, the chief of staff checks real state instead of asking you. It will tell you which connectors it can see. Everything outbound (messages, bookings, purchases) is a draft you approve.
