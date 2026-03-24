# 📊 Ibbani · Data Analyst Journey — v3.0 (2026 Edition)

A complete personal learning + progress tracker for your Data Analyst career journey.
Works fully offline. Saves all data on your device. Installable as an Android/iOS PWA.

---

## 🚀 What's New in v3.0

### Features Added
| Feature | v1 (Before) | v3 (After) |
|---|---|---|
| PIN Lock | ❌ None | ✅ Full 4-digit PIN system |
| Topics | 68 topics | 91 topics (more depth) |
| Navigation tabs | 5 | 7 (added Projects + Interview) |
| Projects section | Inside roadmap | ✅ Dedicated Projects page (9 projects) |
| Interview section | Mixed in Job Plan | ✅ Dedicated Interview page |
| SQL Drills | 10 questions | 20 real interview questions |
| Case Studies | ❌ None | ✅ 5 business case studies with hints |
| Interview Tips | ❌ None | ✅ 8 structured tips |
| Portfolio Guide | ❌ None | ✅ 5-step portfolio building guide |
| GitHub Tips | ❌ None | ✅ 4 GitHub career tips |
| XP System | ❌ None | ✅ Full XP tracking system |
| Progress Arc | ❌ None | ✅ Animated circular progress |
| Dark Theme | ❌ Light only | ✅ Professional dark theme |
| Offline Support | Partial | ✅ Full (all assets cached) |
| Settings page | Static | ✅ Editable name, PIN change |
| Data migration | ❌ | ✅ Auto-migrates v1 data |

---

## 📁 Files

```
ibbani-upgraded/
├── index.html      ← Main app (single file, all-in-one)
├── sw.js           ← Service Worker (offline caching)
├── manifest.json   ← PWA manifest (for install)
└── README.md       ← This file
```

> **Note:** You'll need to add icon-192.png and icon-512.png for the full PWA install experience.

---

## 🏃 How to Run

### Option 1: Direct browser (easiest)
1. Open `index.html` directly in Chrome/Safari/Firefox
2. Set your PIN when prompted
3. Start using!

### Option 2: Local server (recommended for PWA features)
```bash
# Using Python
cd ibbani-upgraded
python3 -m http.server 8080

# Then open: http://localhost:8080
```

### Option 3: VS Code Live Server
- Install "Live Server" extension
- Right-click `index.html` → "Open with Live Server"

---

## 📱 Convert to Android APK

### Method 1: PWABuilder (Easiest — Free)
1. Host the folder on GitHub Pages or Netlify (free)
2. Go to https://www.pwabuilder.com
3. Enter your site URL
4. Click "Build My PWA" → Download Android APK
5. Install the APK on your phone

### Method 2: GitHub Pages (Free Hosting)
1. Create a new GitHub repo
2. Upload these 4 files
3. Go to Settings → Pages → Enable GitHub Pages
4. Your app is live at: `https://yourusername.github.io/repo-name`

### Method 3: Netlify Drop (Instant)
1. Go to https://netlify.com/drop
2. Drag and drop the `ibbani-upgraded` folder
3. Get a live URL instantly (free)

---

## 🔐 PIN System

- **First launch:** You'll be asked to set a 4-digit PIN
- **Every launch:** Enter PIN to access your data
- **Forgot PIN?** Tap "Forgot PIN?" on the lock screen — it resets your PIN but keeps all progress
- **Change PIN:** Settings → Security → Change PIN

---

## 💾 Data Storage

All data is stored in your browser's `localStorage` under key `ibbani_da_v3`.

**What's saved:**
- Topic completion status (done / missed / cleared)
- Skill self-ratings (1-5 stars)
- Job plan task completion
- SQL drills solved
- Study streak + study days
- XP points
- Your name + PIN

---

## 📊 Roadmap Overview

| Level | Topic | Weeks | Topics | XP |
|---|---|---|---|---|
| 1 | Excel & Spreadsheets | 1–2 | 10 | 80 |
| 2 | SQL | 3–6 | 12 | 120 |
| 3 | Python + Pandas | 7–10 | 12 | 150 |
| 4 | Statistics | 11–12 | 10 | 100 |
| 5 | Power BI / Dashboards | 13–15 | 10 | 130 |
| 6 | ML Basics + AI Tools | 16–18 | 12 | 140 |
| 7 | Get the Job | 19–24 | 12 | 200 |
| **Total** | | **24 weeks** | **78 topics** | **920 XP** |

---

## 🎯 Target: ₹10L+ Data Analyst in 6 months

Made with ❤️ for Ibbani · 2026 Edition
