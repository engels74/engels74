# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

The remote is `engels74/engels74` — a GitHub profile repository, where the repo name matches the account name. `README.md` therefore renders directly on <https://github.com/engels74>, so every README change is immediately public-facing.

Tracked content is three files: `README.md`, `renovate.json`, and `LICENSE` (AGPL-3.0). There is no source code, package manifest, build step, test suite, linter, or CI workflow. Do not search for or invent project commands — validation here is reading the rendered Markdown, not running a toolchain.

## The Stats Images Are Generated Elsewhere

`README.md` embeds two SVGs served from a *different* repository, `engels74/github-stats`, branch `generated`:

- `https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg`
- `https://raw.githubusercontent.com/engels74/github-stats/generated/languages.svg`

Nothing in this repository produces, stores, or can alter those images. To change what the stats measure, how they are computed, or how they are styled, work in `engels74/github-stats`. Only the embedding markup is editable here.

## Image Embedding Pattern

Each stats image uses the same three-element `<picture>` block: a dark `<source>`, a light `<source>`, and an `<img>` fallback. Both theming mechanisms are applied together — the `media="(prefers-color-scheme: ...)"` attribute *and* a `#gh-dark-mode-only` / `#gh-light-mode-only` URL fragment. Reuse this exact shape when adding an image:

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-dark-mode-only">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-light-mode-only">
  <img alt="GitHub statistics overview" src="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-light-mode-only">
</picture>
```

Constraints, each removed deliberately in history — restoring them reverts an intentional decision:

| Rule | Evidence |
| --- | --- |
| Render images bare; do not wrap them in anchor tags | `5a029ba` "Render stats images without links" |
| Do not add attribution text beneath the stats | `6300e83` "Remove stats attribution from profile README" |
| Use `raw.githubusercontent.com`, never a `github.com/.../blob/...` URL | current markup in `README.md` |
| Give the `<img>` fallback the light-mode fragment | current markup in `README.md` |

## renovate.json Is Fleet Policy

`renovate.json` is a shared standard applied across the owner's repositories, not per-repo tuning — see commit `e72eed8`, "chore(renovate): standardize fleet renovate policy". Change it only as part of a deliberate fleet-wide Renovate update; a local-only edit silently drifts this repo away from the rest of the fleet.

The `gitIgnoredAuthors` entries (`github-actions[bot]`, `engels74-bot`) exist so Renovate resumes auto-rebasing after those bots push fix commits. Because the repository has no dependency manifests, Renovate has nothing to update here — an untouched `renovate.json` is the expected steady state.

## Commit Messages

Do not infer the convention from `git log`: four of the five commits predate the current standard and use plain imperative subjects. Follow Conventional Commits, as the most recent commit (`e72eed8`) does.
