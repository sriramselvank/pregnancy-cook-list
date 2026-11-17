# Pregnancy Cook List — installable app (PWA)

A home-screen app for Android **and** iPhone that shows what to cook today
(with a refresh button) and a full week where each day is varied from the last —
all pregnancy-safe, liver-free. Works offline once installed.

## What's in this folder
```
PregnancyCookApp/
├─ index.html              ← the app
├─ manifest.webmanifest    ← app name, icons, standalone mode
├─ service-worker.js       ← offline support
├─ icons/                  ← app icons (Android, iOS, favicon)
└─ README.md               ← this file
```

---

## Step 1 — Put it online (one time, ~2 minutes, free)

A phone can only install it from an **https://** web address, so the folder
needs to be hosted. Pick ONE:

### Option A — Netlify Drop (easiest, no account needed to try)
1. Go to **https://app.netlify.com/drop**
2. Drag the **whole `PregnancyCookApp` folder** onto the page.
3. It gives you a link like `https://something.netlify.app` — that's your app.
   (Create a free account to keep the link permanently.)

### Option B — GitHub Pages (free, permanent)
1. Create a free GitHub account, make a new **public** repository.
2. Upload all files from this folder (keep the `icons` folder inside).
3. Repo **Settings → Pages →** Branch: `main`, Folder: `/root` → Save.
4. Your app appears at `https://<username>.github.io/<repo>/`.

> Tip: whichever you pick, open the link once on a computer first to check it loads.

---

## Step 2 — Install on the phone

### iPhone / iPad (use Safari — this only works in Safari)
1. Open the app link in **Safari**.
2. Tap the **Share** button (square with an up-arrow).
3. Scroll down → **Add to Home Screen** → **Add**.
4. The green plate icon appears on the home screen and opens fullscreen, like an app.

### Android (use Chrome)
1. Open the app link in **Chrome**.
2. Either tap the **"Install app" / "Add to Home screen"** banner that pops up,
   or tap the **⋮ menu → Install app / Add to Home screen**.
3. Confirm — the icon lands on the home screen and opens as a standalone app.

That's it. After the first open it works **offline**, and each person's plan +
today's check-offs are saved on their own phone.

---

## Updating the app later
If I change `index.html`, re-upload the folder to the same host and bump the
`CACHE` name in `service-worker.js` (e.g. `preg-cooklist-v5` → `v6`). Phones
pick up the new version next time they open it online.

## Notes
- This is a general nutrition helper, **not medical advice** — the doctor should
  confirm anything specific to the pregnancy.
- No app-store submission is needed for this install method. If you later want it
  on the Google Play / Apple App Store, that's a separate build (Expo/Capacitor) —
  just ask.
