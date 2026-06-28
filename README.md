# Wrek'd Tech — Landing Page

The public landing page for **Wrek'd Tech, LLC**, a South Carolina-based green-tech
startup developing business, compliance-readiness, and R&D pathways for future
electronic waste innovation.

**Tagline:** *Greener Thinking, Smarter Recycling*

Live site: <https://shamoka80.github.io/wrekdtech/>

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
- **Minimal JavaScript** — only for the accessible mobile navigation button toggle.

No frameworks, no build step, no package manager, no bundler, no CMS, no analytics,
and no external font dependency (system font stacks only). The site loads fast and
can be edited directly.

---

## Project structure

```
.
├── index.html      All page markup and copy
├── styles.css      All layout, typography, color, and visual styling
└── README.md       This file
```

---

## Deployment (GitHub Pages)

This site is hosted via **GitHub Pages** from the repository
[`Shamoka80/wrekdtech`](https://github.com/Shamoka80/wrekdtech).

1. Commit `index.html`, `styles.css`, and `README.md` to the default branch.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, select
   the default branch and the `/ (root)` folder, then **Save**.
4. Keep **Settings → Pages → Custom domain** empty for the active default-URL deployment.
5. Do not add a root `CNAME` file while the custom domain is deferred.

GitHub redeploys automatically on every push to the default branch.

---

## Custom domain reconnection (deferred)

The active deployment currently uses the default GitHub Pages URL:
<https://shamoka80.github.io/wrekdtech/>. The custom domain `www.wrekdtech.com`
is deferred and is not the active live-site URL. There must be no active root
`CNAME` file while the site remains on the default GitHub Pages URL.

When custom-domain reconnection is intentionally resumed, use **one canonical
custom domain** for this site: `www.wrekdtech.com`. At that time only, add a root
`CNAME` file containing exactly that hostname, configure the same value in
**Settings → Pages → Custom domain**, and update active metadata such as the
canonical URL and Open Graph URL away from the default GitHub Pages URL.

Before reconnecting the custom domain, configure the public DNS zone for
`wrekdtech.com` as follows:

| Host/name | Record type | Value/target | Purpose |
| --- | --- | --- | --- |
| `www` | `CNAME` | `shamoka80.github.io` | Sends the deferred `www.wrekdtech.com` custom domain to GitHub Pages. Do not point this record at GoDaddy parking, forwarding, or the apex domain. |
| `@` | `A` | `185.199.108.153` | Sends the apex domain to GitHub Pages so GitHub can redirect it to `www` after custom-domain reconnection. |
| `@` | `A` | `185.199.109.153` | GitHub Pages apex IPv4 address. |
| `@` | `A` | `185.199.110.153` | GitHub Pages apex IPv4 address. |
| `@` | `A` | `185.199.111.153` | GitHub Pages apex IPv4 address. |

Optional IPv6 records for `@` may also be added if the DNS provider supports them:
`2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, and
`2606:50c0:8003::153`.

Remove or disable any conflicting records that send `@`, `www`, or wildcard hosts
to GoDaddy Website Builder, GoDaddy parking, domain forwarding, or a default
"Coming Soon" page. In particular, `www` must not have an `A`, `AAAA`, forwarding,
or parked-site record alongside the `CNAME` record when reconnection is resumed.

After DNS changes propagate and the custom domain is intentionally re-enabled,
these checks must be true:

```sh
dig www.wrekdtech.com +nostats +nocomments +nocmd
dig wrekdtech.com +noall +answer -t A
curl -I https://www.wrekdtech.com/
```

Expected reconnection results:

- `www.wrekdtech.com` returns a `CNAME` chain that includes `shamoka80.github.io`.
- `wrekdtech.com` returns only GitHub Pages `A` records unless optional GitHub Pages
  `AAAA` records are also configured.
- `https://www.wrekdtech.com/` is served by GitHub Pages and returns the deployed
  landing page, not a GoDaddy parking or forwarding page.

---

## Editing guide

- **Copy and structure:** edit `index.html`. Each section is labeled with an HTML
  comment and a stable `id` (`#home`, `#overview`, `#location`, `#ex-spec`,
  `#collaboration`, `#r2-ready`, `#founder`, `#contact`).
- **Colors and spacing:** edit the `:root` custom properties at the top of
  `styles.css` (`--green`, `--blue`, `--bg`, the `--sp-*` scale, etc.).
- **Contact address:** `partners@wrekdtech.com` is the public contact address used in
  the Contact section of `index.html`.
- **Public social links:** approved public social links are included as plain text
  links in the Contact section only.

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
