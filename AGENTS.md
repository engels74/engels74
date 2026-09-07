# AGENTS.md

This file provides guidance to AI coding agents when working with code in this
repository.

## What this repository is

The remote is `engels74/engels74` — a GitHub profile repository, so `README.md`
renders directly on <https://github.com/engels74>. Every README change is
immediately public-facing.

Content is Markdown and the AGPL-3.0 license. There is no application build or
runtime test suite. [CI.md](CI.md) documents the read-only prek validation,
shared CI gate and Renovate policy for workflow and hook dependencies.

## The stats images live in another repository

`README.md` embeds two SVGs served from `engels74/github-stats`, branch
`generated`:

- `.../github-stats/generated/overview.svg`
- `.../github-stats/generated/languages.svg`

Nothing here produces, stores, or can alter them. To change what the stats
measure or how they are styled, work in `engels74/github-stats`; only the
embedding markup is editable here.

### Embedding rules

Copy the existing `<picture>` block in `README.md` rather than writing fresh
markup when adding an image. It applies both theming mechanisms together — the
`media="(prefers-color-scheme: ...)"` attribute *and* a `#gh-dark-mode-only` /
`#gh-light-mode-only` URL fragment — and gives the `<img>` fallback the
light-mode fragment.

Source images from `raw.githubusercontent.com`, never a `github.com/.../blob/...`
URL, which serves an HTML page instead of the image.

Two constraints were each removed deliberately; restoring them reverts an
intentional decision:

- Render the stats images bare — no wrapping anchor tags (`5a029ba`)
- No attribution text beneath the stats (`6300e83`)

## Editing README.md

The footer `<sub>Last edited: YYYY-MM-DD</sub>` is maintained by hand. Bump it
to the current date in the same commit as any README content change — nothing
enforces it.

## renovate.json is fleet policy

`renovate.json` is a shared standard applied across the owner's repositories
(`e72eed8`, "chore(renovate): standardize fleet renovate policy"), not per-repo
tuning. Change it only as part of a deliberate fleet-wide update; a local-only
edit silently drifts this repo away from the rest of the fleet.

Renovate updates CI action versions and prek hook revisions through the shared
versioned preset. It does not regenerate the profile stats images.
