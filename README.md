# DAYBOOK MAX — PWA Deployment Guide

## 📁 Files Needed in Your GitHub Repo Root
```
index.html
manifest.json
sw.js
icon.svg
```

---

## 🌐 Deploy to GitHub Pages (Free Hosting)

1. Create a **public** GitHub repository (e.g. `daybook-max`)
2. Upload all 4 files to the root of the `main` branch
3. Go to **Settings → Pages → Source → Deploy from branch → main / root**
4. Your PWA URL will be: `https://YOUR_USERNAME.github.io/daybook-max/`

> ⚠️ HTTPS is required for PWA install banners — GitHub Pages provides this automatically.

---

## 📲 Install as PWA (Add to Home Screen)

### Android (Chrome)
1. Open the GitHub Pages URL in Chrome
2. Tap the **3-dot menu → "Add to Home screen"** or wait for the install banner to appear automatically
3. Tap **Install** — the app icon appears on your home screen

### iOS (Safari)
1. Open the URL in Safari
2. Tap the **Share button (box with arrow)**
3. Scroll down → **"Add to Home Screen"**
4. Tap **Add**

---

## 📦 Convert to APK (Android App)

### Option A — PWA2APK (Easiest, Free)
1. Go to https://www.pwa2apk.com
2. Enter your GitHub Pages URL
3. Download the generated APK
4. Install on Android (enable "Install from unknown sources" in settings)

### Option B — Bubblewrap (Google's Official Tool)
1. Install Node.js
2. `npm i -g @bubblewrap/cli`
3. `bubblewrap init --manifest https://YOUR_USERNAME.github.io/daybook-max/manifest.json`
4. `bubblewrap build`
5. This creates a signed APK/AAB ready for Play Store

### Option C — PWABuilder (Microsoft, Recommended)
1. Go to https://www.pwabuilder.com
2. Enter your GitHub Pages URL
3. Click **Build My PWA → Android**
4. Download and sign the APK

---

## ✅ Checklist Before Deploying
- [ ] All 4 files are in repo root
- [ ] Repo is **public**
- [ ] GitHub Pages is enabled
- [ ] Test URL in Chrome mobile — install banner should appear

---

## 🔧 Updating the App
Just push updated `index.html` to GitHub — the service worker will automatically update on next app launch.
