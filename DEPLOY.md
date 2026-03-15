# Launch XRPLedgerAmericas — GitHub + Vercel

Use these steps to push the site to your **XRPLedgerAmericas** repo and go live.

---

## 1. Add your logo and preview (if you haven’t)

Copy these into `xrpledgeramericas-site/assets/`:

- **logo.png** (or **logo.jpeg**) — from your saved assets (e.g. Cursor project assets folder)
- **preview.png** — for social/snippet previews

The site works without them; the hero will still show “XRPLedger AMERICAS” and the rest of the layout.

---

## 2. Push this site to GitHub (XRPLedgerAmericas repo)

Your repo: **https://github.com/Shellfish011235/XRPLedgerAmericas**

**Option A — You have the XRPLedgerAmericas repo cloned already**

1. Open the cloned **XRPLedgerAmericas** folder (not the control-room repo).
2. Copy **all contents** of `xrpledgeramericas-site` into that folder (so that folder has `index.html`, `css/`, `assets/`, `README.md` at the top level).
3. In that folder:
   ```powershell
   git add .
   git commit -m "Initial XRPLedgerAmericas site"
   git branch -M main
   git push -u origin main
   ```

**Option B — Clone the repo and copy the site in**

1. In a folder **outside** the control-room project (e.g. `C:\Users\anamb\Projects`):
   ```powershell
   git clone https://github.com/Shellfish011235/XRPLedgerAmericas.git
   cd XRPLedgerAmericas
   ```
2. Copy everything from **this** folder  
   `c:\Users\anamb\xrpl-control-room-gamer-ui\xrpledgeramericas-site`  
   into the cloned `XRPLedgerAmericas` folder (so `index.html`, `css/`, `assets/`, `README.md` are in the repo root).
3. Then:
   ```powershell
   git add .
   git commit -m "Initial XRPLedgerAmericas site"
   git branch -M main
   git push -u origin main
   ```

**Option C — This folder is the only copy; create a new repo from it**

1. Open a terminal in `c:\Users\anamb\xrpl-control-room-gamer-ui\xrpledgeramericas-site`.
2. Run:
   ```powershell
   git init
   git add .
   git commit -m "Initial XRPLedgerAmericas site"
   git branch -M main
   git remote add origin https://github.com/Shellfish011235/XRPLedgerAmericas.git
   git push -u origin main
   ```
   If the repo already has a README on GitHub, use:
   ```powershell
   git pull origin main --allow-unrelated-histories
   git push -u origin main
   ```
   if needed, then push.

---

## 3. Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) and sign in (with GitHub if possible).
2. **Add New** → **Project**.
3. **Import** the **Shellfish011235/XRPLedgerAmericas** repository.
4. Settings:
   - **Framework Preset:** Other
   - **Root Directory:** `./` (leave default)
   - **Build Command:** leave empty (static site)
   - **Output Directory:** leave empty
5. Click **Deploy**. Wait for the build to finish.
6. Your site will be at `https://xrpledgeramericas-xxx.vercel.app` (or similar).

---

## 4. Connect your domain (www.xrpledgeramericas.com)

1. In Vercel: open the project → **Settings** → **Domains**.
2. Add **www.xrpledgeramericas.com** (and optionally **xrpledgeramericas.com**).
3. Vercel will show the DNS records you need (usually a CNAME for `www` and A records for apex).
4. In your domain registrar (where you bought xrpledgeramericas.com), add those records.
5. After DNS propagates (a few minutes to 48 hours), the site will be live at **www.xrpledgeramericas.com**.

---

## 5. Summary

| Step | Action |
|------|--------|
| 1 | Add `logo.png` and `preview.png` to `assets/` (optional but recommended) |
| 2 | Push site contents to **GitHub** repo **Shellfish011235/XRPLedgerAmericas** |
| 3 | **Vercel** → Import repo → Deploy |
| 4 | **Domains** → Add www.xrpledgeramericas.com → Set DNS at registrar |

After this, every push to `main` will trigger a new Vercel deployment.
