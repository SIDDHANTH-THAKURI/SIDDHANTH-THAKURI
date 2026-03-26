# Setup Guide — Complete GitHub Profile

## Files in this package

```
SIDDHANTH-THAKURI/          ← your profile repo (must match your GitHub username exactly)
├── README.md               ← main profile
├── header.svg              ← animated header (self-hosted, never breaks)
└── .github/
    └── workflows/
        ├── snake.yml       ← contribution snake animation
        ├── waka.yml        ← WakaTime coding stats
        └── 3d-contrib.yml  ← 3D contribution graph
```

---

## Step 1 — Create the profile repo

Go to GitHub → New Repository
Name it exactly: `SIDDHANTH-THAKURI` (same as your username)
Make it Public
Check "Add a README file"

---

## Step 2 — Upload files

Upload `README.md`, `header.svg`, and the `.github/workflows/` folder to the repo root.

---

## Step 3 — Snake animation

No setup needed — just push the workflow file.
Go to Actions tab → "Generate Snake Animation" → Run workflow manually first.
After it runs, the snake SVG will appear at the output branch.

---

## Step 4 — WakaTime (coding time tracker)

1. Sign up free at https://wakatime.com
2. Install the WakaTime plugin in VS Code (Extensions → search WakaTime)
3. Paste your API key when prompted — it tracks silently from then on
4. Go to your GitHub profile repo → Settings → Secrets → Actions
5. Add secret: `WAKATIME_API_KEY` = your WakaTime API key
6. Add secret: `GH_TOKEN` = a GitHub Personal Access Token with `repo` scope
   (GitHub → Settings → Developer Settings → Personal Access Tokens → Classic)
7. Push the waka.yml workflow — it updates daily at midnight

---

## Step 5 — 3D Contribution Graph

No extra setup — uses your GITHUB_TOKEN automatically.
Go to Actions → "GitHub-Profile-3D-Contrib" → Run workflow manually first.
The graph SVG will be committed to your repo automatically.

---

## Step 6 — Update live links

Once ShiftMate and WAYA are live, replace the badge hrefs in README.md:

Find:
  `[![ShiftMate](https://img.shields.io/badge/Status-Active%20Build-brightgreen?style=for-the-badge)](https://github.com/SIDDHANTH-THAKURI)`

Replace with:
  `[![ShiftMate](https://img.shields.io/badge/Status-Live-brightgreen?style=for-the-badge)](https://YOUR-SHIFTMATE-URL)`

Same for WAYA.

---

## What auto-updates on schedule

| Feature | Frequency |
|---|---|
| Snake animation | Every 12 hours |
| WakaTime coding stats | Daily at midnight |
| 3D contribution graph | Daily at 6pm UTC |
