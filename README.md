# Wrek'd Tech — Landing Page

The public landing page for **Wrek'd Tech, LLC**, a South Carolina-based green-tech
startup developing business, compliance-readiness, and R&D pathways for future
electronic waste innovation.

**Tagline:** *Greener Thinking, Smarter Recycling*

Live site: <https://wrekdtech.com>

---

## Purpose

This page is a **public credibility anchor** for exploratory academic, agency,
incubator, advisor, and technical collaboration conversations.

It is **not** a sales site, a repair service site, a recycling-pickup site, an
investor solicitation page, a franchise page, or the R2 Ready web app.

---

## Disclosure & release control

This repository is a **public-safe external disclosure artifact**. Because the
repository and its GitHub Pages deployment may be publicly visible, every file here —
`index.html`, `styles.css`, `README.md`, inline SVGs, code comments, metadata, alt
text, and Open Graph tags — contains only public-safe materials.

It **intentionally excludes** all confidential technical, administrative, legal,
financial, intellectual-property, and partnership materials, including (but not
limited to): Ex-Spec module-level architecture, process parameters, algorithms, or
recovery mechanisms; R2 Ready product architecture, requirement logic, question
banks, or compliance-engine details; financial forecasts, fundraising targets, and
cost models; IP and patent strategy; internal governance, ownership, or cap-table
details; registration or tax identifiers; named institutions, agencies, professors,
advisors, or outreach strategy; and any internal document IDs or controlled planning
artifacts.

Keep this boundary intact when editing: add only public-safe identity, high-level
mission, general Ex-Spec concept, alpha-stage R2 Ready, founder-safe positioning, and
general exploratory-collaboration language.

---

## Tech stack

Intentionally minimal and easy to maintain by hand:

- **Plain HTML5** — semantic, accessible markup (`index.html`)
- **Plain CSS3** — a single stylesheet with CSS custom properties for color and
  spacing (`styles.css`)
- **Inline SVG** — all visuals (circular-economy/circuit motifs, the stylized South
  Carolina outline, concept and network diagrams) are hand-built SVG or CSS. No
  stock photography.
- **No JavaScript** — the mobile navigation uses a CSS-only checkbox toggle.

No frameworks, no build step, no package manager, no bundler, no CMS, no analytics,
and no external font dependency (system font stacks only). The site loads fast and
can be edited directly.

---

## Project structure

```
.
├── index.html      All page markup and copy
├── styles.css      All layout, typography, color, and visual styling
├── CNAME           Custom domain for GitHub Pages (wrekdtech.com)
└── README.md       This file
```

---

## Deployment (GitHub Pages)

This site is hosted via **GitHub Pages** from the repository
[`Shamoka80/wrekdtech`](https://github.com/Shamoka80/wrekdtech).

1. Commit `index.html`, `styles.css`, `CNAME`, and `README.md` to the default branch.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, select
   the default branch and the `/ (root)` folder, then **Save**.
4. The `CNAME` file points the published site at **wrekdtech.com**. Confirm the
   custom domain in **Settings → Pages** and enable **Enforce HTTPS** once the
   certificate is issued.
5. Configure DNS at the domain registrar:
   - An apex (`wrekdtech.com`) `ALIAS`/`ANAME` or `A` records to GitHub Pages IPs, **or**
   - A `CNAME` record for `www` pointing to `shamoka80.github.io`.

GitHub redeploys automatically on every push to the default branch.

---

## Editing guide

- **Copy and structure:** edit `index.html`. Each section is labeled with an HTML
  comment and a stable `id` (`#home`, `#overview`, `#location`, `#ex-spec`,
  `#collaboration`, `#r2-ready`, `#founder`, `#contact`).
- **Colors and spacing:** edit the `:root` custom properties at the top of
  `styles.css` (`--green`, `--blue`, `--bg`, the `--sp-*` scale, etc.).
- **Contact address:** the placeholder `contact@wrekdtech.com` appears in the
  Contact section and footer of `index.html`; update both when a live address is set.

---

## Claim boundaries (current status vs. future intent)

The page is written to present the company accurately and without overclaiming.
Please preserve these boundaries when editing:

- Wrek'd Tech is **currently founder-led from North Charleston, South Carolina**.
- **Orangeburg, South Carolina** is the **designated future headquarters** only.
- Wrek'd Tech does **not** currently operate a recycling facility, ITAD facility,
  lab, warehouse, office, or commercial processing site.
- **Ex-Spec** is a **conceptual** advanced e-waste recovery system at the
  **validation-readiness** stage — no physical prototype exists today.
- **R2 Ready** is an **alpha-stage compliance-readiness initiative**. It does not
  certify facilities, guarantee certification, replace auditors or Certification
  Bodies, override certification processes, or represent SERI or any Certification
  Body.
- The page makes no claim of current customers, revenue, pilots, formal
  partnerships, university or agency backing, employees, advisors, co-founders,
  IP filings, patents, certification authority, or validated/operational technology.

All materials are **informational and exploratory** only.

---

© 2026 Wrek'd Tech, LLC. All rights reserved.
