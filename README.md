# Calendar Perso — Grist-Friendly Calendar → Life Planner (Life OS)

A lightweight, dependency-minimal calendar UI built with HTML, CSS, and vanilla JavaScript, designed to embed in other apps (Grist, Linea21, intranet portals).
Originally focused on business-hours weekday scheduling, **now evolving into a full Life Planner (Calendar + Tasks + Journal + Goals + Reviews + AI scheduling)** — still embed-friendly, responsive, and minimal-deps.

Live demo: https://nicodioub.github.io/calendar-perso/

---

## 🎯 Vision

Build **one personal Life OS** that manages:
- Planning (calendar + time blocking)
- Tasks (weekly execution + carryover)
- Long-term goals (yearly/multi-year)
- Journal & reflection (daily prompts, mood, habits)
- Reviews (weekly/monthly/yearly)
- AI agent that can **reschedule and optimize** your life (trading / DevOps / alternance / sport / personal)

Key principles:
- Embed & Integration-first: works as an embeddable web app (Notion, portals) and can connect to major calendar providers (Outlook/Google/CalDAV).
- **Mobile-first responsive** (PWA-ready)
- **Offline-first** (local data first)
- **Zero/low dependencies** (vanilla JS)
- **Privacy-first** (no tracking by default)

---

## ✨ Current Features (Implemented)

- Weekday view (hide Saturday/Sunday)
- Business hours (default: 07:00–19:00)
- Responsive layout for desktop/tablet
- Simple data adapter (plug a JSON feed / API)
- Embeddable via `<iframe>` in Grist or any CMS
- Zero build tools (open `index.html`)

---

## ✅ Planned Features (Backlog / Roadmap)

### 1) Core Planning — 
**Goal:** fast scheduling + reliable weekly planning + smooth rescheduling.

**MVP**
- [ ] **Tasks carryover**: move unfinished tasks from week → next week automatically
- [ ] Task statuses: `todo / doing / done / skipped`
- [ ] Quick add task/event (keyboard + mobile input)
- [ ] Drag & drop time blocks (desktop + mobile-friendly fallback)
- [ ] Bulk actions: move/copy blocks to another day/week

**V1**
- [ ] Monthly view + mini overview navigation
- [ ] Year view + **completion heatmap**
- [ ] Custom views: business-hours only / weekdays only / focus mode
- [ ] Buffers & routines: auto-add “sleep/meal/gym” blocks from habits templates
- [ ] Smart recurrence rules (weekly tasks, monthly routines)

**V2**
- [ ] Multi-calendar overlay (Personal / Work / School / Trading)
- [ ] Conflict detection + suggestions
- [ ] “Energy-aware” planning (heavy tasks in high-energy slots)

---

### 2) AI Scheduling Agent (Conversational)
**Goal:** talk to your calendar like Claude: schedule, move, optimize, explain.

**MVP**
- [ ] AI chat panel (embedded) with safe commands
- [ ] Natural language commands:
  - “Décale tout d’1h, je suis en retard”
  - “Planifie ma semaine trading / DevOps”
  - “Rappelle-moi les tâches alternance”
- [ ] “Explain why” mode: AI must justify suggestions (“pourquoi ce créneau ?”)
- [ ] Manual fallback always available (AI never locks you)

**V1**
- [ ] AI prioritization: deadlines + estimated duration + energy level
- [ ] Auto-rescheduler with constraints (no overlap, business hours, breaks)
- [ ] Templates: “Semaine Alternance”, “Semaine Trading”, “Semaine Exam”

**V2**
- [ ] Personalized planning rules (your habits: sleep schedule, meals, sport)
- [ ] Voice input (optional) for mobile PWA
- [ ] “What-if” planning simulations (time budget + forecast)

---

### 3) Journal & Reflection (Not in Morgen)
**Goal:** daily journaling linked to tasks/events, searchable, structured, useful.

**MVP**
- [ ] Daily journal entry attached to each day
- [ ] Prompt system (custom prompts):
  - “Qu’as-tu appris aujourd’hui en trading ?”
  - “1 chose réussie / 1 chose à améliorer”
