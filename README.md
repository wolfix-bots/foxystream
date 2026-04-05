# 🦊 FoxyStream — Render Deploy

> **Production-ready static build** of FoxyStream. Deploy this repo directly on Render — no build step required.

## What is this?
This is the pre-compiled `dist/` output of [cyber-stream-foxy](https://github.com/wolfix-bots/cyber-stream-foxy) served by a lightweight Express server (`server.mjs`).

## Deploy on Render (Web Service)

| Setting | Value |
|---|---|
| **Build Command** | `yarn` |
| **Start Command** | `yarn start` |
| **Node Version** | 18+ |
| **Environment** | `PORT` is set automatically by Render |

> No additional env vars required. The app calls xcasper directly from the browser.

## Update the Build
When [cyber-stream-foxy](https://github.com/wolfix-bots/cyber-stream-foxy) has new changes:
```bash
cd cyber-stream-foxy && npm run build
cp -r dist/ ../foxystream/dist/
cd ../foxystream && git add dist/ && git commit -m "rebuild" && git push
```

---
**Maintained by Foxy Tech** · Powered by Casper Tech Kenya
