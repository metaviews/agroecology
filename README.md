# Vibe Coding for Agroecology

A farmer, an AI coding partner (M3), and a right to repair ethos. Tools built end-to-end for a small farm near Almonte, Ontario.

## About M3

M3 (MiniMax-M3) is a large language model from MiniMax, a foundation model company. Large language models like M3 read and generate text and code in response to prompts; the *vibe coding* approach in this project uses M3 as a coding partner that takes a farmer's domain knowledge and turns it into working software artifacts.

This site was submitted to the **M3 Showcase**, a community challenge for projects built with M3. The four "why M3" claims on this site — domain translation, pedagogical scaffolding, sovereignty by design, customization at the edge — are the submission's argument for what M3 specifically enables in agroecology and right to repair work.

## What this is

A static site with one working case study: the **Equipment Maintenance Assistant**, a tool that turns a farmer's equipment list into a maintenance calendar, parts list (with OEM and aftermarket sourcing), troubleshooting guide, operator handoff document, and printable shop card. Each output is generated locally in the browser, from a JSON file the farmer owns.

The wider project: an argument that M3 has distinctive value for agroecology and right to repair, demonstrated through a real build, not a slide deck. The four claims, with the build artifacts that demonstrate them, are on the site.

## Project structure

```
vibe-coding-agroecology/
├── index.html              ← framing page (the thesis, the four "why M3" claims)
├── case-maintenance.html   ← the case study and the working tool
├── process.html            ← how M3 and the owner built this (the contest receipt)
├── contribute.html         ← build one for your farm (the contribution path)
├── style.css               ← one stylesheet, zine aesthetic, earth tones
└── README.md               ← this file
```

## License

This work is released under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the terms of:
- **Attribution** — you must give appropriate credit, provide a link to the license, and indicate if changes were made
- **ShareAlike** — if you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original

The license choice is deliberate. CC BY-SA matches the right to repair and knowledge-commons ethos: the means of maintenance belong to the operator, the source code belongs to everyone who comes after, and adaptations must remain open.

## Running it locally

Three ways, in order of simplicity:

1. **Open the file.** Download the folder, double-click `index.html`. The site opens in your default browser. The case study works. The maintenance tool works. You are done.

2. **Edit the equipment list and reload.** Open `case-maintenance.html` in a text editor. Find the `DEMO_JSON` near the top of the `<script>` block. Replace the three machines with yours. Save. Reload. The outputs re-render with your data.

3. **Host it on a USB stick in a farm shed.** Copy the folder onto a USB stick. Plug it into any computer with a browser. Open `index.html`. The site works offline. The Google Fonts load will fail (and degrade gracefully to system fonts), but everything else is local. This is the right to repair move: the tool works when the wifi does not.

## Contributing

The honest feedback path is the GitHub Issues page for this project. Open an issue titled with your farm name and the tool you built. Include:

- Your equipment list (or whatever data structure you used)
- What you changed from the demo
- What the tool enabled for you that off-the-shelf ag software did not

There is no analytics on this site, no newsletter signup, no SaaS feedback form. Sovereignty by design means the feedback loop is on the farmer's terms.

## Deployment

The site is a static folder with no build step. Two main paths:

**Cloudflare Pages via GitHub (recommended for a permanent URL):**

1. Create a GitHub repo, push the folder, set it to public.
2. In Cloudflare dashboard → Pages → Create application → Connect to Git, select the repo.
3. Build settings: framework preset None, build command empty, build output directory `/`.
4. Cloudflare deploys on first push and gives you a `*.pages.dev` URL. Custom domain can be added under Custom domains.

Future updates: push to `main` → Cloudflare auto-deploys. No configuration needed.

**Local / offline use:**

See "Running it locally" above. The site works offline once the folder is copied to a USB stick or a Raspberry Pi in a farm shed. The Google Fonts CDN load is the only external dependency and degrades gracefully to system fonts.

## The "why M3" claims

These four claims, made visible on the site, are the contest receipt:

1. **Domain translation** — M3 takes agroecological and right to repair concepts and translates them into structured, working tools that non-coders can actually use.
2. **Pedagogical scaffolding** — M3 produces a traceable process the user can read, modify, and learn from. Vibe coding as popular education, not productivity hack.
3. **Sovereignty by design** — the tools M3 builds are static, file-based, open, and modifiable. The means of production — and maintenance — belong to the operator.
4. **Customization at the edge** — a non-coder with M3 can build the maintenance tool that fits their equipment, at any scale, with no developer in the loop.

The `process.html` page walks through each claim with concrete "M3 said X, I changed it to Y, because Z" examples from the actual build.

## The build itself

- **M3** (MiniMax-M3) did the synthesis: scaffolded the site structure, drafted the case study and process text, built the JavaScript tool, generated the service interval and parts templates. M3 is a large language model from MiniMax; in this project it functioned as a coding partner taking the owner's domain knowledge and turning it into working software artifacts.
- **The owner** did the editorial judgment, the agroecological and right to repair framing, the pedagogical sequencing, the real farm data (three machines from `~/farm-equipment/records/`), and the final "what this means" framing. The pushback on M3 outputs — visible in `process.html` — is the part that made the tool sharper than what M3 would have produced alone.

## Credits and sources

The canonical equipment data in the case study comes from real machine records:

- John Deere 1120 tractor (T1) — vintage, 5,335 hours, German assembly
- Polaris Ranger EV 2022 (UT1) — electric, 145.2 hours, lead-acid pack
- Sunward SWE18UF excavator (E1) — 2021, 64.2 hours, Yanmar engine

Location: Almonte, Ontario, Canada. The right to repair movement context draws on John Deere / U.S. PIRG / Repair.org organizing and on the Colorado, Minnesota, and North Dakota ag right to repair laws (2023-2024).

---

*Built with M3. Static site, no framework, no SaaS. Fork it, edit it, host it on a thumb drive.*
