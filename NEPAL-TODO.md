# Nepal landing page — LOCAL ONLY (not live)

This folder is a duplicate of the Bangladesh landing page with country/language/phone
substitutions applied automatically. **Do not deploy until the Nepal content arrives and the
items below are reviewed.**

## What was changed automatically
- Bangladesh → Nepal, Bangladeshi → Nepali, Bengali → Nepali (all copy, titles, meta, JSON-LD)
- 🇧🇩 → 🇳🇵 flags; "For patients and families in Nepal" badge
- Phone prefix +880 → +977; form placeholder 98XXXXXXXX; city placeholder Kathmandu
- Language toggle: English / नेपाली (Google Translate `ne,en`)
- WhatsApp pre-filled messages say "contacting you from Nepal"
- `lead.php`: subject "[Nepal Lead — …]", sender name "GlobalCare Nepal Landing Page",
  backup folder `/home/rx/storage/nepal_leads`, +977 number normalisation
- `.htaccess` RewriteBase `/nepal/` (planned live path: https://4rx.co/nepal/)

## Must review when the Nepal content arrives
1. **Visa / VIL wording** — DONE (visa chip, support bullet and visa FAQ commented out; other sentences reworded to "no visa required for Nepali citizens"). Re-check when the Nepal copy arrives. Original note: Nepali citizens do not need a visa for India. The Bangladesh page
   talks about the medical visa and the hospital Visa Invitation Letter (VIL) in the hero chips,
   How It Works step 6, Nepal-support bullets, FAQ and footer. Replace with the actual Nepal
   travel/entry guidance GlobalCare provides.
2. **Hero / section copy** — the wording is still the Bangladesh SEO copy with the country name
   swapped. Replace with the Nepal document (H1, subheading, FAQ, meta title/description, keywords).
3. **Hospital list** — confirm which hospitals GlobalCare routes Nepal patients to (currently the
   same 9 as Bangladesh).
4. **Contact number / WhatsApp** — currently +91 92113 12666 (same as Bangladesh). Confirm the
   number and email for Nepal enquiries; change `LEAD_TO` in `lead.php` if a different inbox.
5. **Patient stories** — the Facebook videos and photos are the same as the Bangladesh page.
   Swap in Nepal patient stories if available (with consent).
6. **Numbers** (128+, 150+, 7,500+, 3,100+) — confirm they apply.
7. **Google Ads URLs** once live: `/nepal/`, `/nepal/bmt`, `/nepal/cardiac`.

## Local preview
Run from the Claude Code browser pane: launch config `np-landing-php` (http://localhost:8766),
or:

    C:/xampp/php/php.exe -S localhost:8766 -t globalcare-bangladesh-landing-page/globalcare-bangladesh-landing-page/nepal-landing-page

## Go-live (later)
Upload the folder contents (excluding README/TODO/vercel.json) to `/home/rx/public_html/nepal/`
on the 4rx.co server and `chown -R rx:rx` it, the same way as the Bangladesh page.
