# Tará Travel Co. — Going Live Guide

This walks you through everything, slowly, in plain English. Do it in order — each phase depends on the one before it. None of this requires writing code; you'll mostly be clicking buttons in websites and one app.

Your website folder is already prepared:
- `index.html` is your homepage (this used to be `taratravelco-homepage-PREVIEW.html` — renamed so it loads automatically when someone visits your domain).
- A `.gitignore` file tells GitHub to skip junk files (`.bak` backups, `.DS_Store`) so they don't get uploaded.
- Your other pages (booking page, travel guides, etc.) keep their existing file names — they'll work fine as-is.

---

## Phase 1 — Create a GitHub account + install GitHub Desktop

GitHub is just a place to store your website's files online. GitHub Desktop is a free app that lets you upload/update those files by clicking a button — no command line needed.

1. Go to **github.com** and click **Sign up**. Use your email, pick a username, set a password.
2. Go to **desktop.github.com** and download **GitHub Desktop** for Mac. Open it and sign in with the account you just made.

---

## Phase 2 — Upload your website folder to GitHub

If GitHub Desktop's "Let's get started" screen already shows a repo under "Your Repositories" (e.g. `yourname/taratravelco-website`), that means a repo was already created on GitHub.com — use these steps. (If you ever start completely from scratch with no repo listed, use **File → New Repository** instead and point it straight at your `taratravelco-new-website` folder.)

1. Click that repo in the list, then click the blue **Clone [repo name]** button.
2. When asked where to save it, pick somewhere simple like your **Desktop**, then click **Clone**. This downloads an empty (or near-empty) folder linked to your GitHub repo.
3. Open **Finder**. Open the newly cloned folder (it'll be wherever you chose in step 2).
4. Open your `taratravelco-new-website` folder in another Finder window, select everything inside it (`index.html`, `.gitignore`, `GUIDE.md`, the `Media` folder, and all the other `.html` files), and drag them all into the cloned folder from step 3.
5. Switch back to GitHub Desktop — it'll now list all those files under "Changes" on the left.
6. Type a summary at the bottom-left like `Initial upload` and click **Commit to main**.
7. Click **Push origin** in the top bar (it says "push" rather than "publish" since the repo already exists on GitHub).

That's it — your whole site (including the Media folder) is now on GitHub. From now on, always make edits inside the **cloned folder** (the one from step 2), not the original `taratravelco-new-website` folder, so GitHub Desktop can see the changes. Whenever you want to update the live site after an edit, repeat just steps 5–7 — GitHub Desktop will only ask about files that actually changed.

---

## Phase 3 — Deploy it with Vercel

Vercel is the hosting service that actually serves your site to visitors, and it auto-updates every time you push changes to GitHub.

1. Go to **vercel.com** and click **Sign Up** → choose **Continue with GitHub** (this links the two automatically).
2. Click **Add New...** → **Project**.
3. Find `tara-travel-website` in the list and click **Import**.
4. On the settings screen: under **Framework Preset**, choose **Other** (your site is plain HTML, no build step needed). Leave everything else as default.
5. Click **Deploy**. Wait about 30–60 seconds.
6. You'll get a free working link like `tara-travel-website.vercel.app` — click it to check your live site loads correctly before moving on.

---

## Phase 4 — Point your real domain to Vercel

Important: this does **not** require moving your domain away from Hostinger or canceling anything there. You're just telling your domain to *show* the Vercel-hosted site instead of the Hostinger-hosted one. You keep owning/renewing the domain at Hostinger exactly as before.

⚠️ **Before you touch anything: if you use email at your domain (e.g. info@taratravel...), read this first.** Email and website hosting use separate DNS records (MX records for email, A/CNAME records for the website). As long as you only change the records Vercel tells you to (step 3 below) and don't change your domain's nameservers wholesale, your email keeps working untouched. If you're not sure which method Hostinger uses for your email, it's worth a quick check with Hostinger support before this step, just to be safe.

1. In your Vercel project, go to **Settings → Domains**. Type in your domain (e.g. `taratravel.co`) and click **Add**.
2. Vercel will show you 1–2 DNS records to add — usually an **A record** (pointing `@` to an IP address) and a **CNAME record** (pointing `www` to `cname.vercel-dns.com`). Keep this tab open.
3. Log into **Hostinger** → go to your domain's **DNS / Zone Editor**.
4. Add the exact records Vercel showed you. Don't delete your existing **MX records** (those are what make email work) — only add/edit the A and CNAME records for the website.
5. Save. DNS changes can take anywhere from a few minutes to a few hours to take effect. Vercel's Domains page will show a green checkmark once it's verified.

---

## Phase 5 — Get the trip-planner form to actually email you

Right now, when someone fills out and submits the trip planner form, the data goes nowhere — there's no inbox connected to it yet. Here's the free, no-code fix:

1. Go to **formspree.io** and sign up free.
2. Click **New Form**, give it a name like "Tará Trip Planner", and set the notification email to wherever you want submissions to land (e.g. info@taratravel...).
3. Formspree will show you a unique endpoint URL that looks like `https://formspree.io/f/abcd1234`.
4. Send me that exact URL — I'll paste it into `index.html` in place of the placeholder (it's currently `https://formspree.io/f/REPLACE_WITH_YOUR_FORM_ID`), and you'll just need to commit + push that one change in GitHub Desktop (Phase 2, steps 5–7) for it to go live.
5. Test it: fill out the form on your live site once, then check your email — you should get the submission within a minute.

---

## Quick recap of how future edits work

1. I (or you) edit a file in your `taratravelco-new-website` folder.
2. Open GitHub Desktop → you'll see the changed file(s) → write a short summary → **Commit to main** → **Push origin**.
3. Vercel automatically redeploys your live site within about a minute. No other steps needed.
