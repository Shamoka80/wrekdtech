# Wrek'd Tech Logo Branding Implementation

This document records the logo selection and placement strategy for the Wrek'd Tech website refresh.

## Final Source Selections

| Section | Selected Drive source | Reason |
| --- | --- | --- |
| Header | `FULL LOGO 2.png` | Primary horizontal lockup with the logo mark, company name, and tagline. This is the best fit for the top-left header because it establishes brand identity without creating excessive header height. |
| Contact page | `mini FULL LOGO.png` | More balanced than `hiRez1w.png` for a centered contact-page anchor. It retains the logo mark, company name, and tagline but is visually less dominant. |
| Footer | `Logo Symbol.png` | Preferred compact footer mark because it preserves the same gear, lightning, and leaf visual language at higher resolution than `mini.logo.png`. `mini.logo.png` remains an acceptable fallback. |

## Prepared Web Asset Names

The assets should be placed under `assets/brand/` using these names:

| Section | Web asset | Recommended rendered size | Placement logic |
| --- | --- | --- | --- |
| Header | `assets/brand/wrekd-tech-header-logo.svg` | Desktop width: 230–260px; mobile width: 180–210px; max-height: 52px | Top-left inside the sticky header, replacing the inline SVG mark and typed name. Use `object-fit: contain`, no stretching, and preserve normal header height. |
| Contact page | `assets/brand/wrekd-tech-contact-logo.svg` | Width: 180–220px; max-height: 150px | Centered directly above the `Contact` label with 14–18px bottom spacing. This should function as a quiet brand anchor, not a hero logo. |
| Footer | `assets/brand/wrekd-tech-footer-mark.svg` | Width/height: 44–56px desktop; 38–46px mobile | Compact mark beside or above footer identity text. Keep footer vertical padding tight and group social links together in the footer. |

## Transparency / Background Handling

The source images were evaluated visually. The prepared web assets should use transparent backgrounds so the mark and wordage sit cleanly on the site’s dark technical background. White or rectangular source backgrounds should not be carried into the site.

Background-removal method used for the prepared files:

1. Removed only white/near-white edge-connected background regions.
2. Preserved internal metallic highlights in the gear and wordmark.
3. Cropped excess whitespace after transparency cleanup.
4. Added light transparent padding to avoid edge clipping.
5. Exported web-ready transparent logo files.

## Recommended Implementation

The current inline header/footer SVG placeholders should be replaced with image elements using the prepared brand assets. Suggested HTML structure:

```html
<a class="brand" href="#home" aria-label="Wrek'd Tech home">
  <img class="site-logo site-logo--header" src="assets/brand/wrekd-tech-header-logo.svg" alt="Wrek'd Tech">
</a>
```

```html
<img class="contact-logo" src="assets/brand/wrekd-tech-contact-logo.svg" alt="Wrek'd Tech">
<span class="eyebrow" style="justify-content: center;">Contact</span>
```

```html
<img class="footer-logo" src="assets/brand/wrekd-tech-footer-mark.svg" alt="" aria-hidden="true">
```

Suggested CSS:

```css
.site-logo,
.contact-logo,
.footer-logo {
  display: block;
  height: auto;
  object-fit: contain;
}

.site-logo--header {
  width: clamp(180px, 20vw, 260px);
  max-height: 52px;
}

.contact-logo {
  width: clamp(180px, 28vw, 220px);
  max-height: 150px;
  margin: 0 auto 16px;
}

.footer-logo {
  width: 52px;
  max-height: 52px;
  flex: 0 0 auto;
}

.site-footer {
  padding-block: 24px;
}

.social-links {
  display: flex;
  flex-wrap: wrap;
  gap: 10px 14px;
  align-items: center;
}

@media (max-width: 760px) {
  .site-logo--header { width: clamp(170px, 56vw, 210px); }
  .contact-logo { width: min(200px, 64vw); }
  .footer-logo { width: 44px; max-height: 44px; }
}
```

## Review Notes

The previous text-only wordmark selections should not be used as the primary website identity. The logo mark is important because it communicates technology, recycling, energy, and green innovation through the gear, lightning bolt, and leaves. The header and contact page should retain the full visual language, while the footer should use a compact mark to keep the footer efficient.