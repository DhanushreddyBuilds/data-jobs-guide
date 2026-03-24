# Ibbani DA App — v5 Changes (Fixes Applied)

## Bugs Fixed

### 🔴 CRITICAL — Roadmap page blank on navigation
- `showPage('roadmap')` was missing `renderRoadmap()` call
- Clicking the Roadmap nav tab showed a blank page every time
- **Fixed:** Added `if (name === 'roadmap') renderRoadmap()` to routing function

### 🔴 PIN Security — No brute-force protection
- Infinite wrong PIN attempts were allowed with no consequences
- "Forgot PIN" was a single confirm() dialog — trivially bypassable
- **Fixed:** 5-attempt limit → 30-second lockout with live countdown timer
- **Fixed:** `pinForgot` now requires typing your name to verify identity
- **Fixed:** `pinInput` blocks all digit input during lockout period

### 🟡 Storage Key Mismatch
- App was v4 but storage key was `ibbani_da_v3`
- **Fixed:** Bumped to `ibbani_da_v4`
- **Fixed:** Migration now copies all fields from v3 → v4 with zero data loss

### 🟡 Service Worker Cache Stale
- SW cache was `ibbani-da-v3` — old installs kept serving stale files
- `sw.js` itself was not being cached (invisible update problem)
- **Fixed:** Cache bumped to `ibbani-da-v4` and `ibbani-fonts-v2`
- **Fixed:** `sw.js` added to CORE_ASSETS so it caches itself
- **Fixed:** Fonts pre-cached at install time, not just on first visit
- **Fixed:** Background cache refresh (stale-while-revalidate for local assets)

## Features Improved

### ✅ Guided Learning — "Start Here" Banner
- First-time users (0 topics done) now see a 5-step onboarding card
- Clear instructions: Roadmap → Expand Level → Do Tasks → Mark Done → Build Project
- Dismissable with ✕ button, hides automatically once you start learning

### ✅ Roadmap — Progression Path Banner
- Beginner → Intermediate → Advanced → Job-Ready phases shown at top
- Topic counter "X/67 topics done" visible at all times
- "How to use" instructions always visible for new users

### ✅ Roadmap — Topic Numbering & Job-Relevance Tags
- Topics now show sequential numbers (1, 2, 3...)
- Key high-value topics tagged: "🔥 Top Interview Topic", "✅ Core Daily Tool", etc.
- Subtask header renamed to "PRACTICAL TASKS — Do these hands-on" for clarity

## How to Test

| Fix | How to verify |
|-----|---------------|
| Roadmap nav bug | Click 🗺️ roadmap tab — content must render immediately |
| PIN lockout | Enter wrong PIN 5 times → 30s countdown appears |
| PIN forgot | Click "Forgot PIN" → must type your name correctly |
| First-time banner | Clear localStorage → reload → orange "Start Here" card appears |
| Progression bar | Open Roadmap tab → Beginner/Intermediate/Advanced/Job-Ready bar at top |
| Data migration | If you had v3 data, it loads automatically with no data loss |
| Offline | DevTools → Network → Offline → reload → full app works |
