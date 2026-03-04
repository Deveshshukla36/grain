# GRAIN — Photography Community

> Minimal black & white photo sharing. Zero backend. Zero cost. Works forever.

**No Firebase. No accounts. No server. Just open and use.**

Photos and accounts are stored in your browser's built-in storage (IndexedDB + localStorage). The app works completely offline after the first load.

---

## ✦ Features

- **Sign up & Sign in** — local accounts, no email needed
- **Global Feed** — all photos in chronological order
- **Trending** — photos ranked by most likes
- **Like photos** — liked ones rise to Trending
- **Profile** — view your posted & liked photos, edit bio
- **Groups** — create collectives, invite members, post to group
- **Post photos** — from gallery or camera, add camera model + location
- **Photo viewer** — full details, camera info, like directly

---

## 🚀 Deploy to GitHub Pages in 3 Steps

### 1. Create a GitHub repository

- Go to [github.com](https://github.com) → **New repository**
- Name it `grain` (or anything)
- Set to **Public** → **Create repository**

### 2. Push this file

```bash
cd path/to/grain
git init
git add .
git commit -m "GRAIN launch"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/grain.git
git push -u origin main
```

### 3. Enable GitHub Pages

- In your repo → **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: `main` · Folder: `/ (root)`
- **Save**

**Your site will be live at:**
```
https://YOUR_USERNAME.github.io/grain/
```

That's it. Free forever. No expiry.

---

## 📦 How the Storage Works

| Data | Where stored |
|------|-------------|
| User accounts | `localStorage` |
| Photo metadata (caption, likes, etc.) | `localStorage` |
| Photo images | **IndexedDB** (browser database, handles large files) |
| Session | `localStorage` |

Images are automatically compressed to ~1200px before storing, so they don't eat up space.

**Note:** Since there's no central server, each person's data lives in their own browser. This is perfect for a personal gallery or a group of people on the same device. For a shared community across multiple devices, you'd need a backend (like Supabase — free tier available).

---

## 🗂 File Structure

```
grain/
├── index.html   ← Entire app (single file, no dependencies)
└── README.md    ← This file
```

---

*GRAIN — photography, simplified.*
