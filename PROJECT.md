# NUR-FAREENA BT MUSTAFA — Perodua SA Website

**Working file (SOURCE OF TRUTH):** `~/projects/nur-fareena-perodua/index.html`
**Reference cloned from:** peroduasemenyihsales.com (`~/perodua-nurul/index.html`)
**Preview:** https://preview.funnelcraft.my/nur-fareena-perodua/
**Built:** 14 Jul 2026 (web-dev profile)

## Client Data
- Name: Nur-Fareena bt Mustafa
- Phone/WhatsApp: 014-9361401 → wa.me/60149361401
- Email: nurfareenamustafa@gmail.com
- Showroom: Lot 10, Batu 4½, Jalan Ipoh, Kampung Batu, 51200 Kuala Lumpur, WP KL
- Experience: 3 tahun · 7 kereta/bulan

## Build Notes
- USP (4) → "Kenapa Pilih" 6 cards
- OTR prices from client's price image (OCR + cross-checked vs real 2026 pricing) — **PENDING client verify**
- Award section removed (none); profile photo = placeholder (`images/profile-placeholder.jpg`)
- Text testimonials removed (no real reviews — no fabrication)
- Delivery gallery: 18 curated photos from Google Drive (of 64 downloaded)
- GTM removed (was Nurul's container GTM-5QKFZGR9)
- Brochure buttons removed (reference links were dead)
- Form endpoints → `api.funnelcraft.my/api/v1/submit/nur-fareena` + `webhook.funnelcraft.my/lead`

## QA
- Desktop + mobile (390px) vision-verified: no horizontal overflow, no broken images, tables fit, buttons sized correctly.

## PENDING (needs Boss input before deploy)
1. Verify OTR price table against original image
2. Domain name (none assigned yet)
3. Provision backend slug `nur-fareena` + WhatsApp notify → 014-9361401
4. Deploy: GitHub repo → Cloudflare Pages (after confirm)
