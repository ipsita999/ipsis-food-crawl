# Ipsi's Birthday Food Crawl — Deploy Guide 🎀

This folder is a complete website with its OWN built-in group sync
(no third-party services, so ad blockers can't break it, and no room codes —
everyone who opens your site URL is automatically in the same group).

## What's inside
- index.html ............ the site
- netlify.toml .......... tells Netlify where the function lives
- netlify/functions/room.mjs ... tiny storage API (already bundled, zero setup)

## Deploy (~15 min, no terminal needed)

IMPORTANT: plain drag-and-drop will NOT deploy the sync function.
You must use the GitHub route (or Netlify CLI) — both are easy:

### Option A — GitHub (recommended, all in the browser)
1. Go to github.com → New repository → name it anything (e.g. ipsi-crawl) → Create.
2. On the empty repo page, click "uploading an existing file".
3. Drag ALL the contents of this folder in (index.html, netlify.toml,
   and the netlify folder — drag the folder itself so the structure is kept).
   Commit.
4. Go to app.netlify.com → Add new project → Import an existing project →
   GitHub → pick your repo → Deploy (no build settings needed — leave defaults).
5. Open your new site URL. The header should say "synced with the group 💞".
6. Text the URL to friends. That's it — no codes, no accounts.

(You can also point your existing site at the repo: Site settings →
Build & deploy → Link repository.)

### Option B — Netlify CLI (if you have Node installed)
    npm i -g netlify-cli
    netlify deploy --prod
    (run from inside this folder, pick/create your site)

## How you know it worked
Under the title, the status dot should be GREEN: "synced with the group 💞".
If it says "sync offline — site needs the full folder deploy", the function
didn't deploy (usually means drag-and-drop was used — use Option A).

## Fallback
Even with zero sync, everyone's phone saves their own ratings, and the
"📋 result codes" button lets you merge everyone's picks manually. The game
always works.
