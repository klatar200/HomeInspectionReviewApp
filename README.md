# Inspec (working title) — Home Inspection Review App

A review and discovery site for residential home inspectors, starting with new-build buyers within 50 miles of Plainfield, IL. Goal: help buyers find inspectors who are thorough and independent of the builder, and record documented cases where builders restrict or steer inspections.

Status: planning. See PLAN.md (scope, data model, wireframes, phases), DECISIONS.md (what was decided and why), RESEARCH.md (background and sources).

## Develop
Requires Node 22+. `npm install` · `npm run check` (lint, typecheck, test, build) · `npm run dev -w @inspec/api` (API :3001) · `npm run dev -w @inspec/web` (web :5173) · `docker compose up -d db` (local Postgres; copy `.env.example` to `.env`).
