# AI Dubai Registration — Decision Record

> Lifecycle: populate-once, then append/amend deliberately · Owner: Lead · Load: Always
> Canonical source of truth. Change decisions here first, then update dependent docs.

**Version:** 0.2
**Last updated:** 2026-10-11
**Status:** Draft. Requirements gathering in progress; items marked OPEN await the owner.

## A. Concept

| ID | Decision | Rationale |
|---|---|---|
| D-1 | A WordPress plugin for aidubaiconference.com/2026 (organised by Future 10X) that lets visitors register through a form on the site, emails them a confirmation, lets the organiser email updates and personal QR codes to registrants, and lets each registrant make a shareable "I'm attending" poster with their name and photo. | Owner's goal (2026-10-11). |
| D-2 | Users: **Visitor/registrant** and **Organiser (admin)**. A check-in **Staff** role is OPEN (H-4). | Keeps roles minimal. |
| D-3 | Not in scope: TBD with the owner (see open questions). | |

## B. Foundations

| ID | Decision | Rationale |
|---|---|---|
| D-4 | Standalone vs Eventin attendees: OPEN (H-1). | Eventin already handles events/speakers/schedule and has attendee registration. |

## T. Tech stack

| ID | Decision | Rationale |
|---|---|---|
| D-5 | Runs on the live site: WordPress 7.1, PHP 8.3, Exhibz (classic) + Elementor, alongside Eventin, Wordfence, Yoast, Google Site Kit; Plesk hosting. No build step, no external services required. | Matches the sponsor portal setup the owner already runs. |
| D-6 | Reuse the sponsor portal plugin (halmaaini/sponsor-portal) approaches: `portal.css` tokens and theme-proof button overrides, container-query layout, QR generation, invite-style email flow, no-CAPTCHA spam protection, GitHub updater, `bin/build.sh`. | Proven on this site; owner request. |
| D-7 | One-click updates from the GitHub repo's `main` branch (`dist/` zip); `bin/build.sh` checks the three version numbers match and rebuilds `dist/`. | Owner request; same as sponsor portal. |

## U. Design

| ID | Decision | Rationale |
|---|---|---|
| D-8 | Light, corporate style matching the real site and the approved sponsor portal demo: white page with faint dot texture; violet #3B1D82 titles/links, centred titles with short violet underline; Emirati-green #017330 buttons (4px radius), white + thin violet border secondary; accents magenta #FF057C, orchid #E536F0, blue #5D78FF used sparingly; violet→magenta curve only on banners/headers; white cards, 1px #E4DFF2 border, 8–10px radius; body #4F4A66, muted #7A7590, tint #F7F5FC; Roboto; small inline SVG icons, no emoji. | Earlier attempts were rejected as "gamic". |

## P. Process

| ID | Decision | Rationale |
|---|---|---|
| D-9 | Order of work: questions → clickable demo artifact (incl. poster maker from the owner's sample) → owner approval → plugin build → local end-to-end test → independent code review with every finding fixed → plain-English README. | Owner's working method. |
| D-10 | Commits authored as halmaaini (haithamalmaaini@hotmail.com), no co-author or AI attribution lines. Pull requests only on request. | Owner instruction. |

## Open questions

| ID | Question | Owner | Status |
|---|---|---|---|
| H-1 | Integrate with Eventin attendees or stay standalone? **Recommended: standalone**, with an optional one-way copy into Eventin attendees later. Findings (Eventin 4.1.26 source): attendees are post type `etn-attendee` with undocumented meta; QR codes, check-in scanner, RSVP and custom fields need Eventin Pro; no consent field or privacy export/erase; no bulk email. | Owner | OPEN |
| H-2 | Form fields, free/paid, capacity limits. | Owner | OPEN |
| H-3 | One event or several dates/venues (AI Bus stops). | Owner | OPEN |
| H-4 | QR purpose; staff check-in scanner page. | Owner | OPEN |
| H-5 | Email sending (SMTP), bulk limits, unsubscribe. | Owner | OPEN |
| H-6 | Privacy and consent (UAE PDPL). | Owner | OPEN |
| H-7 | Poster: photo upload/crop, text, sizes, download/share. Awaiting owner's sample. | Owner | OPEN |
| H-8 | Export to Excel. | Owner | OPEN |

## Change history

| Version | Date | Change |
|---|---|---|
| 0.2 | 2026-10-11 | First fill from the owner's brief. |
