PAYCHEKX Operations Manual

This document is for internal operational continuity.

Stripe Link Rotation

To rotate Stripe links:

Create new Stripe Payment Links

Update monetization page links

Update delivery routing tier mapping

Price Changes

To change prices:

Update Stripe Payment Links

Update pricing text on monetization page

Invalidating a Bad Release

If a tool breaks:

Replace the tool HTML file

Commit and deploy

Tier Debugging

Tier is determined by URL query string:

? tier=single | core | full

Single Tool Lock Reset

Local debug override:

localStorage.removeItem('paychekx_single_tool_lock')

Deployment Flow

Commit changes

Push to GitHub

GitHub Pages auto‑deploys

Stripe Failure Recovery

If Stripe link breaks:

Disable old link

Issue new link

Update monetization page

Architecture Summary

Static HTML

Vanilla JS

No backend

No accounts

No analytics

Governance

PAYCHEKX is a locked product line.

All changes require:

Version bump

Changelog entry

End of Operations Manual.
