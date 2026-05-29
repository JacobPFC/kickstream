[README.md](https://github.com/user-attachments/files/28393666/README.md)
# ⚡ KickStream

> A self-hosted sports & movies streaming hub — two standalone pages, one repo.

![Status](https://img.shields.io/badge/status-active-00e676?style=flat-square)
![HTML](https://img.shields.io/badge/built%20with-HTML%2FJS-00b0ff?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)

---

## 📁 What's in this repo

| File | Purpose |
|---|---|
| `index.html` | 🏟️ **KickStream Sports** — live sports streams |
| `movies.html` | 🎬 **KickStream Movies** — movies & TV on demand |

These are two completely separate tools that share a brand. No framework, no build step — just open the HTML file in a browser or host it anywhere static.

---

## 🏟️ KickStream Sports (`index.html`)

Live sports streaming aggregator pulling real-time match data from an API backend.

**Features:**
- 🔴 Live, Today, and Upcoming match filters
- ⚽ Sport & league sidebar with live match counts
- 🖥️ In-page embedded stream player with automatic stream failover
- ⊞ **Multistream** — watch up to 4 matches side-by-side
- 🎉 **Watch Party** — sync playback with friends via a shared party code (powered by Ably)
- ⭐ Favourite teams — pinned to the top and highlighted across all views
- 📺 Live TV channels with HLS playback (via hls.js)
- 🔍 Real-time search across all matches
- 📱 Fully mobile-responsive with iOS PWA support

**Sports covered:**
Football · Basketball · Tennis · American Football · Baseball · Hockey · MMA · Cricket · Rugby · F1 · Golf · and more

---

## 🎬 KickStream Movies (`movies.html`)

On-demand movies & TV shows powered by the TMDB API, with multi-source embedded playback.

**Features:**
- 🔥 Trending, Top Rated, and New Releases rows on the home screen
- 🎭 Browse by genre (Action, Comedy, Horror, Sci-Fi, Drama, Crime, and more)
- 🔍 Search with live autocomplete across movies & TV shows
- ▶️ Multi-source player (8 stream sources with one-click switching)
- 📺 TV show episode browser with season selector and auto-next episode
- ⬇️ **Download modal** with live YTS API torrent results + fallback sources
- 🕐 Continue Watching & Recently Watched history
- 🔞 NSFW filter toggle (excludes adult content from all results and search)
- 🎬 Trailer viewer (YouTube embed)
- 🎨 6 themes: Default · Coastal · Forest · Minimalist · Sunset · Winter
- 📱 Mobile-first with overlay search and touch-optimised controls
- ♾️ Infinite scroll with a range of decade, rating, and mood filters

---

## 🚀 Usage

No install required. Just serve the files statically — GitHub Pages, Netlify, Cloudflare Pages, or a plain web server all work.

```bash
# Quick local preview (Python)
python -m http.server 8080
# Then open http://localhost:8080
```

For GitHub Pages, enable it on the `main` branch root and your pages will be live at:

```
https://<your-username>.github.io/<repo-name>/          # Sports
https://<your-username>.github.io/<repo-name>/movies    # Movies
```

---

## 🔑 API Keys

| Service | Used in | Notes |
|---|---|---|
| [TMDB](https://www.themoviedb.org/settings/api) | `movies.html` | Free — required for all movie/TV data |
| [Ably](https://ably.com) | `index.html` | Free tier — used for Watch Party sync |
| YTS API | `movies.html` | Public, no key needed |

Replace the key constants near the top of each file:

```js
// movies.html
const TMDB_KEY = 'your_tmdb_key_here';

// index.html — Ably key is loaded via their CDN
```

---

## ⚠️ Disclaimer

KickStream does not host or store any media files. All streams and content are linked from third-party sources. Use a VPN if streams are geo-restricted in your region. This project is intended for personal and educational use only.

---

## 🤝 Community

[![Discord](https://img.shields.io/badge/Join%20Discord-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/ZnpTZE4jMu)
