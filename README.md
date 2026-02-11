Calendar Perso — Grist-Friendly Calendar (HTML/CSS/JS)

A lightweight, dependency-minimal calendar UI built with HTML, CSS, and vanilla JavaScript, designed to embed in other apps (e.g., Grist, Linea21, intranet portals).
Focus: business hours, weekdays only, and clean, responsive rendering.

Live demo: https://nicodioub.github.io/calendar-perso/

✨ Features

Weekday view (hide Saturday/Sunday)

Business hours (default: 07:00–19:00)

Responsive layout for desktop/tablet

Simple data adapter (plug your JSON feed / API easily)

Embeddable via <iframe> in Grist or any CMS

Zero build tools (just open index.html)
- peut passer les tâches d'une samine qui n'ont pas été complétées sur une autre semaine
- ai agent that you can talk to that manage planning
- si je dis a mon agent ia que j'ai du retard sur un rendez vous il peut décaler tous mes trucs d'une heure par exemple
- review annuel
- Voici une liste exhaustive de fonctionnalités à ajouter à votre Calendar Perso (ou hybride Grist) pour en faire un Life Planner complet — plus puissant que Morgen (qui reste daily-focused, sans journal profond/bucket list/review annuelle). L'objectif : une app unique gérant toute votre vie (planning, tâches, réflexion, goals long-terme, journal), avec IA (Claude-like) pour automatiser/rescheduler/review. Priorisez embed-friendly, responsive, zero-deps comme votre base HTML/JS.

Core Planning (dépasser Morgen)
Report auto tâches inachevées (semaine → semaine, avec IA priorisation via deadlines/énergie estimée).

Agent IA conversationnel (Claude/Anthropic intégré) : commandes NL comme "décale tout d'1h pour retard RDV", "planifie ma semaine trading/DevOps", "rappelle tâches alternance".

Vues custom : business hours/weekdays only (comme maintenant), + monthly/yearly zoom-out avec heatmap complétion.

Time-blocking IA adaptatif (comme Morgen, mais + buffers auto sommeil/repas basés habitudes).

Journal quotidien intégré : prompts IA ("Qu'as-tu appris trading ?"), mood tracking (liée à tâches), searchable (OCR notes/photos via votre skill Python).

Review annuelle : bilan auto-généré ("Tâches 2025 : 72% done, retards gaming, succès DevOps"), insights IA ("Moins League, + Subnautica pour wellness").

Gratitude/habits/reflections : streaks (sommeil 20h-8h, meals solo), tied à calendrier (ex: "post-gaming journal").
  

🧱 Tech Stack

HTML5 + CSS3

Vanilla JavaScript (no framework)

Optional: a tiny local server for dev (any static file server)
