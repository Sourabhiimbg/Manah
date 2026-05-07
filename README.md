# 🎬 DriveFlix

A Netflix-style video streaming interface for your Google Drive library. Browse and play your videos with a beautiful, dark cinema UI — no backend needed.

---

## ✨ Features

- 🎨 **Netflix-style UI** — dark theme, hero banner, horizontal scroll rows, hover cards
- 📁 **Folder-based organisation** — videos grouped by Drive folder into separate rows
- 🔍 **Search** — filter videos by name instantly
- 🖼️ **Auto thumbnails** — uses Google Drive's built-in video thumbnails
- 🎬 **Smart titles** — strips file extensions and quality tags (720p, x264, etc.)
- 📱 **Responsive** — works on mobile and desktop
- 💾 **Saves config** — API key and folder ID stored in localStorage
- 🎭 **Demo mode** — try the UI without a Google account

---

## 🚀 Deploy to GitHub Pages

### Step 1 — Push to GitHub

```bash
git init
git add index.html README.md
git commit -m "Initial DriveFlix"
git remote add origin https://github.com/YOUR_USERNAME/driveflix.git
git push -u origin main
```

### Step 2 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` → folder: `/ (root)`
4. Click **Save**

Your site will be live at: `https://YOUR_USERNAME.github.io/driveflix`

---

## 🔑 Google Drive API Setup

### 1. Create a Google Cloud Project

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a new project (e.g. "DriveFlix")
3. Enable **Google Drive API** (APIs & Services → Library → search "Drive API")

### 2. Create an API Key

1. APIs & Services → **Credentials** → Create Credentials → **API Key**
2. Click **Restrict Key**:
   - API restrictions → **Google Drive API**
   - (Optional) HTTP referrer restriction → add your GitHub Pages URL

### 3. Share Your Drive Folder

- Right-click the folder in Google Drive
- Share → change to **"Anyone with the link"** (Viewer)
- Copy the **Folder ID** from the URL:
  ```
  drive.google.com/drive/folders/[THIS-IS-YOUR-FOLDER-ID]
  ```

### 4. Enter Credentials in DriveFlix

Click **⚙ Configure** and enter:
- API Key
- Folder ID
- Library Name

---

## 📂 Supported Video Formats

- MP4, MKV, AVI, MOV, WEBM, MPEG, 3GP

---

## 🛡️ Privacy Notes

- Your API key is stored only in your browser's `localStorage` — never sent anywhere except Google's API
- The app is purely client-side — no server, no tracking
- To restrict API key usage, add your GitHub Pages URL as an HTTP referrer in Google Cloud Console

---

## 🗂️ Folder Structure Tip

Organise your Drive folder like this for best results:

```
📁 My Videos (Folder ID you enter)
  📁 Movies
  📁 Series
  📁 Documentaries
  📁 Shorts
```

Each sub-folder becomes a separate row in DriveFlix.

---

## License

MIT — free to use and modify.
