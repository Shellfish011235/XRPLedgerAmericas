# XRPLedgerAmericas — Standalone Project

This folder is the **separate** XRPLedgerAmericas project:

- **Local:** `C:\Users\anamb\XRPLedgerAmericas` (not inside xrpl-control-room-gamer-ui)
- **GitHub:** [Shellfish011235/XRPLedgerAmericas](https://github.com/Shellfish011235/XRPLedgerAmericas)
- **Vercel:** Create a new project and import the GitHub repo above

## First-time push to GitHub

```powershell
cd C:\Users\anamb\XRPLedgerAmericas

# If you haven't set Git identity yet:
# git config --global user.email "your@email.com"
# git config --global user.name "Your Name"

git commit -m "Initial XRPLedgerAmericas site"
git branch -M main
git push -u origin main
```

## Deploy on Vercel

1. [vercel.com](https://vercel.com) → **Add New** → **Project**
2. **Import** → **Shellfish011235/XRPLedgerAmericas**
3. Deploy (Framework: Other, root: `./`)
4. Add domain **www.xrpledgeramericas.com** in Project Settings → Domains

See **DEPLOY.md** for domain DNS steps.
