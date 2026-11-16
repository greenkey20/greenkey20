# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

The GitHub **profile README** (`greenkey20/greenkey20`, branch `main`). It contains a single file, `README.md`, written in Korean (합니다체) with shields.io badges. There is no build, lint, or test tooling. **A push goes live immediately** at https://github.com/greenkey20, and the page is used as a recruiting reference link, so wrong claims are costly.

## Workflow

- Show the diff first. Commit and push only when the user asks (they have consistently reviewed edits before publishing).
- Another agent has edited the README on the remote before, so run `git pull --rebase` before pushing.
- After publishing, check that every linked repo is public (`gh repo view greenkey20/<repo> --json isPrivate -q .isPrivate`) and that external links resolve. `modu_llm5` is **private**, so it appears as text only, never as a link.

## Where the facts come from

The README summarizes material that lives elsewhere; do not invent or inflate anything.

- **Work experience**: the user's Notion CV (https://greenkey20.notion.site/eunyoung-kang) is the source of truth. It is JavaScript-rendered, so WebFetch and curl return nothing; read the exported `.md` the user provides instead.
- **Project details**: the sibling repos under `~/Documents/Development/` (`inner-orbit`, `song-lingo`, `SOSOBUTSTRONG` (a fork of a team repo), `knou-key-project`). Verify claims against their code or READMEs before writing them.
- **Company code** (`project_if/`, Tradegene) may be read to verify claims, but no source code or internal details go into this README.

## Content rules the user has decided

- Describe the work role accurately. The Tradegene R&R is the **algorithmic-trading backend**: algorithm signal event log and rule signal, Risk Management, Portfolio, plus their `_query` services (Hexagonal + CQRS MSA). The user is also **sub-responsible for the data (custom) management MSA** (KRX order-book snapshots and per-second statistics into Redis/DB); the **execution candles belong to a colleague**, so never claim them. It is not the web front end. The CLS payment system is ProFrame (C) / Oracle, kept separate from the Java/Spring Boot work.
- `project_if/` has no git history, so authorship cannot be verified from the code. Code review only confirmed that these structures exist (Hexagonal + CQRS, signal/rule/risk/portfolio modules, an EventBuffer cache in the KDB and Woori `bond_algorithm`, per-tick/per-timer order snapshot caches in data management). Who did what comes from the user's own statements.
- Tradegene may be described (it is the company's public product, tradegene.co.kr). Customers appear only as initials, as in the CV; never add anything beyond what the CV already shows.
- The personal blog link was removed on purpose; do not add it back.
- Only include numbers the user can defend in an interview. The README currently carries "about 80% memory reduction" (the Redis event buffer in the in-house crypto trading project, not the bank projects) and "35% shorter Phase 2" unverified; the user will re-derive the quantitative results while writing the job application, so keep the README in sync with those final numbers. The CLS manual-work count is deliberately not in the README (the CV disagreed with itself, 10 vs 15 per day; 10, the smaller figure, was chosen provisionally and still has to be applied in Notion and confirmed by the user).
- Where the README and the CV could differ, the user's latest CV wins (decided 2026-11-17): Alloc is dated 2023.7~8, the Modu LLM bootcamp is shown as a single project (the national-bond-market access-infrastructure document RAG), and the data (custom) management sub-responsibility is deliberately left out of both.
- Team projects (SOSOBUTSTRONG) must state the user's own responsibilities rather than the whole project's.
- Section order is intentional: Experience, then Web channel experience (Spring MVC/MyBatis/JSP/AJAX projects), then backend design/operations (inner-orbit, song-lingo, RAG), then awards/certifications, then badges and contact. This matches the Web/WTS channel developer posting the page is tailored to.
