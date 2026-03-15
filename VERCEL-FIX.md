# Fix: xrpledgeramericas.com Showing Control Room

Vercel is launching the **Control Room** project for xrpledgeramericas.com. Do the following so the **Americas** site is the one that goes live.

---

## Step 1: Create a separate Vercel project for XRPLedgerAmericas

1. Go to **[vercel.com/dashboard](https://vercel.com/dashboard)** and sign in.
2. Click **"Add New..."** → **"Project"**.
3. Under **Import Git Repository**, find and select **Shellfish011235/XRPLedgerAmericas**.
   - If you don’t see it, click **"Import third-party Git Repository"** and paste:  
     `https://github.com/Shellfish011235/XRPLedgerAmericas`
4. Click **Import**.
5. On the configure screen:
   - **Framework Preset:** Other
   - **Root Directory:** `./` (leave as is)
   - **Build Command:** leave empty
   - **Output Directory:** leave empty
6. Click **Deploy**.
7. Wait for the deployment to finish. You’ll get a URL like `https://xrpledgeramericas-xxxx.vercel.app`. Open it and confirm you see the **Americas** site (dark theme, “The community gateway for XRPL across the Americas”), not the Control Room.

You now have **two** Vercel projects:
- One for **xrpl-control-room-gamer-ui** (Control Room)
- One for **XRPLedgerAmericas** (Americas site)

---

## Step 2: Take the domain off the Control Room project

1. In Vercel, open the **Control Room** project (the one that currently shows when you open xrpledgeramericas.com).
2. Go to **Settings** → **Domains**.
3. If **xrpledgeramericas.com** or **www.xrpledgeramericas.com** is listed, **remove** it (click the three dots or trash icon next to the domain and remove it).

That way the Control Room project will only serve its own URLs (e.g. its `.vercel.app` domain), not xrpledgeramericas.com.

---

## Step 3: Attach the domain to the XRPLedgerAmericas project

1. In Vercel, open the **XRPLedgerAmericas** project (the one you created in Step 1).
2. Go to **Settings** → **Domains**.
3. Click **Add** and enter: **www.xrpledgeramericas.com**
4. Add **xrpledgeramericas.com** as well if you want the non-www version to work.
5. Vercel will show the DNS records you need (e.g. CNAME for `www`).
6. In your **domain registrar** (where you bought xrpledgeramericas.com), add exactly those records. If you already had records pointing to the Control Room project, update them to the values Vercel shows for the **XRPLedgerAmericas** project.

After DNS updates (usually 5–30 minutes), **www.xrpledgeramericas.com** will serve the Americas site and no longer the Control Room.

---

## Summary

| What | Action |
|------|--------|
| **New Vercel project** | Create one that imports **Shellfish011235/XRPLedgerAmericas** only. Deploy and confirm the Americas site on its `.vercel.app` URL. |
| **Control Room project** | Remove **xrpledgeramericas.com** and **www.xrpledgeramericas.com** from its Domains. |
| **XRPLedgerAmericas project** | Add **www.xrpledgeramericas.com** (and optionally **xrpledgeramericas.com**) in Domains and set DNS at your registrar. |

Result: GitHub has the Americas repo; Vercel has two projects (Control Room + XRPLedgerAmericas); only the XRPLedgerAmericas project is connected to xrpledgeramericas.com.
