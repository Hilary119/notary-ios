# NY Notary Study Aid — iOS (Capacitor 8)

A offline study app for the New York Notary Public License Law, wrapped as a native iOS app using Capacitor 8.

- **App name:** NY Notary Study Aid
- **Bundle ID:** `com.duoduo.notarystudy` (change to your own in `capacitor.config.json`)
- **Requires:** Xcode 26+, Node.js 22+, Apple Developer account
- **No CocoaPods needed** — Capacitor 8 uses Swift Package Manager

---

## Quick Start

```bash
npm install
npx cap add ios
npx cap sync
npx cap open ios   # then pick a Simulator and press ▶ Run
```

---

## App Icon

Create your own 1024×1024 PNG icon and name it `icon-only.png`, place it in the `assets/` folder, then:

```bash
npx @capacitor/assets generate --ios
npx cap sync
```

---

## Adding Questions

Open `www/index.html` and find the `QUESTIONS` array. Each question follows this format:

```js
{
  t: "Topic",
  q: "Question text",
  o: ["Option A", "Option B", "Option C", "Option D"],
  a: 0,   // index of the correct answer (0–3)
  e: "Explanation shown after answering"
}
```

---

## Updating the App

1. Edit `www/index.html`
2. `npx cap sync`
3. Re-run or re-archive in Xcode (bump the version/build number for a new submission)
