PAYCHEKX — Financial Clarity Tools

paychekx-site

PAYCHEKX is a privacy-first, self-service financial clarity system designed to help everyday people understand their cash flow, prioritize bills, and reduce money stress without accounts, tracking, or data collection.

This repository contains the complete static site and tool suite for the PAYCHEKX product line, developed and governed by Artificial Intelligence Capital Ventures (AICV).

Overview

PAYCHEKX is built as a fully static product system:

No backend

No accounts

No authentication

No analytics

No cookies

No data storage

All tools run locally in the user’s browser.

The system is designed for:

One-time purchases via Stripe

Instant access after payment

Offline-friendly operation

Minimal support overhead

Product Scope
Core Pages

/index.html
Main marketing / landing page.

/monetization/index.html
Pricing and Stripe routing page.

/delivery/thank-you.html
Post-purchase confirmation and routing.

/access/index.html
Tool access hub with tier-based gating.

Tools (/tools/)

Each tool is a standalone HTML + JS artifact:

Paycheck Runway Checker

Bill Triage Board

Payday Split Planner

Emergency Micro Budget

Bill Shock Buffer Builder

Money Stress Reality Check

Hidden Bills & Subscription Finder

Debt Pressure Snapshot

All tools:

Run locally

Store no personal data

Do not transmit any information

Monetization Model

PAYCHEKX uses Stripe Payment Links with three tiers:

Tier	Price	Access
Single Tool	$9	One tool, device-locked
Core Bundle	$19	4 essential tools
Full Suite	$29	All 8 tools

Delivery Flow:

User purchases via Stripe

Stripe redirects to /delivery/thank-you.html?tier=...

Thank You page routes to /access/?tier=...

Access page gates tools based on tier

Single Tool tier uses a device-based hard lock via localStorage.

Architecture

Static HTML + CSS + Vanilla JavaScript

No external JS libraries

No frameworks

Designed for GitHub Pages deployment

All routing handled via relative paths and query parameters

Tier detection is handled by:

? tier=single | core | full


Single tool locking is handled via:

localStorage

One-time tool selection per device

Privacy & Data Policy

PAYCHEKX intentionally collects no data.

No accounts

No tracking

No analytics

No cookies

No server-side storage

All computation happens in the user’s browser.

Licensing & Use

PAYCHEKX is proprietary software.

Licensed for personal use only

No resale

No redistribution

No rebranding

No commercial reuse

All branding, structure, and system design are the exclusive intellectual property of Artificial Intelligence Capital Ventures (AICV).

Deployment

Typical deployment:

GitHub Pages

Netlify

Static web hosting

Required assets (per folder as needed):

favicon.ico

aicv-mark.png

paychekx-logo.png

aicv-glyph.svg

All pages assume relative path loading.

Governance

PAYCHEKX v1 is a locked product line

No new tools may be added without version bump

All changes must preserve:

No accounts

No tracking

No backend

Low liability posture

Versioning follows:

v1.x — minor UI or logic refinements

v2.0 — architecture or scope expansion

Founder & Ownership

PAYCHEKX was founded by Elijah L. Cooley
and developed through his venture studio,
Artificial Intelligence Capital Ventures (AICV).

Contact

For licensing, partnerships, or inquiries:

Product: PAYCHEKX

Organization: AICV

Founder: Elijah L. Cooley
