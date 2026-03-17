# Get Fit — Deploy Instructions

## Files in this folder
- `index.html` — the full app
- `manifest.json` — makes it installable as a PWA
- `sw.js` — service worker (enables offline use)
- `icon-192.png` / `icon-512.png` — add your own app icons (optional but nice)

---

## Option 1: GitHub Pages (Free forever, easiest)

1. Go to github.com and create a free account
2. Click "New repository" → name it `getfit` → set to Public → click Create
3. Click "uploading an existing file"
4. Drag all 3 files (index.html, manifest.json, sw.js) into the uploader
5. Click "Commit changes"
6. Go to Settings → Pages → under "Source" select "Deploy from a branch" → pick `main` → click Save
7. Wait ~60 seconds → your app is live at: `https://YOUR-USERNAME.github.io/getfit`

Share that link with your friends. On iPhone, they open it in Safari → tap the Share button → "Add to Home Screen" → Done. It installs like a real app.

---

## Option 2: Vercel (Free, very fast)

1. Go to vercel.com → create a free account
2. Click "Add New Project" → choose "Deploy without Git"
3. Drag your getfit folder into the upload zone
4. Click Deploy
5. Done — you get a URL like `getfit.vercel.app`

---

## Option 3: Cloudflare Pages (Free, unlimited bandwidth)

1. Go to pages.cloudflare.com → create a free account
2. Click "Create a project" → "Direct Upload"
3. Upload your getfit folder
4. Click Deploy
5. Done — you get a URL like `getfit.pages.dev`

---

## Option 4: Render (Free)

1. Go to render.com → create a free account
2. New → Static Site
3. Connect GitHub (upload files there first) or use manual deploy
4. Done

---

## Adding real icons (optional)

Replace icon-192.png and icon-512.png with your own PNG images at those exact sizes.
You can make a simple one at: https://favicon.io/favicon-generator/
Use "G" as the letter, background color #7c6fff, and download the PNG files.

---

## Important note about data storage

Get Fit stores all data in localStorage on each device/browser. This means:
- Each person's data lives on THEIR device
- The leaderboard shows everyone who has created an account on that same device/browser
- For true cross-device squad leaderboards, you'd need a backend (e.g. Supabase free tier)

For a small friend group using the same shared link on their own phones, the simplest setup is:
everyone creates their account on their own device — the leaderboard will sync once you add a backend.
