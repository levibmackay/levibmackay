# Changelog

## 2026-07-17
- Fixed the broken streak-stats widget: the public streak-stats.demolab.com endpoint hit a GitHub API rate limit, and GitHub's image proxy (camo) cached that failure for 24h, so the widget kept showing an error long after the underlying service recovered.
- Replaced the remote widget with a GitHub Actions workflow (`.github/workflows/streak-stats.yml`) that renders the stats to a static `profile/streak.svg` on a daily schedule, using GitHub's built-in token. No more dependency on a shared third-party rate limit.

## 2026-07-16
- Fixed broken pinned-project links (Lydia → lydia-cli, NFCCard → nfc-card) and a dead portfolio URL.
- Corrected the Lydia project description to match what it actually is (a local AI coding agent with 30+ GitHub stars), gave it its own featured section with live stars/tests/language badges.
- Replaced the static banner.png and about_me.png screenshots with real markdown (typing-SVG header + text bullets) — theme-adaptive, accessible, and no longer dependent on baked images.
- Rewrote the "about" section to lead with shipped work and internship status instead of a generic bio.
- Removed now-unused assets/banner.png and assets/about_me.png.
- Routine maintenance and minor cleanup.
