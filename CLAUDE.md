# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

This is the **GitHub special profile repository** for the user `MarcArmy2003` (Gillon Marchetti, founder of Veteran Analytics LLC). Because the repo name matches the username, `README.md` renders directly on the GitHub profile page at https://github.com/MarcArmy2003.

This is a **content-only repository** — there is no application code, build, lint, or test step. The two tracked content files are:

- `README.md` — the public GitHub profile card (bio + links to Veteran Analytics projects).
- `Privacy_Policy.md` — the privacy policy for **TERA Alignment GPT**, a custom GPT. This is published content that a hosted GPT links to; treat edits as legal/compliance-sensitive.

## Editing Notes

- **`Privacy_Policy` and `Privacy_Policy.md` are byte-for-byte identical** — the extensionless `Privacy_Policy` is a duplicate. Any edit to the policy must be applied to **both** files (or the duplicate removed) to avoid the two drifting. Prefer consolidating to the `.md` file unless the extensionless copy is a deliberate link target.
- The `Privacy_Policy.md` template still contains an unfilled placeholder: `[e.g., OpenAI/Google]`. Resolve it to the actual hosting platform before treating the policy as final.
- README links point to live production surfaces (`veterananalytics.com`, `app.veterananalytics.com/calculator`). Verify any URL change against the current platform routing — per the sister repos, product hosting moved across `veterananalytics.com` / `askvalor.ai` (see ADR-008 in `valor-core`), and the "VALOR AI" brand is under trademark review (S112).

## Relationship to Other Repos

This profile repo is part of the Veteran Analytics LLC workspace (sibling clones under the same parent directory):

- `valor-core` — data pipeline + ops, and the **cross-surface alignment authority** (session protocols, `state.json`, lessons log).
- `veteran-analytics` — the `valor-api` Flask app (serves `askvalor.ai` product + `veteranintel.org`).
- `valor-ai` — the `veterananalytics.com` corporate shingle (static site + redirect wrapper).

This repo is **not** part of the deploy pipeline and has no Cloud Run service. Changes here only affect the public GitHub profile and the linked GPT privacy policy.

## Commit Conventions

Match the workspace standard used across the sister repos:

- Git author: `Veteran Analytics LLC <gillon.marchetti@veterananalytics.com>`
- No `Co-Authored-By: Claude` trailers.
- Do not commit credentials or non-public infrastructure details (this repo's content is public).
