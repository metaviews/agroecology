# Discord Submission Post — Vibe Coding for Agroecology

**Status:** SAVED FOR LATER. Do not post until content is finalized. Deployment target: Cloudflare Pages via GitHub.

**Channel:** 🧩丨show-your-projects
**Tag:** Minimax-M3
**Hero image:** `hero.png` from the project folder (attach when posting)

---

## Pre-publish checklist

Before posting, work through this in order:

- [ ] **Content lock.** Read all four pages one more time, especially `index.html` ("The fight this sits inside" context paragraph) and `case-maintenance.html` (the "before" snapshot and the four claims). Tweak any wording that doesn't sound like the owner's voice.
- [ ] **GitHub repo.** Create a new repo (suggested name: `vibe-coding-agroecology`). Push the project folder. Set the repo to public.
- [ ] **Cloudflare Pages.** Connect the repo at https://dash.cloudflare.com → Pages → Create application → Connect to Git. Build settings: leave build command empty, build output directory `.` (or `/`). Cloudflare will detect the static site and serve it on first push.
- [ ] **Verify deployment.** Open the `*.pages.dev` URL Cloudflare gives you. Click through all four pages. Generate the tool's outputs to make sure the JSON loads.
- [ ] **Update links.** Replace the bracketed `[link to ...]` placeholders in the post body below with the deployed URLs.
- [ ] **Post.** Upload `hero.png`, paste the post body, hit send.

---

## Title (working)

**Vibe Coding for Agroecology — A Right to Repair Tool, Built by a Farmer with M3**

---

## Post body

[Attach `hero.png` to the post — it shows the project title, the three real machines (vintage Deere 1120, Polaris Ranger EV, Sunward SWE18UF), and the zine / Whole Earth Catalog aesthetic.]

Most "AI for ag" tools are built by engineers for engineers. This project asks: what if a farmer could build their own tools, in their own context, with AI as a coding partner?

M3 makes that possible. Here is a working case from a small farm near Almonte, Ontario: an **Equipment Maintenance Assistant** that turns a farmer's equipment list into a maintenance calendar, a parts list with OEM and aftermarket sourcing, a troubleshooting guide, an operator handoff document, and a printable shop card.

The canonical demo uses three real machines from the farm — a 1967-1975 John Deere 1120 (5,335 hours, vintage, fully DIY-able), a 2022 Polaris Ranger EV (electric, lead-acid, dealer-locked but the batteries are commodity), and a 2021 Sunward SWE18UF excavator (modern, geography-locked rather than DRM-locked). Three different right to repair stories, one tool that handles all three.

The frame is right to repair: the parts list has a "source independently" column, the maintenance calendar flags DIY-able intervals separately from dealer-only steps, the handoff document closes with "leave the next operator better than you found the machine." The whole site is static HTML, file-based, modifiable. No accounts, no SaaS, no platform. Fork it, edit the JSON, redeploy. Or run it on a USB stick in a farm shed with no wifi.

The wider fight is real: the January 2023 John Deere / American Farm Bureau MOU, Colorado's 2024 ag right to repair law, Canada's Bill C-244. The laws say farmers can repair. This tool says farmers can also document, share, and own the knowledge that goes with repair.

The four "why M3" claims — domain translation, pedagogical scaffolding, sovereignty by design, customization at the edge — are walked through on the process page, with concrete "M3 said X, I changed it to Y, because Z" examples from the actual build. The "M3 vs owner" division of labor is the receipt, not a footnote.

Built in collaboration between a farmer (agroecology, right to repair framing, pedagogical sequencing, real farm data) and M3 (synthesis, code, design scaffolding, illustration) via portal.nousresearch.com.

**The site:** [URL — fill in after deploying]
**The case study + working tool:** [URL/case-maintenance.html]
**The process (the contest receipt):** [URL/process.html]

Try the tool. Edit the JSON to your equipment. Build one for your farm.

---

## Deployment — Cloudflare Pages via GitHub

The static site has no build step, so Cloudflare Pages serves it as-is.

**Step 1. Create the GitHub repo.**

```bash
cd /home/farmer/vibe-coding-agroecology
git init
git add .
git commit -m "Initial build: Vibe Coding for Agroecology"
gh repo create vibe-coding-agroecology --public --source=. --remote=origin --push
```

(If `gh` is not authenticated, create the repo on github.com and push manually with `git remote add origin ...` and `git push -u origin main`.)

**Step 2. Connect to Cloudflare Pages.**

- Go to https://dash.cloudflare.com → Pages → Create application → Connect to Git.
- Select the `vibe-coding-agroecology` repo.
- Build settings:
  - **Framework preset:** None
  - **Build command:** (leave empty)
  - **Build output directory:** `/` (or `.`)
- Click "Save and Deploy." Cloudflare deploys on first push and gives you a `vibe-coding-agroecology.pages.dev` URL.

**Step 3. (Optional) Custom domain.**

If you have a domain, add it under "Custom domains" in the Cloudflare Pages project. DNS auto-configures if the domain is already on Cloudflare; otherwise add the CNAME at your registrar.

**Step 4. Future updates.**

Push to `main` → Cloudflare auto-deploys. No build step, no configuration. Edits to `hero.png` or any other file ship on the next push.

---

## File checklist for the submission

- [x] `index.html` — the framing page (with the right to repair context paragraph)
- [x] `case-maintenance.html` — the case study + working tool
- [x] `process.html` — the M3 / owner walkthrough
- [x] `contribute.html` — build one for your farm
- [x] `style.css` — zine system
- [x] `README.md` — license + structure + deployment
- [x] `hero.png` — upload to Discord post
- [x] `submission-post.md` — this file, the saved-for-later post body
