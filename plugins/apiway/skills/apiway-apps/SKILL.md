---
name: apiway-apps
description: Build and update the person's Apiway apps — CRMs, Telegram bots, internal tools — hosted by Apiway (its own database, address, sign-in). Use when the person asks to create, change or fix an Apiway app, or says "make me a CRM / a bot / an app".
---

# Apiway apps

Apiway hosts apps the person builds with you. You write ordinary code; Apiway gives each app a
database, an address, sign-in for the team, a design kit and a PREVIEW. The person publishes.

## A new app

1. `create_code_app` with a name and a kit (`crm`, `telegram-bot`, `blank` — call without `kit` to
   see them).
2. The brief: `get_setup_questions` → ask them with your question tool (offer the options; the
   business type fills the rest) → `submit_setup_answers`. Apiway puts the base app in the preview.
3. `get_code_app` → run its download command in a new folder → follow that folder's AGENTS.md,
   BRIEF.md and SETUP.md.

## An existing app

`list_code_apps` → `get_code_app` (slug) → work in its folder by its AGENTS.md. If the folder is
already there, start with `get_app_kit`.

## Every task

1. `get_app_kit` — if its version differs from `apiway-kit/VERSION`, run the command it returns.
2. Build it. Report each step with `report_progress` (in the person's language) — they watch it.
3. Update the preview: `npm run typecheck`, then `start_preview_update` → run the upload command →
   `finish_preview_update`. If it fails, read the log, fix, try again.
4. When it works, call `report_progress` with `done: true` and paste the message it returns to the
   person as it is.
5. The person asks to remove the examples → `delete_example_data`.
6. The person pastes a "Fix" task or says something is broken → `get_code_app_errors` for what broke,
   `get_code_app_logs` for the log; fix it, update the preview, tell them in one sentence what it was.

## Words

Talk to the person in **preview** and **publish** — words like deploy, container or localhost mean
nothing to most people. Understand all of them when THEY say them: any way of saying "put it live"
means publish.

## What Apiway gives this app

- Two copies: the **preview** (every change you make lands here, only the owner sees it) and the
  **published** app at the app's address (changes only when the person presses Publish). One database for both.
- Its own Postgres database, secrets, sign-in, logs (`get_code_app_logs`, slot `preview` or
  `published`), errors (`get_code_app_errors`), and the Apiway SDK (`apiway-kit/sdk`).
