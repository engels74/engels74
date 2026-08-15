# Hi, I'm @engels74 👋

Self-hosted tools for Plex and the \*arr stack, plus Homebrew taps and Docker images.

## Released

| Project | What it is | Docker |
| --- | --- | --- |
| [EasyHDR](https://github.com/engels74/EasyHDR) | Windows tray app. Turns HDR on when a configured app starts, and off when it closes | — |
| [mover-status](https://github.com/engels74/mover-status) | One Bash script for Unraid. Posts mover progress to Discord or Telegram while the cache drains | [mover-status-docker](https://github.com/engels74/mover-status-docker) |
| [obzorarr](https://github.com/engels74/obzorarr) | Year in review for Plex — "Spotify Wrapped", as a story-mode slideshow or a scrollable recap. Reads the Plex API, no Tautulli | [obzorarr-docker](https://github.com/engels74/obzorarr-docker) |
| [wings-vpn](https://github.com/engels74/wings-vpn) | Fork of Pelican's Wings. Adds `docker.network.network_mode`, so game servers share another container's network namespace — a VPN, for example | — |

## Functional, but WIP

Expect breaking changes.

| Project | What it is | Docker |
| --- | --- | --- |
| [otpravkarr](https://github.com/engels74/otpravkarr) | Provisions Plex users into [Dispatcharr](https://github.com/Dispatcharr/Dispatcharr) and serves each user their own IPTV credentials and playlist | [otpravkarr-docker](https://github.com/engels74/otpravkarr-docker) (`:nightly`) |
| [zondarr](https://github.com/engels74/zondarr) | Invite and user manager for Plex and Jellyfin, an alternative to Wizarr. Wizard steps around the invite: clicks, timers, ToS, text input, quizzes | [zondarr-docker](https://github.com/engels74/zondarr-docker) |

## WIP, not yet functional

| Project | What it is |
| --- | --- |
| [afisharr](https://github.com/engels74/afisharr) | Plex collections, posters, and overlays. One Rust binary with the web UI embedded |
| [comradarr](https://github.com/engels74/comradarr) | Finds missing or upgradeable content across Sonarr, Radarr, and Whisparr, then requests it |
| [zimuarr](https://github.com/engels74/zimuarr) | Subtitle translation for Bazarr. A translation is provably complete, or it did not happen |

## Homebrew taps

A workflow checks upstream every 6 hours, re-hosts the release here, updates the cask, and appends a VirusTotal report.

```bash
brew install --cask engels74/<tap>/<app>
```

| Tap | Installs |
| --- | --- |
| [homebrew-fcast-sender](https://github.com/engels74/homebrew-fcast-sender) | [FCast Sender](https://fcast.org/) — cast video and audio to any FCast receiver |
| [homebrew-flixor](https://github.com/engels74/homebrew-flixor) | [Flixor](https://github.com/Flixorui/flixor) — Plex client with a Netflix-like UI |
| [homebrew-fredtv](https://github.com/engels74/homebrew-fredtv) | [Fred TV](https://github.com/Fredolx/open-tv) — IPTV app, formerly Open TV |
| [homebrew-paicord](https://github.com/engels74/homebrew-paicord) | [Paicord](https://github.com/llsc12/Paicord) — native macOS Discord client |
| [homebrew-qview](https://github.com/engels74/homebrew-qview) | [qView](https://github.com/jurplel/qView) — minimal image viewer |

## Docker images

Forks of [hotio](https://github.com/hotio)'s images, with extra features.

```bash
docker pull ghcr.io/engels74/<image>
```

| Image | Difference from upstream |
| --- | --- |
| [base-image](https://github.com/engels74/base-image) | s6-overlay and VPN base for the images below, synced from `hotio/base` |
| [qbittorrent](https://github.com/engels74/qbittorrent) | libtorrent v2 by default, plus the themes hotio dropped (VueTorrent) |
| [qflood](https://github.com/engels74/qflood) | jesec's flood + qBittorrent, libtorrent v2 by default. hotio archived his |
| [sabnzbd](https://github.com/engels74/sabnzbd) | SABnzbd with `ffprobe`, for post-processing scripts |

## GitHub stats

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-dark-mode-only">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-light-mode-only">
  <img alt="GitHub statistics overview" src="https://raw.githubusercontent.com/engels74/github-stats/generated/overview.svg#gh-light-mode-only">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/languages.svg#gh-dark-mode-only">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/engels74/github-stats/generated/languages.svg#gh-light-mode-only">
  <img alt="GitHub language statistics" src="https://raw.githubusercontent.com/engels74/github-stats/generated/languages.svg#gh-light-mode-only">
</picture>

---

<sub>Last edited: 2026-08-15</sub>