- [ ] Mood tracking (simple scale + tags)

**V1**
- [ ] Journal linked to tasks/events (e.g., “post-gaming journal”, “after workout”)
- [ ] Search (by text/tags/date)
- [ ] Habit streaks (sleep, meals, sport, study, journaling)

**V2**
- [ ] Attachments: notes/photos (lightweight)
- [ ] Optional OCR (via Python backend) for photo notes
- [ ] Insight summaries: patterns between mood ↔ tasks ↔ habits

---

### 4) Reviews (Weekly / Monthly / Yearly)
**Goal:** automatic retrospectives with stats + AI insights.

**MVP**
- [ ] Weekly review page: done vs planned, carryover list, blockers
- [ ] Basic stats: completion %, total hours planned vs completed

**V1**
- [ ] Monthly review: focus areas, missed routines, top categories
- [ ] AI-generated review summary (editable)

**V2**
- [ ] Annual review:
  - “Tâches 2026 : X% done, retards sur Y, succès sur Z”
  - Insights & recommendations (ex: “moins X, plus Y”)
- [ ] Goal tracking report (milestones, progress forecasting)

---

### 5) Goals & Bucket List (Long-Term)
**Goal:** connect “big life goals” → milestones → calendar tasks.

**MVP**
- [ ] Goals dashboard (yearly + multi-year)
- [ ] Milestones per goal + link to tasks/time blocks

**V1**
- [ ] Wheel of Life categories (health, career, trading, learning, social, etc.)
- [ ] Bucket list (checklist) + conversion into scheduled tasks

**V2**
- [ ] Visual bucket list (map/travel pins) — optional module
- [ ] AI forecasting: “à ce rythme, objectif Q2 OK ?”

---

### 6) Integrations & Automation
**Goal:** connect your real world tools to tasks/calendar.

**MVP**
- [ ] Import/export JSON (backup + restore)
- [ ] Simple “data adapters” for Grist tables

**V1**
- [ ] Google Calendar sync (optional)
- [ ] Notification system (local reminders)

**V2**
- [ ] Trading integrations (alerts → tasks): MetaTrader5 / HyperLiquid (optional)
- [ ] DevOps integrations: GitHub issues → tasks, VS Code context (optional)
- [ ] Two-way sync (advanced)

---

### 7) Mobile, Offline & Embed (Non-negotiable)
**Goal:** smooth experience on iPhone/Android + embeds.

**MVP**
- [ ] Fully responsive UI (phone/tablet/desktop)
- [ ] Offline-first storage (localStorage/IndexedDB)
- [ ] PWA basics (installable, offline cache)

**V1**
- [ ] Mobile drag alternatives (tap-to-move, long-press)
- [ ] Fast week navigation (swipe)

**V2**
- [ ] Multi-device sync strategy (privacy-first)

---

### 8) Data Model & Storage
**Goal:** stable structure to support everything.

**Core entities**
- Events (time blocks)
- Tasks (with status + carryover)
- Journal entries (text + mood + tags)
- Goals (milestones, category)
- Habits (streaks, schedule rules)

**Storage layers**
- Local: JSON + IndexedDB
- Optional: backend sync (Python/FastAPI) later

---

## 🧱 Tech Stack

- HTML5 + CSS3
- Vanilla JavaScript (no framework)
- Optional: tiny local server for dev (any static file server)
- Optional (future): Python backend (FastAPI) for reviews/sync/OCR
- Optional (future): Claude/LLM API for AI scheduling agent

---

## 🗺️ Suggested Implementation Steps

1) **Local storage layer** (tasks + journal + goals)
2) **Tasks carryover + statuses** (weekly execution)
3) **AI agent v0** (basic commands: “move everything 1h”)
4) **Review weekly/monthly** (stats + summary)
5) **PWA + mobile polish**
6) Optional integrations (Grist/Google/Trading/DevOps)

---

## 📌 Project Status

- Current: calendar UI stable + embed-friendly
- Next: tasks carryover + AI reschedule + journal (MVP Life Planner)

---

## License
(choose: MIT / Apache-2.0 / GPL-3.0)
