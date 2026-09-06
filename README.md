# Hi, I'm @engels74 👋

Self-hosted tools for Plex and the \*arr stack, plus Homebrew taps and Docker images.

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

## Released

| Project | What it is | Docker |
| --- | --- | --- |
| [EasyHDR](https://github.com/engels74/EasyHDR) | Windows tray app. Turns HDR on when a configured app starts, and off when it closes | — |
| [mover-status](https://github.com/engels74/mover-status) | One Bash script for Unraid. Posts mover progress to Discord or Telegram while the cache drains | — |
| [obzorarr](https://github.com/engels74/obzorarr) | Year in review for Plex — "Spotify Wrapped", as a story-mode slideshow or a scrollable recap. Reads the Plex API, no Tautulli | [obzorarr-docker](https://github.com/engels74/obzorarr-docker) |
| [wings-vpn](https://github.com/engels74/wings-vpn) | Fork of Pelican's Wings. Adds `docker.network.network_mode`, so game servers share another container's network namespace — a VPN, for example | — |

## Functional, but WIP

Expect breaking changes.

| Project | What it is | Docker |
| --- | --- | --- |
| [otpravkarr](https://github.com/engels74/otpravkarr) | Provisions Plex users into [Dispatcharr](https://github.com/Dispatcharr/Dispatcharr) and serves each user their own IPTV credentials and playlist | [otpravkarr-docker](https://github.com/engels74/otpravkarr-docker) |
| [zondarr](https://github.com/engels74/zondarr) | Invite and user manager for Plex and Jellyfin, an alternative to Wizarr. Wizard steps around the invite: clicks, timers, ToS, text input, quizzes | [zondarr-docker](https://github.com/engels74/zondarr-docker) |

## WIP, not yet functional

| Project | What it is |
| --- | --- |
| [afisharr](https://github.com/engels74/afisharr) | Plex collections, posters, and overlays. One Rust binary with the web UI embedded |
| [comradarr](https://github.com/engels74/comradarr) | Finds missing or upgradeable content across Sonarr, Radarr, and Whisparr, then requests it |
| [zimuarr](https://github.com/engels74/zimuarr) | Subtitle translation for Bazarr. A translation is provably complete, or it did not happen |

## Homebrew taps

One tap, [homebrew-taps](https://github.com/engels74/homebrew-taps), for macOS apps that homebrew-cask does not carry. A workflow checks upstream every 6 hours, re-hosts the release there, updates the cask, and appends a VirusTotal report.

| App | Install |
| --- | --- |
| [FCast Sender](https://fcast.org/) | `brew install --cask engels74/taps/fcast-sender` |
| [Flixor](https://github.com/Flixorui/flixor) | `brew install --cask engels74/taps/flixor` |
| [Fred TV](https://github.com/Fredolx/open-tv) | `brew install --cask engels74/taps/fredtv` |
| [Paicord](https://github.com/llsc12/Paicord) | `brew install --cask engels74/taps/paicord` |
| [qView](https://github.com/jurplel/qView) | `brew install --cask engels74/taps/qview` |

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

---

<sub>Last edited: 2026-09-06</sub>
