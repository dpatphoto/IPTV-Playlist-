# UHF Free Legal IPTV – GitHub starter

This repository mirrors the live-TV playlist and XMLTV guide from the
`biskyt/legalFreeIPTVplaylist` project, which documents its stream-rights
checks and credits. It publishes two playlists:

- `all-live.m3u` – all accepted live channels
- `sports.m3u` – entries whose M3U `group-title` contains “Sports”
- `epg.xml.gz` – the matching XMLTV guide

The upstream project rebuilds daily. This repository refreshes daily too.

## Important limitations

- This includes only streams the upstream project accepts as legally free.
- It does **not** unlock ESPN, FOX cable/satellite feeds, TNT, or TBS.
- Sports channels may be free sports networks, sports news, or event channels;
  availability and live-event rights vary.
- EPG listings depend on upstream guide coverage. A channel without a matching
  `tvg-id`/listing may show no programme information.
- Do not use a VPN to bypass a service's geographic restrictions.

## Setup

1. Create a **public** GitHub repository (for example `uhf-free-iptv`).
2. Upload these files, preserving the `.github/workflows/` and `scripts/` paths.
3. In the repository, open **Settings → Pages** and set **Build and deployment**
   to **GitHub Actions**.
4. Open **Actions** and enable workflows if GitHub asks.
5. Run **Build UHF playlists** once manually from Actions → Build UHF playlists
   → Run workflow.
6. When the run finishes, GitHub Pages publishes the files.

## URLs for UHF

Replace `YOUR-USERNAME` with your GitHub username:

- All live: `https://YOUR-USERNAME.github.io/uhf-free-iptv/all-live.m3u`
- Sports only: `https://YOUR-USERNAME.github.io/uhf-free-iptv/sports.m3u`
- EPG: `https://YOUR-USERNAME.github.io/uhf-free-iptv/epg.xml.gz`

Use `sports.m3u` as a separate playlist in UHF if you want a sports-only view.
Use `all-live.m3u` for the full set. Both playlist headers point to the EPG
published by this repository.

## Refresh

The workflow runs daily at 06:20 UTC and can also be started manually.
