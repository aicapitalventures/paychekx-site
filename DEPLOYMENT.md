DEPLOYMENT

PAYCHEKX Hosting Checklist

This checklist covers how to deploy PAYCHEKX as a static site with working Stripe redirects and correct file paths.

PAYCHEKX is designed to run with:

Static HTML + CSS + Vanilla JS

No backend

No accounts

No tracking

Stripe Payment Links

1. Required Site Structure

Recommended folder layout:

/ (site root)
  index.html
  favicon.ico
  aicv-mark.png
  paychekx-logo.png
  aicv-glyph.svg

  /monetization/
    index.html

  /delivery/
    thank-you.html

  /access/
    index.html

  /tools/
    Paycheck Runway Checker.html
    Bill Triage Board.html
    Payday Split Planner.html
    Emergency Micro Budget.html
    Bill Shock Buffer Builder.html
    Money Stress Reality Check.html
    Hidden Bills & Subscription Finder.html
    Debt Pressure Snapshot.html


Important:

Keep filenames consistent.

If you rename tool files, update links in /access/index.html.

2. Asset Placement Rules

To avoid broken images across folders, use one of these approaches:

Option A (Recommended): Keep assets at root

Place favicon.ico, aicv-mark.png, paychekx-logo.png, aicv-glyph.svg in the site root.

Reference them from subpages using absolute paths:

/favicon.ico
/aicv-mark.png
/paychekx-logo.png
/aicv-glyph.svg

Option B: Copy assets into each folder

Copy assets into /monetization/, /delivery/, /access/, and optionally /tools/.

Use relative paths.

Option A is cleaner and reduces duplication.

3. Stripe Payment Link Redirects (Critical)

PAYCHEKX uses Stripe Payment Links with success redirects containing tier:

Success URL format:

https://YOURDOMAIN.com/delivery/thank-you.html?tier=single

https://YOURDOMAIN.com/delivery/thank-you.html?tier=core

https://YOURDOMAIN.com/delivery/thank-you.html?tier=full

Checklist:

Confirm each Payment Link has the correct Success URL.

Confirm Cancel URL returns to a safe page (recommended: /monetization/).

Recommended Cancel URL:

https://YOURDOMAIN.com/monetization/

4. Tier Routing Verification

The delivery page must route users to:

/access/?tier=single

/access/?tier=core

/access/?tier=full

Checklist:

Open each of these URLs manually and confirm correct behavior:

https://YOURDOMAIN.com/access/?tier=single

https://YOURDOMAIN.com/access/?tier=core

https://YOURDOMAIN.com/access/?tier=full

5. Single Tool Lock Verification

Single tier uses device-based lock via localStorage.

Checklist:

Purchase or simulate single tier access.

Select a tool once.

Confirm other tools are blocked after selection.

Confirm the lock persists after refresh.

Confirm “debug override” (if enabled) behaves as expected.

Note:

This is not DRM.

It is delivery hygiene and tier enforcement.

6. Local Testing vs Live Hosting Differences

Local file testing (file://) can behave differently than hosted pages.

Checklist:

Always test using a local server for path accuracy when possible.

If using GitHub Pages, test on the real domain because absolute paths and query strings behave as they will for customers.

7. GitHub Pages Deployment
Step-by-step

Push repo to GitHub

Go to Settings → Pages

Select:

Source: Deploy from a branch

Branch: main (or master)

Folder: /root

Save

Checklist:

Wait for Pages URL to populate.

Confirm:

/index.html loads

/monetization/ loads

/delivery/thank-you.html loads

/access/ loads

/tools/ tool pages open

8. Custom Domain (paychekx.com)

If using a custom domain:

Checklist:

Add domain in GitHub Pages / host settings.

Set DNS records correctly:

A records for apex domain or CNAME for www

Ensure HTTPS is enabled.

Confirm that Stripe Success URLs use the final HTTPS domain.

Important:

Stripe redirects must match the real domain exactly.

9. Final Pre-Launch QA (Non-Negotiable)

Do this checklist before running ads:

 All pages load on mobile

 Images display correctly (AICV mark and PAYCHEKX logo)

 Monetization buttons go to correct Stripe links

 Stripe purchase succeeds

 Success redirect lands on Thank You page with correct tier

 Access page shows correct tool set for tier

 Tools open successfully from Access page

 Single tool lock works

 Terms link works (if included)

 No broken links anywhere

10. Post-Launch Monitoring

Without analytics, you still monitor using:

Stripe payments and refund activity

Customer messages or comments

Manual periodic link testing

Recommended:

Run a real $9 purchase test monthly to ensure Stripe redirects still work.

Support Note

PAYCHEKX is intentionally built for minimal support:

No accounts

No password resets

No data recovery

If a customer loses access, the primary recovery method is:

Their Stripe receipt and the access URL structure.
