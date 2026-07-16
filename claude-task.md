# Task: Design & Beautification Audit — neenaperodua website (READ-ONLY)

## Context
- Project: /home/hamiddi/projects/neenaperodua
- This is a Malaysian Perodua sales advisor (SA) landing site, deployed at https://neenaperodua.pages.dev
- Files to audit:
  - index.html — main SA landing page (Malay copy, model cards, price tables, loan calculator, lead form)
  - qv-e.html — Perodua QV-E EV landing page (cloned 1:1 from the official ev.perodua.com.my — DOM + compiled CSS reused intentionally; do NOT flag the clone approach itself as an issue)
  - assets/index-D4yxpEu2.css — compiled CSS used by qv-e.html
- This is an AUDIT ONLY. You must NOT modify any file.

## Scope — audit both pages against these checklists

### A. Emoji scan
- Any emoji in buttons/CTAs, nav, badges, section headings, CSS ::before/::after content, or inline-styled elements. Professional pages must use inline SVG, not emoji.

### B. Link validation (critical)
- WhatsApp links: extract all wa.me/ numbers — flag double country code (60 + 60...), wrong length (valid MY mobile = 60 + 9-10 digits).
- tel: links — inconsistent formatting.
- Empty href="" or href="#" dead links.
- Internal links pointing to files/anchors that do not exist in the project.

### C. Structure & hierarchy
- Exactly one h1 per page.
- Consistent section vertical padding; sections missing from padding selectors.
- Mobile nav: if links hidden on mobile, is there a hamburger/flyover replacement?
- Classes used in HTML that have NO matching CSS rule (silent fallthrough).
- Classes named *-grid that lack display:grid.
- Empty ::before/::after with content:'' creating phantom flex items.

### D. Buttons/CTAs
- Any width:100% / stretched buttons (must be width:auto fit-to-text).
- Three-layer contrast: button text vs button bg vs section bg.
- Consistent CTA sizing across the page.
- !important conflicts making outline buttons invisible on dark sections.

### E. Mobile (375px reasoning from code)
- Anything in the CSS/HTML that would cause horizontal overflow at 375px (fixed widths >375px, 100vw usage, large min-widths, tables without overflow wrappers).
- Body text below 16px on mobile.
- Tap targets below 44px.
- Dark sections with only 16px side padding.

### F. Performance / technical
- Render-blocking or duplicate font loads, unused large assets referenced, missing image lazy-loading, missing meta description, oversized inline base64 images.
- Broken image references (src pointing to files that don't exist in the project folder — verify with ls).
- JS errors likely at runtime (functions referenced but not defined, listeners on missing elements).

### G. Copywriting (index.html only, Malay)
- H1 leads with price/benefit vs abstract.
- CTA action-driven.
- Any use of the words "loan" or "pinjaman" in VISIBLE text (forbidden for car pages — must be "pembiayaan"; JS function names are fine).

## Output format
Return a structured report:
1. CRITICAL issues (broken/blocking) — file, line/selector, evidence, suggested fix
2. MAJOR issues (visual/conversion impact)
3. MINOR issues (polish)
4. PASSED checks (one-line list)
Keep it factual. Cite exact line numbers or grep evidence for every claim. No fabricated findings — if a check passes, say it passes.

## DO NOT
- Do not edit, write, or create any file.
- Do not run git commands that change state.
- Do not flag the qv-e.html clone strategy, its inline data-URI images, or its Vue data-v attributes as issues — they are intentional.
- Do not audit files in images/ or archive/ folders beyond existence checks.
